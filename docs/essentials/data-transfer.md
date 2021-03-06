---
title: 'Xamarin.Essentials: Datenübertragung'
description: Die DataTransfer-Klasse in Xamarin.Essentials ermöglicht eine Anwendung zum Freigeben von Daten, z. B. Text und Web Links zu anderen Anwendungen auf dem Gerät.
ms.assetid: B7B01D55-0129-4C87-B515-89F8F4E94665
author: jamesmontemagno
ms.author: jamont
ms.date: 05/04/2018
ms.openlocfilehash: 31e27556a6681b144084d2177cf3fde8fe8e5459
ms.sourcegitcommit: 51c274f37369d8965b68ff587e1c2d9865f85da7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/30/2018
ms.locfileid: "39353518"
---
# <a name="xamarinessentials-data-transfer"></a>Xamarin.Essentials: Datenübertragung

![Vorabversionen von NuGet](~/media/shared/pre-release.png)

Die **DataTransfer** -Klasse kann eine Anwendung zum Freigeben von Daten, z. B. Text und Web Links zu anderen Anwendungen auf dem Gerät.

## <a name="using-data-transfer"></a>Verwenden die Datenübertragung

Fügen Sie einen Verweis auf Xamarin.Essentials in Ihrer Klasse hinzu:

```csharp
using Xamarin.Essentials;
```

Die Funktionalität zum Übertragen von Daten erfolgt durch Aufrufen der `RequestAsync` -Methode mit einer Anforderungsnutzlast für Daten, die Informationen zum Freigeben für andere Anwendungen enthält. Text und Uri können kombiniert werden, und jede Plattform Filterung basierend auf den Inhalt behandelt.

```csharp

public class DataTransferTest
{
    public async Task ShareText(string text)
    {
        await DataTransfer.RequestAsync(new ShareTextRequest
            {
                Text = text,
                Title = "Share Text"
            });
    }

    public async Task ShareUri(string uri)
    {
        await DataTransfer.RequestAsync(new ShareTextRequest
            {
                Uri = uri,
                Title = "Share Web Link"
            });
    }
}
```

Die Benutzeroberfläche an externe Anwendung freigeben, die angezeigt wird, wenn die Anforderung gesendet wird:

![Datenübertragung](data-transfer-images/data-transfer.png)

## <a name="platform-differences"></a>Plattformunterschiede

# <a name="androidtabandroid"></a>[Android](#tab/android)

* `Subject` Eigenschaft wird für die gewünschte Betreff einer Nachricht verwendet.

# <a name="iostabios"></a>[iOS](#tab/ios)

* `Subject` Nicht verwendet.
* `Title` Nicht verwendet.

# <a name="uwptabuwp"></a>[UWP](#tab/uwp)

* `Title` wird standardmäßig die Anwendungsname Wenn nicht festgelegt.
* `Subject` Nicht verwendet.

-----

## <a name="api"></a>API

- [Data Transfer-Quellcode](https://github.com/xamarin/Essentials/tree/master/Xamarin.Essentials/DataTransfer)
- [Data Transfer API-Dokumentation](xref:Xamarin.Essentials.DataTransfer)

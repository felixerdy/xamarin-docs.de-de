---
title: Xamarin.Forms-Zellen
description: Xamarin.Forms-Zellen können durch ListViews und TableViews hinzugefügt werden. Dieser Artikel beschreibt die Zellen in Xamarin.Forms enthalten.
ms.prod: xamarin
ms.assetid: 77DA0C89-35D6-4C09-A072-3ADE53FD56CF
ms.technology: xamarin-forms
author: davidbritch
ms.author: dabritch
ms.date: 01/12/2016
ms.openlocfilehash: 3b69aaf0a10468a5950e0ccf5a61ab6ecbbc110f
ms.sourcegitcommit: 6e955f6851794d58334d41f7a550d93a47e834d2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/12/2018
ms.locfileid: "38995919"
---
# <a name="xamarinforms-cells"></a>Xamarin.Forms-Zellen

_Xamarin.Forms-Zellen können durch ListViews und TableViews hinzugefügt werden._

Ein *Zelle* ist eine spezielle Element für Elemente in einer Tabelle verwendet, und beschreibt, wie jedes Element in einer Liste gerendert werden soll. Die [ `Cell` ](xref:Xamarin.Forms.Cell) Klasse leitet sich von [ `Element` ](xref:Xamarin.Forms.Element), von dem [ `VisualElement` ](xref:Xamarin.Forms.Element) auch abgeleitet wird. Eine Zelle ist nicht selbst ein visuelles Element; Es wird stattdessen eine Vorlage für ein visuelles Element erstellen.

`Cell` wird verwendet, ausschließlich mit [ `ListView` ](views.md#listView) und [ `TableView` ](views.md#tableView) Steuerelemente. Weitere Informationen zum verwenden und Anpassen von Zellen, finden Sie in der [ `ListView` ](~/xamarin-forms/user-interface/listview/index.md) und [ `TableView` ](~/xamarin-forms/user-interface/tableview.md) Dokumentation.

## <a name="cells"></a>Zellen

Xamarin.Forms unterstützt die folgenden Zellentypen:

<a name="textCell" />

### <a name="textcell"></a>TextCell

|     |     |
| --- | --- |
| Ein [ `TextCell` ](xref:Xamarin.Forms.TextCell) zeigt ein oder zwei Textzeichenfolgen. Legen Sie die [ `Text` ](xref:Xamarin.Forms.TextCell.Text) Eigenschaft und optional die [ `Detail` ](xref:Xamarin.Forms.TextCell.Detail) Eigenschaft, um diese Textzeichenfolgen.<br /><br />[API-Dokumentation](xref:Xamarin.Forms.TextCell) / [Handbuch](~/xamarin-forms/user-interface/listview/customizing-cell-appearance.md#TextCell) | [![Beispiel für TextCell](cells-images/TextCell.png "TextCell Beispiel")](cells-images/TextCell-Large.png#lightbox "TextCell-Beispiel")<br />[C#-Code für diese Seite](https://github.com/xamarin/xamarin-forms-samples/blob/master/FormsGallery/FormsGallery/FormsGallery/CodeExamples/TextCellDemoPage.cs) / [XAML-Seite](https://github.com/xamarin/xamarin-forms-samples/blob/master/FormsGallery/FormsGallery/FormsGallery/XamlExamples/TextCellDemoPage.xaml) |
|     |     |

### <a name="imagecell"></a>ImageCell

|     |     |
| --- | --- |
| Die [ `ImageCell` ](xref:Xamarin.Forms.ImageCell) zeigt dieselbe Informationen wie [ `TextCell` ](#textCell) enthält eine Bitmap, die Sie eingerichtet, aber die [ `Source` ](xref:Xamarin.Forms.Image.Source) Eigenschaft.<br /><br />[API-Dokumentation](xref:Xamarin.Forms.ImageCell) / [Handbuch](~/xamarin-forms/user-interface/listview/customizing-cell-appearance.md#ImageCell) | [![Beispiel für ImageCell](cells-images/ImageCell.png "ImageCell Beispiel")](cells-images/ImageCell-Large.png#lightbox "ImageCell-Beispiel")<br />[C#-Code für diese Seite](https://github.com/xamarin/xamarin-forms-samples/blob/master/FormsGallery/FormsGallery/FormsGallery/CodeExamples/ImageCellDemoPage.cs) / [XAML-Seite](https://github.com/xamarin/xamarin-forms-samples/blob/master/FormsGallery/FormsGallery/FormsGallery/XamlExamples/ImageCellDemoPage.xaml) |
|     |     |

### <a name="switchcell"></a>SwitchCell

|     |     |
| --- | --- |
| Die [ `SwitchCell` ](xref:Xamarin.Forms.SwitchCell) enthält Text, legen Sie mit der [ `Text`"](xref:Xamarin.Forms.SwitchCell.Text) Eigenschaft und und in/aus-Schalter, die anfänglich mit dem booleschen festgelegt [ `On` ](xref:Xamarin.Forms.SwitchCell.On) Eigenschaft. Behandeln der [ `OnChanged` ](xref:Xamarin.Forms.SwitchCell.OnChanged) Ereignis, wann die `On` eigenschaftenänderungen.<br /><br />[API-Dokumentation](xref:Xamarin.Forms.SwitchCell) / [Handbuch](~/xamarin-forms/user-interface/tableview.md#switchcell) | [![Beispiel für SwitchCell](cells-images/SwitchCell.png "SwitchCell Beispiel")](cells-images/SwitchCell-Large.png#lightbox "SwitchCell-Beispiel")<br />[C#-Code für diese Seite](https://github.com/xamarin/xamarin-forms-samples/blob/master/FormsGallery/FormsGallery/FormsGallery/CodeExamples/SwitchCellDemoPage.cs) / [XAML-Seite](https://github.com/xamarin/xamarin-forms-samples/blob/master/FormsGallery/FormsGallery/FormsGallery/XamlExamples/SwitchCellDemoPage.xaml) |
|     |     |

### <a name="entrycell"></a>EntryCell

|     |     |
| --- | --- |
| Die [ `EntryCell` ](xref:Xamarin.Forms.EntryCell) definiert eine [ `Label` ](xref:Xamarin.Forms.EntryCell.Label) , die die Zelle und bearbeitbaren Text in eine einzige Zeile identifiziert die [ `Text` ](xref:Xamarin.Forms.EntryCell.Text) Eigenschaft. Behandeln der [ `Completed` ](xref:Xamarin.Forms.EntryCell.Completed) Ereignis benachrichtigt werden, wenn der Benutzer die Texteingabe abgeschlossen hat.<br /><br />[API-Dokumentation](xref:Xamarin.Forms.EntryCell) / [Handbuch](~/xamarin-forms/user-interface/tableview.md#entrycell) | [![Beispiel für EntryCell](cells-images/EntryCell.png "EntryCell Beispiel")](cells-images/EntryCell-Large.png#lightbox "EntryCell-Beispiel")<br />[C#-Code für diese Seite](https://github.com/xamarin/xamarin-forms-samples/blob/master/FormsGallery/FormsGallery/FormsGallery/CodeExamples/EntryCellDemoPage.cs) / [XAML-Seite](https://github.com/xamarin/xamarin-forms-samples/blob/master/FormsGallery/FormsGallery/FormsGallery/XamlExamples/EntryCellDemoPage.xaml) |
|     |     |


## <a name="related-links"></a>Verwandte Links

- [Introduction to Xamarin.Forms (Einführung in Xamarin.Forms)](~/xamarin-forms/get-started/introduction-to-xamarin-forms.md)
- [Beispiel für Xamarin.Forms FormsGallery](https://developer.xamarin.com/samples/xamarin-forms/FormsGallery/)
- [Xamarin.Forms Samples (Beispiele für Xamarin.Forms)](https://developer.xamarin.com/samples/xamarin-forms/all/)
- [Xamarin.Forms-API-Dokumentation](https://docs.microsoft.com/dotnet/api/xamarin.forms?view=xamarin-forms)

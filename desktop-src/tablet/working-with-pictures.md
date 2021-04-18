---
description: Questo argomento descrive come modificare le immagini usando la proprietà System. Windows. Forms. PictureBox. SizeMode e come visualizzare le immagini in Microsoft Visual Studio .NET.
ms.assetid: 9f4f0f96-68a3-447d-a239-599c9fd3e343
title: Uso delle immagini
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af3a90c0d18253eaf4aea60eafc48bd1c24fcc3e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307950"
---
# <a name="working-with-pictures"></a>Uso delle immagini

Questo argomento descrive come modificare le immagini usando la proprietà [System. Windows. Forms. PictureBox. SizeMode](/dotnet/api/system.windows.forms.picturebox.sizemode?view=netcore-3.1) e come visualizzare le immagini in Microsoft Visual Studio .NET.

## <a name="the-sizemode-property"></a>Proprietà SizeMode

È possibile specificare il modo in cui un'immagine si integra nel controllo con la proprietà [SizeMode](/dotnet/api/system.windows.forms.picturebox.sizemode?view=netcore-3.1) . La proprietà SizeMode è disponibile sia nella libreria gestita che nella libreria di automazione. Con SizeMode è possibile:

-   Ridimensionare i bordi del controllo in modo da adattarli a un'immagine.
-   Estendere un'immagine per adattarla ai bordi del controllo.
-   Centrare un'immagine all'interno dei bordi del controllo.
-   Ancorare un'immagine all'area superiore sinistra del controllo senza ridimensionare l'immagine o il controllo (alcune immagini potrebbero non essere visualizzabili se non si ridimensiona l'immagine o il controllo).

## <a name="working-with-pictures-in-visual-studio-net"></a>Uso delle immagini in Visual Studio .NET

Per visualizzare un'immagine in fase di progettazione in Visual Studio .NET:

1.  Trascinare un controllo [InkPicture](/previous-versions/aa514604(v=msdn.10)) in un form oppure fare doppio clic sul controllo InkPicture nella casella degli strumenti.
2.  Nella finestra **Proprietà** selezionare la proprietà **immagine** , quindi fare clic sul pulsante con i puntini di sospensione per aprire la finestra di dialogo **Apri** .
3.  Se si sta cercando un tipo di file specifico, ad esempio file con estensione jpg, selezionarlo nella casella **tipo file** .
4.  Selezionare il file che si desidera visualizzare.

Per cancellare l'immagine in fase di progettazione:

1.  Nella finestra **Proprietà** selezionare la proprietà **immagine** e fare clic con il pulsante destro del mouse sull'immagine di anteprima.
2.  Fare clic su **Reimposta**.

Il controllo [InkPicture](/previous-versions/aa514604(v=msdn.10)) viene visualizzato per impostazione predefinita senza bordi. È possibile specificare un bordo standard o tridimensionale usando la proprietà [BorderStyle](/dotnet/api/system.windows.forms.picturebox.borderstyle?view=netcore-3.1) per distinguere la casella InkPicture dal resto del form, anche se non contiene alcuna immagine.

È possibile visualizzare un'immagine in fase di esecuzione con il metodo [FromFile](/dotnet/api/system.drawing.image.fromfile?view=dotnet-plat-ext-3.1&preserve-view=true) dell'oggetto [System. Drawing. image](/dotnet/api/system.drawing.image?view=dotnet-plat-ext-3.1&preserve-view=true) :


```C++
ctlInkPicture.Image = Image.FromFile("c:\myImageFile")
```



È anche possibile includere un'immagine di sfondo con la proprietà [BackgroundImage](/dotnet/api/system.windows.forms.control.backgroundimage?view=netcore-3.1) dell'oggetto [Image](/dotnet/api/system.drawing.image?view=dotnet-plat-ext-3.1&preserve-view=true) ereditato. Tuttavia, l'immagine non può essere ridimensionata.

 

 

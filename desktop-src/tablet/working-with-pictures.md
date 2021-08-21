---
description: Questo argomento descrive come modificare le immagini usando il sistema. Windows. Proprietà Forms.PictureBox.SizeMode e come visualizzare immagini in Microsoft Visual Studio .NET.
ms.assetid: 9f4f0f96-68a3-447d-a239-599c9fd3e343
title: Uso delle immagini
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad6e3331d384f30084082e8ef29c5a3a5b44232843bc834a8282bf1786a088d8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118449178"
---
# <a name="working-with-pictures"></a>Uso delle immagini

Questo argomento descrive come modificare le immagini usando [System.Windows. Proprietà Forms.PictureBox.SizeMode](/dotnet/api/system.windows.forms.picturebox.sizemode?view=netcore-3.1) e come visualizzare immagini in Microsoft Visual Studio .NET.

## <a name="the-sizemode-property"></a>Proprietà SizeMode

È possibile specificare il modo in cui un'immagine si adatta al controllo con la [proprietà SizeMode.](/dotnet/api/system.windows.forms.picturebox.sizemode?view=netcore-3.1) La proprietà SizeMode è disponibile sia nella libreria gestita che nella libreria di automazione. Con SizeMode è possibile:

-   Ridimensionare i bordi del controllo per adattarlo a un'immagine.
-   Estendere un'immagine per adattarla ai bordi del controllo.
-   Centrare un'immagine all'interno dei bordi del controllo.
-   Ancorare un'immagine all'area superiore sinistra del controllo senza ridimensionare l'immagine o il controllo .Parte dell'immagine potrebbe non essere visualizzabile se non si ridimensiona l'immagine o il controllo.

## <a name="working-with-pictures-in-visual-studio-net"></a>Uso delle immagini in Visual Studio .NET

Per visualizzare un'immagine in fase di progettazione in Visual Studio .NET:

1.  Trascinare [un controllo InkPicture](/previous-versions/aa514604(v=msdn.10)) in un form oppure fare doppio clic sul controllo InkPicture nella casella degli strumenti.
2.  Nella finestra **Proprietà** selezionare la **proprietà Immagine** e quindi fare clic sul pulsante con i puntini di sospensione per aprire la **finestra di** dialogo Apri.
3.  Se si sta cercando un tipo di file specifico, ad esempio .jpg file, selezionarlo nella **casella File di** tipo .
4.  Selezionare il file da visualizzare.

Per cancellare l'immagine in fase di progettazione:

1.  Nella finestra **Proprietà selezionare** la proprietà **Immagine** e fare clic con il pulsante destro del mouse sull'immagine di anteprima.
2.  Fare clic su **Reimposta**.

Il [controllo InkPicture](/previous-versions/aa514604(v=msdn.10)) viene visualizzato per impostazione predefinita senza bordi. Puoi specificare un bordo standard o tridimensionale usando la proprietà [BorderStyle](/dotnet/api/system.windows.forms.picturebox.borderstyle?view=netcore-3.1) per distinguere la casella InkPicture dal resto del form, anche se non contiene alcuna immagine.

È possibile visualizzare un'immagine in fase di esecuzione con il metodo [FromFile](/dotnet/api/system.drawing.image.fromfile?view=dotnet-plat-ext-3.1&preserve-view=true) dell'oggetto [System.Drawing.Image:](/dotnet/api/system.drawing.image?view=dotnet-plat-ext-3.1&preserve-view=true)


```C++
ctlInkPicture.Image = Image.FromFile("c:\myImageFile")
```



È anche possibile includere un'immagine di sfondo con la proprietà [BackgroundImage](/dotnet/api/system.drawing.image?view=dotnet-plat-ext-3.1&preserve-view=true) dell'oggetto [Image ereditato.](/dotnet/api/system.windows.forms.control.backgroundimage?view=netcore-3.1) Tuttavia, tale immagine non può essere ridimensionata.

 

 

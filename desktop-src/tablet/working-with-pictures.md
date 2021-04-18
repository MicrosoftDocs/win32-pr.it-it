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
# <a name="working-with-pictures"></a><span data-ttu-id="0f753-103">Uso delle immagini</span><span class="sxs-lookup"><span data-stu-id="0f753-103">Working with Pictures</span></span>

<span data-ttu-id="0f753-104">Questo argomento descrive come modificare le immagini usando la proprietà [System. Windows. Forms. PictureBox. SizeMode](/dotnet/api/system.windows.forms.picturebox.sizemode?view=netcore-3.1) e come visualizzare le immagini in Microsoft Visual Studio .NET.</span><span class="sxs-lookup"><span data-stu-id="0f753-104">This topic describes how to adjust pictures using the [System.Windows.Forms.PictureBox.SizeMode](/dotnet/api/system.windows.forms.picturebox.sizemode?view=netcore-3.1) property, and how to display pictures in Microsoft Visual Studio .NET.</span></span>

## <a name="the-sizemode-property"></a><span data-ttu-id="0f753-105">Proprietà SizeMode</span><span class="sxs-lookup"><span data-stu-id="0f753-105">The SizeMode Property</span></span>

<span data-ttu-id="0f753-106">È possibile specificare il modo in cui un'immagine si integra nel controllo con la proprietà [SizeMode](/dotnet/api/system.windows.forms.picturebox.sizemode?view=netcore-3.1) .</span><span class="sxs-lookup"><span data-stu-id="0f753-106">You can specify how an image fits in the control with the [SizeMode](/dotnet/api/system.windows.forms.picturebox.sizemode?view=netcore-3.1) property.</span></span> <span data-ttu-id="0f753-107">La proprietà SizeMode è disponibile sia nella libreria gestita che nella libreria di automazione.</span><span class="sxs-lookup"><span data-stu-id="0f753-107">The SizeMode property is available in both the Managed Library and in the Automation Library.</span></span> <span data-ttu-id="0f753-108">Con SizeMode è possibile:</span><span class="sxs-lookup"><span data-stu-id="0f753-108">With SizeMode you can:</span></span>

-   <span data-ttu-id="0f753-109">Ridimensionare i bordi del controllo in modo da adattarli a un'immagine.</span><span class="sxs-lookup"><span data-stu-id="0f753-109">Resize the control borders to fit an image.</span></span>
-   <span data-ttu-id="0f753-110">Estendere un'immagine per adattarla ai bordi del controllo.</span><span class="sxs-lookup"><span data-stu-id="0f753-110">Stretch an image to fit the control borders.</span></span>
-   <span data-ttu-id="0f753-111">Centrare un'immagine all'interno dei bordi del controllo.</span><span class="sxs-lookup"><span data-stu-id="0f753-111">Center an image within the control borders.</span></span>
-   <span data-ttu-id="0f753-112">Ancorare un'immagine all'area superiore sinistra del controllo senza ridimensionare l'immagine o il controllo (alcune immagini potrebbero non essere visualizzabili se non si ridimensiona l'immagine o il controllo).</span><span class="sxs-lookup"><span data-stu-id="0f753-112">Anchor an image to the upper-left area of the control without resizing the image or control (some of the image may not be viewable if you do not resize the image or control).</span></span>

## <a name="working-with-pictures-in-visual-studio-net"></a><span data-ttu-id="0f753-113">Uso delle immagini in Visual Studio .NET</span><span class="sxs-lookup"><span data-stu-id="0f753-113">Working with Pictures in Visual Studio .NET</span></span>

<span data-ttu-id="0f753-114">Per visualizzare un'immagine in fase di progettazione in Visual Studio .NET:</span><span class="sxs-lookup"><span data-stu-id="0f753-114">To display an image at design time in Visual Studio .NET:</span></span>

1.  <span data-ttu-id="0f753-115">Trascinare un controllo [InkPicture](/previous-versions/aa514604(v=msdn.10)) in un form oppure fare doppio clic sul controllo InkPicture nella casella degli strumenti.</span><span class="sxs-lookup"><span data-stu-id="0f753-115">Drag an [InkPicture](/previous-versions/aa514604(v=msdn.10)) control on a form, or double-click the InkPicture control in the Toolbox.</span></span>
2.  <span data-ttu-id="0f753-116">Nella finestra **Proprietà** selezionare la proprietà **immagine** , quindi fare clic sul pulsante con i puntini di sospensione per aprire la finestra di dialogo **Apri** .</span><span class="sxs-lookup"><span data-stu-id="0f753-116">In the **Properties** window, select the **Image** property, and then click the ellipsis button to open the **Open** dialog box.</span></span>
3.  <span data-ttu-id="0f753-117">Se si sta cercando un tipo di file specifico, ad esempio file con estensione jpg, selezionarlo nella casella **tipo file** .</span><span class="sxs-lookup"><span data-stu-id="0f753-117">If you are looking for a specific file type (for example, .jpg files), select it in the **Files of type** box.</span></span>
4.  <span data-ttu-id="0f753-118">Selezionare il file che si desidera visualizzare.</span><span class="sxs-lookup"><span data-stu-id="0f753-118">Select the file you want to display.</span></span>

<span data-ttu-id="0f753-119">Per cancellare l'immagine in fase di progettazione:</span><span class="sxs-lookup"><span data-stu-id="0f753-119">To clear the picture at design time:</span></span>

1.  <span data-ttu-id="0f753-120">Nella finestra **Proprietà** selezionare la proprietà **immagine** e fare clic con il pulsante destro del mouse sull'immagine di anteprima.</span><span class="sxs-lookup"><span data-stu-id="0f753-120">In the **Properties** window, select the **Image** property and right-click the thumbnail image.</span></span>
2.  <span data-ttu-id="0f753-121">Fare clic su **Reimposta**.</span><span class="sxs-lookup"><span data-stu-id="0f753-121">Click **Reset**.</span></span>

<span data-ttu-id="0f753-122">Il controllo [InkPicture](/previous-versions/aa514604(v=msdn.10)) viene visualizzato per impostazione predefinita senza bordi.</span><span class="sxs-lookup"><span data-stu-id="0f753-122">The [InkPicture](/previous-versions/aa514604(v=msdn.10)) control is displayed by default without any borders.</span></span> <span data-ttu-id="0f753-123">È possibile specificare un bordo standard o tridimensionale usando la proprietà [BorderStyle](/dotnet/api/system.windows.forms.picturebox.borderstyle?view=netcore-3.1) per distinguere la casella InkPicture dal resto del form, anche se non contiene alcuna immagine.</span><span class="sxs-lookup"><span data-stu-id="0f753-123">You can provide a standard or three-dimensional border using the [BorderStyle](/dotnet/api/system.windows.forms.picturebox.borderstyle?view=netcore-3.1) property to distinguish the InkPicture box from the rest of the form, even if it contains no image.</span></span>

<span data-ttu-id="0f753-124">È possibile visualizzare un'immagine in fase di esecuzione con il metodo [FromFile](/dotnet/api/system.drawing.image.fromfile?view=dotnet-plat-ext-3.1&preserve-view=true) dell'oggetto [System. Drawing. image](/dotnet/api/system.drawing.image?view=dotnet-plat-ext-3.1&preserve-view=true) :</span><span class="sxs-lookup"><span data-stu-id="0f753-124">You can display an image at run time with the [System.Drawing.Image](/dotnet/api/system.drawing.image?view=dotnet-plat-ext-3.1&preserve-view=true) object's [FromFile](/dotnet/api/system.drawing.image.fromfile?view=dotnet-plat-ext-3.1&preserve-view=true) method:</span></span>


```C++
ctlInkPicture.Image = Image.FromFile("c:\myImageFile")
```



<span data-ttu-id="0f753-125">È anche possibile includere un'immagine di sfondo con la proprietà [BackgroundImage](/dotnet/api/system.windows.forms.control.backgroundimage?view=netcore-3.1) dell'oggetto [Image](/dotnet/api/system.drawing.image?view=dotnet-plat-ext-3.1&preserve-view=true) ereditato. Tuttavia, l'immagine non può essere ridimensionata.</span><span class="sxs-lookup"><span data-stu-id="0f753-125">You can also include a background image with the inherited [Image](/dotnet/api/system.drawing.image?view=dotnet-plat-ext-3.1&preserve-view=true) object's [BackgroundImage](/dotnet/api/system.windows.forms.control.backgroundimage?view=netcore-3.1) property; however, that image cannot be resized.</span></span>

 

 

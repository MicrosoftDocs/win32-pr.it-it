---
description: Windows GDI+ fornisce la classe Metafile che consente di registrare e visualizzare i metafile.
ms.assetid: a9f9bac4-f3c7-44a1-9f0f-59ff1a27b077
title: Metafile (GDI+)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae75c2185670563f9a9e624d868da5b0e299cbec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343406"
---
# <a name="metafiles-gdi"></a><span data-ttu-id="dfdf8-103">Metafile (GDI+)</span><span class="sxs-lookup"><span data-stu-id="dfdf8-103">Metafiles (GDI+)</span></span>

<span data-ttu-id="dfdf8-104">Windows GDI+ fornisce la classe [**metafile**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) che consente di registrare e visualizzare i metafile.</span><span class="sxs-lookup"><span data-stu-id="dfdf8-104">Windows GDI+ provides the [**Metafile**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) class so that you can record and display metafiles.</span></span> <span data-ttu-id="dfdf8-105">Un metafile, detto anche immagine vettoriale, è un'immagine archiviata come sequenza di comandi e impostazioni di disegno.</span><span class="sxs-lookup"><span data-stu-id="dfdf8-105">A metafile, also called a vector image, is an image that is stored as a sequence of drawing commands and settings.</span></span> <span data-ttu-id="dfdf8-106">I comandi e le impostazioni registrati in un oggetto **metafile** possono essere archiviati in memoria o salvati in un file o in un flusso.</span><span class="sxs-lookup"><span data-stu-id="dfdf8-106">The commands and settings recorded in a **Metafile** object can be stored in memory or saved to a file or stream.</span></span>

<span data-ttu-id="dfdf8-107">GDI+ consente di visualizzare i metafile archiviati nei formati seguenti:</span><span class="sxs-lookup"><span data-stu-id="dfdf8-107">GDI+ can display metafiles that have been stored in the following formats:</span></span>

-   <span data-ttu-id="dfdf8-108">Windows Metafile Format (WMF)</span><span class="sxs-lookup"><span data-stu-id="dfdf8-108">Windows Metafile Format (WMF)</span></span>
-   <span data-ttu-id="dfdf8-109">Enhanced Metafile (EMF)</span><span class="sxs-lookup"><span data-stu-id="dfdf8-109">Enhanced Metafile (EMF)</span></span>
-   <span data-ttu-id="dfdf8-110">EMF +</span><span class="sxs-lookup"><span data-stu-id="dfdf8-110">EMF+</span></span>

<span data-ttu-id="dfdf8-111">GDI+ può registrare i metafile nei formati EMF e EMF +, ma non nel formato WMF.</span><span class="sxs-lookup"><span data-stu-id="dfdf8-111">GDI+ can record metafiles in the EMF and EMF+ formats, but not in the WMF format.</span></span>

<span data-ttu-id="dfdf8-112">EMF + è un'estensione di EMF che consente l'archiviazione di record GDI+.</span><span class="sxs-lookup"><span data-stu-id="dfdf8-112">EMF+ is an extension to EMF that allows GDI+ records to be stored.</span></span> <span data-ttu-id="dfdf8-113">Sono disponibili due varianti nel formato EMF +, ovvero EMF + Only e EMF + Dual.</span><span class="sxs-lookup"><span data-stu-id="dfdf8-113">There are two variations on the EMF+ format: EMF+ Only and EMF+ Dual.</span></span> <span data-ttu-id="dfdf8-114">EMF + solo i metafile contengono solo record GDI+.</span><span class="sxs-lookup"><span data-stu-id="dfdf8-114">EMF+ Only metafiles contain only GDI+ records.</span></span> <span data-ttu-id="dfdf8-115">Tali metafile possono essere visualizzati da GDI+ ma non da Windows Graphics Device Interface (GDI).</span><span class="sxs-lookup"><span data-stu-id="dfdf8-115">Such metafiles can be displayed by GDI+ but not by Windows Graphics Device Interface (GDI).</span></span> <span data-ttu-id="dfdf8-116">I metafile EMF + Dual contengono i record GDI+ e GDI.</span><span class="sxs-lookup"><span data-stu-id="dfdf8-116">EMF+ Dual metafiles contain GDI+ and GDI records.</span></span> <span data-ttu-id="dfdf8-117">Ogni record GDI+ in un metafile EMF + Dual è associato a un record GDI alternativo.</span><span class="sxs-lookup"><span data-stu-id="dfdf8-117">Each GDI+ record in an EMF+ Dual metafile is paired with an alternate GDI record.</span></span> <span data-ttu-id="dfdf8-118">Tali metafile possono essere visualizzati da GDI+ o da GDI.</span><span class="sxs-lookup"><span data-stu-id="dfdf8-118">Such metafiles can be displayed by GDI+ or by GDI.</span></span>

<span data-ttu-id="dfdf8-119">Nell'esempio seguente vengono registrate un'impostazione e un comando Drawing in un file su disco.</span><span class="sxs-lookup"><span data-stu-id="dfdf8-119">The following example records one setting and one drawing command in a disk file.</span></span> <span data-ttu-id="dfdf8-120">Si noti che nell'esempio viene creato un oggetto [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) e che il costruttore per l'oggetto **Graphics** riceve l'indirizzo di un oggetto [**metafile**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) come argomento.</span><span class="sxs-lookup"><span data-stu-id="dfdf8-120">Note that the example creates a [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object and that the constructor for the **Graphics** object receives the address of a [**Metafile**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) object as an argument.</span></span>


```
myMetafile = new Metafile(L"MyDiskFile.emf", hdc);
myGraphics = new Graphics(myMetafile);
   myPen = new Pen(Color(255, 0, 0, 200));
   myGraphics->SetSmoothingMode(SmoothingModeAntiAlias);
   myGraphics->DrawLine(myPen, 0, 0, 60, 40);
delete myGraphics;
delete myPen;
delete myMetafile;
```



<span data-ttu-id="dfdf8-121">Come illustrato nell'esempio precedente, la classe [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) è la chiave per la registrazione di istruzioni e impostazioni in un oggetto [**metafile**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) .</span><span class="sxs-lookup"><span data-stu-id="dfdf8-121">As the preceding example shows, the [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) class is the key to recording instructions and settings in a [**Metafile**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) object.</span></span> <span data-ttu-id="dfdf8-122">Qualsiasi chiamata eseguita a un metodo di un oggetto **Graphics** può essere registrata in un oggetto **metafile** .</span><span class="sxs-lookup"><span data-stu-id="dfdf8-122">Any call made to a method of a **Graphics** object can be recorded in a **Metafile** object.</span></span> <span data-ttu-id="dfdf8-123">Analogamente, è possibile impostare qualsiasi proprietà di un oggetto **Graphics** e registrare tale impostazione in un oggetto **metafile** .</span><span class="sxs-lookup"><span data-stu-id="dfdf8-123">Likewise, you can set any property of a **Graphics** object and record that setting in a **Metafile** object.</span></span> <span data-ttu-id="dfdf8-124">La registrazione termina quando l'oggetto **Graphics** viene eliminato o esce dall'ambito.</span><span class="sxs-lookup"><span data-stu-id="dfdf8-124">The recording ends when the **Graphics** object is deleted or goes out of scope.</span></span>

<span data-ttu-id="dfdf8-125">Nell'esempio seguente viene visualizzato il metafile creato nell'esempio precedente.</span><span class="sxs-lookup"><span data-stu-id="dfdf8-125">The following example displays the metafile created in the preceding example.</span></span> <span data-ttu-id="dfdf8-126">Il metafile viene visualizzato con l'angolo superiore sinistro in (100, 100).</span><span class="sxs-lookup"><span data-stu-id="dfdf8-126">The metafile is displayed with its upper-left corner at (100, 100).</span></span>


```
Graphics myGraphics(hdc);
Image myImage(L"MyDiskFile.emf");
myGraphics.DrawImage(&myImage, 100, 100);
```



<span data-ttu-id="dfdf8-127">Nell'esempio seguente vengono registrate diverse impostazioni delle proprietà (area di ritaglio, trasformazione globale e modalità di smussatura) in un oggetto [**metafile**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) .</span><span class="sxs-lookup"><span data-stu-id="dfdf8-127">The following example records several property settings (clipping region, world transformation, and smoothing mode) in a [**Metafile**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) object.</span></span> <span data-ttu-id="dfdf8-128">Il codice registra quindi diverse istruzioni di disegno.</span><span class="sxs-lookup"><span data-stu-id="dfdf8-128">Then the code records several drawing instructions.</span></span> <span data-ttu-id="dfdf8-129">Le istruzioni e le impostazioni vengono salvate in un file su disco.</span><span class="sxs-lookup"><span data-stu-id="dfdf8-129">The instructions and settings are saved in a disk file.</span></span>


```
myMetafile = new Metafile(L"MyDiskFile2.emf", hdc); 
myGraphics = new Graphics(myMetafile);
   myGraphics->SetSmoothingMode(SmoothingModeAntiAlias);
   myGraphics->RotateTransform(30);

   // Create an elliptical clipping region.
   GraphicsPath myPath;
   myPath.AddEllipse(0, 0, 200, 100);
   Region myRegion(&myPath);
   myGraphics->SetClip(&myRegion);

   Pen myPen(Color(255, 0, 0, 255));
   myGraphics->DrawPath(&myPen, &myPath);

   for(INT j = 0; j <= 300; j += 10)
   {
      myGraphics->DrawLine(&myPen, 0, 0, 300 - j, j);
   }
delete myGraphics;
delete myMetafile;
```



<span data-ttu-id="dfdf8-130">Nell'esempio seguente viene visualizzata l'immagine del metafile creata nell'esempio precedente.</span><span class="sxs-lookup"><span data-stu-id="dfdf8-130">The following example displays the metafile image created in the preceding example.</span></span>


```
myGraphics = new Graphics(hdc);
myMetafile = new Metafile(L"MyDiskFile.emf");
myGraphics->DrawImage(myMetafile, 10, 10);
```



<span data-ttu-id="dfdf8-131">Nella figura seguente viene illustrato l'output del codice precedente.</span><span class="sxs-lookup"><span data-stu-id="dfdf8-131">The following illustration shows the output of the preceding code.</span></span> <span data-ttu-id="dfdf8-132">Si noti l'anti-aliasing, l'area di ritaglio ellittica e la rotazione di 30 gradi.</span><span class="sxs-lookup"><span data-stu-id="dfdf8-132">Note the antialiasing, the elliptical clipping region, and the 30-degree rotation.</span></span>

![Screenshot di una finestra che contiene un'ellisse riempita con righe che hanno origine in un punto esterno all'ellisse](images/aboutgdip05-art00.png)

 

 




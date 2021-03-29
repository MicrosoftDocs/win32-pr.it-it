---
description: La classe Metafile, che eredita dalla classe Image, consente di registrare una sequenza di comandi di disegno.
ms.assetid: 062de6c2-9f82-415d-860e-2d1afd2ac027
title: Registrazione di metafile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 129b8fe810b1394921c60540488c93676341c562
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977559"
---
# <a name="recording-metafiles"></a><span data-ttu-id="6f9d7-103">Registrazione di metafile</span><span class="sxs-lookup"><span data-stu-id="6f9d7-103">Recording Metafiles</span></span>

<span data-ttu-id="6f9d7-104">La classe [**metafile**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) , che eredita dalla classe [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) , consente di registrare una sequenza di comandi di disegno.</span><span class="sxs-lookup"><span data-stu-id="6f9d7-104">The [**Metafile**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) class, which inherits from the [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) class, allows you to record a sequence of drawing commands.</span></span> <span data-ttu-id="6f9d7-105">I comandi registrati possono essere archiviati in memoria, salvati in un file o salvati in un flusso.</span><span class="sxs-lookup"><span data-stu-id="6f9d7-105">The recorded commands can be stored in memory, saved to a file, or saved to a stream.</span></span> <span data-ttu-id="6f9d7-106">I metafile possono contenere grafica vettoriale, immagini raster e testo.</span><span class="sxs-lookup"><span data-stu-id="6f9d7-106">Metafiles can contain vector graphics, raster images, and text.</span></span>

<span data-ttu-id="6f9d7-107">Nell'esempio seguente viene creato un oggetto [**metafile**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) .</span><span class="sxs-lookup"><span data-stu-id="6f9d7-107">The following example creates a [**Metafile**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) object.</span></span> <span data-ttu-id="6f9d7-108">Il codice usa l'oggetto **metafile** per registrare una sequenza di comandi grafici e quindi Salva i comandi registrati in un file denominato SampleMetafile. EMF.</span><span class="sxs-lookup"><span data-stu-id="6f9d7-108">The code uses the **Metafile** object to record a sequence of graphics commands and then saves the recorded commands in a file named SampleMetafile.emf.</span></span> <span data-ttu-id="6f9d7-109">Si noti che il costruttore di **metafile** riceve un handle del contesto di dispositivo e il costruttore di [**grafica**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) riceve l'indirizzo dell'oggetto **metafile** .</span><span class="sxs-lookup"><span data-stu-id="6f9d7-109">Note that the **Metafile** constructor receives a device context handle, and the [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) constructor receives the address of the **Metafile** object.</span></span> <span data-ttu-id="6f9d7-110">La registrazione viene arrestata (e i comandi registrati vengono salvati nel file) quando l'oggetto **Graphics** esce dall'ambito.</span><span class="sxs-lookup"><span data-stu-id="6f9d7-110">The recording stops (and the recorded commands are saved to the file) when the **Graphics** object goes out of scope.</span></span> <span data-ttu-id="6f9d7-111">Le ultime due righe di codice visualizzano il metafile creando un nuovo oggetto **Graphics** e passando l'indirizzo dell'oggetto **metafile** al metodo **DrawImage** di quell'oggetto **Graphics** .</span><span class="sxs-lookup"><span data-stu-id="6f9d7-111">The last two lines of code display the metafile by creating a new **Graphics** object and passing the address of the **Metafile** object to the **DrawImage** method of that **Graphics** object.</span></span> <span data-ttu-id="6f9d7-112">Si noti che il codice usa lo stesso oggetto **metafile** per registrare e visualizzare (riprodurre) il metafile.</span><span class="sxs-lookup"><span data-stu-id="6f9d7-112">Note that the code uses the same **Metafile** object to record and to display (play back) the metafile.</span></span>


```
Metafile metafile(L"SampleMetafile.emf", hdc); 
{
   Graphics graphics(&metafile);
   Pen greenPen(Color(255, 0, 255, 0));
   SolidBrush solidBrush(Color(255, 0, 0, 255));

   // Add a rectangle and an ellipse to the metafile.
   graphics.DrawRectangle(&greenPen, Rect(50, 10, 25, 75));
   graphics.DrawEllipse(&greenPen, Rect(100, 10, 25, 75));

   // Add an ellipse (drawn with antialiasing) to the metafile.
   graphics.SetSmoothingMode(SmoothingModeHighQuality);
   graphics.DrawEllipse(&greenPen, Rect(150, 10, 25, 75));

   // Add some text (drawn with antialiasing) to the metafile.
   FontFamily fontFamily(L"Arial");
   Font font(&fontFamily, 24, FontStyleRegular, UnitPixel);
   
   graphics.SetTextRenderingHint(TextRenderingHintAntiAlias);
   graphics.RotateTransform(30.0f);
   graphics.DrawString(L"Smooth Text", 11, &font, 
      PointF(50.0f, 50.0f), &solidBrush);
} // End of recording metafile.

// Play back the metafile.
Graphics playbackGraphics(hdc);
playbackGraphics.DrawImage(&metafile, 200, 100);
```



> [!Note]  
> <span data-ttu-id="6f9d7-113">Per registrare un metafile, è necessario costruire un oggetto [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) basato su un oggetto [**metafile**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) .</span><span class="sxs-lookup"><span data-stu-id="6f9d7-113">To record a metafile, you must construct a [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object based on a [**Metafile**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) object.</span></span> <span data-ttu-id="6f9d7-114">La registrazione del metafile termina quando l'oggetto **grafico** viene eliminato o esce dall'ambito.</span><span class="sxs-lookup"><span data-stu-id="6f9d7-114">The recording of the metafile ends when that **Graphics** object is deleted or goes out of scope.</span></span>

 

<span data-ttu-id="6f9d7-115">Un metafile contiene il proprio stato di grafica, definito dall'oggetto [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) usato per registrare il metafile.</span><span class="sxs-lookup"><span data-stu-id="6f9d7-115">A metafile contains its own graphics state, which is defined by the [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object used to record the metafile.</span></span> <span data-ttu-id="6f9d7-116">Tutte le proprietà dell'oggetto **Graphics** (area di ritaglio, trasformazione globale, modalità smussatura e like) impostate durante la registrazione del metafile verranno archiviate nel metafile.</span><span class="sxs-lookup"><span data-stu-id="6f9d7-116">Any properties of the **Graphics** object (clip region, world transformation, smoothing mode, and the like) that you set while recording the metafile will be stored in the metafile.</span></span> <span data-ttu-id="6f9d7-117">Quando si Visualizza il metafile, il disegno viene eseguito in base alle proprietà archiviate.</span><span class="sxs-lookup"><span data-stu-id="6f9d7-117">When you display the metafile, the drawing will be done according to those stored properties.</span></span>

<span data-ttu-id="6f9d7-118">Nell'esempio seguente, si supponga che la modalità di smussatura sia stata impostata su SmoothingModeNormal durante la registrazione del metafile.</span><span class="sxs-lookup"><span data-stu-id="6f9d7-118">In the following example, assume that the smoothing mode was set to SmoothingModeNormal during the recording of the metafile.</span></span> <span data-ttu-id="6f9d7-119">Anche se la modalità di smussatura dell'oggetto [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) usato per la riproduzione è impostata su SmoothingModeHighQuality, il metafile verrà riprodotto in base all'impostazione SmoothingModeNormal.</span><span class="sxs-lookup"><span data-stu-id="6f9d7-119">Even though the smoothing mode of the [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object used for playback is set to SmoothingModeHighQuality, the metafile will be played according to the SmoothingModeNormal setting.</span></span> <span data-ttu-id="6f9d7-120">Si tratta della modalità di smussamento impostata durante la registrazione, che è importante, non sulla modalità di smussamento impostata prima della riproduzione.</span><span class="sxs-lookup"><span data-stu-id="6f9d7-120">It is the smoothing mode set during the recording that is important, not the smoothing mode set prior to playback.</span></span>


```
graphics.SetSmoothingMode(SmoothingModeHighQuality);
graphics.DrawImage(&meta, 0, 0);
```



 

 




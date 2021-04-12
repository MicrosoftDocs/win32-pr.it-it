---
title: Windows Touch temporanei usando l'esempio Real-Time stilo (C#)
description: L'esempio Windows Touch temporanei (MTScratchpadRTStylus) Mostra come usare i messaggi Windows Touch per tracciare le tracce dei punti di tocco in una finestra.
ms.assetid: 8e80672f-0780-4dec-a9b4-afec0f7782ad
keywords:
- Windows Touch, esempi di codice
- Windows Touch, codice di esempio
- Windows Touch, esempi temporanei
- Esempi di temporanei
- Oggetto Windows Touch, stilo in tempo reale (RTS)
ms.topic: article
ms.date: 10/28/2019
ms.openlocfilehash: 4cf9ab2e451dcdcaaee808083ca42c420778f231
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "104336305"
---
# <a name="windows-touch-scratchpad-using-the-real-time-stylus-sample-c"></a><span data-ttu-id="141ac-108">Windows Touch temporanei usando l'esempio Real-Time stilo (C#)</span><span class="sxs-lookup"><span data-stu-id="141ac-108">Windows Touch Scratchpad using the Real-Time Stylus Sample (C#)</span></span>

<span data-ttu-id="141ac-109">L'esempio Windows Touch temporanei ([MTScratchpadRTStylus](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTScratchpadRTStylus/CS)) Mostra come usare i messaggi Windows Touch per tracciare le tracce dei punti di tocco in una finestra.</span><span class="sxs-lookup"><span data-stu-id="141ac-109">The Windows Touch Scratchpad sample ([MTScratchpadRTStylus](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTScratchpadRTStylus/CS)) shows how to use Windows Touch messages to draw traces of the touch points to a window.</span></span> <span data-ttu-id="141ac-110">La traccia del dito principale, quella che è stata inserita prima sul digitalizzatore, viene disegnata in nero.</span><span class="sxs-lookup"><span data-stu-id="141ac-110">The trace of the primary finger, the one that was put on the digitizer first, is drawn in black.</span></span> <span data-ttu-id="141ac-111">Le dita secondarie sono disegnate in sei colori: rosso, verde, blu, ciano, magenta e giallo.</span><span class="sxs-lookup"><span data-stu-id="141ac-111">Secondary fingers are drawn in six other colors: red, green, blue, cyan, magenta and yellow.</span></span> <span data-ttu-id="141ac-112">Lo screenshot seguente mostra l'aspetto dell'applicazione durante l'esecuzione.</span><span class="sxs-lookup"><span data-stu-id="141ac-112">The following screen shot shows how the application could look while running.</span></span>

![screenshot che mostra l'esempio Windows Touch temporanei usando lo stilo in tempo reale in c Sharp, con controllo ortografia durante nero e rosso sullo schermo](images/mtscratchpadrtstyluscs.png)

<span data-ttu-id="141ac-114">Per questo esempio viene creato l'oggetto Real-Time stilo (RTS) e il supporto per più punti di contatto è abilitato.</span><span class="sxs-lookup"><span data-stu-id="141ac-114">For this sample, the Real-Time Stylus (RTS) object is created and support for multiple contact points is enabled.</span></span> <span data-ttu-id="141ac-115">Un plug-in di DynamicRenderer viene aggiunto al RTS per eseguire il rendering del contenuto.</span><span class="sxs-lookup"><span data-stu-id="141ac-115">A DynamicRenderer plug-in is added to the RTS to render content.</span></span> <span data-ttu-id="141ac-116">Un plug-in, EventHandlerPlugIn, viene implementato per tenere traccia del numero di dita e per modificare il colore che il renderer dinamico sta disegnando.</span><span class="sxs-lookup"><span data-stu-id="141ac-116">A plug-in, EventHandlerPlugIn, is implemented to track down the number of fingers and to change the color that the dynamic renderer is drawing.</span></span> <span data-ttu-id="141ac-117">Con entrambi i plug-in nello stack di plug-in RTS, l'applicazione Windows Touch temporanei eseguirà il rendering del contatto principale in nero e il resto dei contatti nei vari colori.</span><span class="sxs-lookup"><span data-stu-id="141ac-117">With both plug-ins in the RTS plug-in stack, the Windows Touch Scratchpad application will render the primary contact in black and the rest of the contacts in the various colors.</span></span>

<span data-ttu-id="141ac-118">Nel codice seguente viene illustrato il modo in cui EventHandlerPlugIn incrementa e decrementa un conteggio del numero di contatti e imposta il colore del renderer dinamico.</span><span class="sxs-lookup"><span data-stu-id="141ac-118">The following code shows how the EventHandlerPlugIn increments and decrements a count of the number of contacts and sets the color of the dynamic renderer.</span></span>

```CSharp
        public void StylusDown(RealTimeStylus sender, StylusDownData data)
        {
            // Set new stroke color to the DrawingAttributes of the DynamicRenderer
            // If there are no fingers down, this is a primary contact
            dynamicRenderer.DrawingAttributes.Color = touchColor.GetColor(cntContacts == 0);

            ++cntContacts;  // Increment finger-down counter
        }

        public void StylusUp(RealTimeStylus sender, StylusUpData data)
        {
            --cntContacts;  // Decrement finger-down counter
        }
```

<span data-ttu-id="141ac-119">Il codice seguente illustra il modo in cui viene creato RTS con il supporto di più punti di contatto.</span><span class="sxs-lookup"><span data-stu-id="141ac-119">The following code shows how the RTS is created with multiple contact point support.</span></span>

```CSharp
        private void OnLoadHandler(Object sender, EventArgs e)
        {
            // Create RealTimeStylus object and enable it for multi-touch
            realTimeStylus = new RealTimeStylus(this);
            realTimeStylus.MultiTouchEnabled = true;

            // Create DynamicRenderer and event handler, and add them to the RTS object as synchronous plugins
            dynamicRenderer = new DynamicRenderer(this);
            eventHandler = new EventHandlerPlugIn(this.CreateGraphics(), dynamicRenderer);
            realTimeStylus.SyncPluginCollection.Add(eventHandler);
            realTimeStylus.SyncPluginCollection.Add(dynamicRenderer);

            // Enable RTS and DynamicRenderer object, and enable auto-redraw of the DynamicRenderer
            realTimeStylus.Enabled = true;
            dynamicRenderer.Enabled = true;
            dynamicRenderer.EnableDataCache = true;
        }
```

<span data-ttu-id="141ac-120">Dopo che il colore dell'oggetto DynamicRenderer è stato modificato e sono stati disegnati i tratti, una chiamata a DynamicRenderer:: Refresh provocherà la visualizzazione dei nuovi tratti.</span><span class="sxs-lookup"><span data-stu-id="141ac-120">After the DynamicRenderer object's color has changed and strokes have been drawn, a call to DynamicRenderer::Refresh will cause the new strokes to appear.</span></span> <span data-ttu-id="141ac-121">Nel codice seguente viene illustrato come eseguire questa operazione nel metodo OnPaintHandler.</span><span class="sxs-lookup"><span data-stu-id="141ac-121">The following code shows how this is performed in the OnPaintHandler method.</span></span>

```CSharp
        private void OnPaintHandler(object sender, PaintEventArgs e)
        {
            // Erase the background
            Brush brush = new SolidBrush(SystemColors.Window);
            e.Graphics.FillRectangle(brush, ClientRectangle);

            // Ask DynamicRenderer to redraw itself
            dynamicRenderer.Refresh();
        }
```

## <a name="related-topics"></a><span data-ttu-id="141ac-122">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="141ac-122">Related topics</span></span>

<span data-ttu-id="141ac-123">[Applicazione temporanei multitocco (RTS/C#)](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTScratchpadRTStylus/CS), [applicazione temporanei multitocco (RTS/C++)](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTScratchpadRTStylus/cpp), esempi di [Windows Touch](windows-touch-samples.md)</span><span class="sxs-lookup"><span data-stu-id="141ac-123">[Multi-touch Scratchpad Application (RTS/C#)](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTScratchpadRTStylus/CS), [Multi-touch Scratchpad Application (RTS/C++)](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTScratchpadRTStylus/cpp), [Windows Touch Samples](windows-touch-samples.md)</span></span>

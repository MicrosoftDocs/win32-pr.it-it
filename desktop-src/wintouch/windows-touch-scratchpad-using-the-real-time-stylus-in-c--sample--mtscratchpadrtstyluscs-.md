---
title: Windows Touch Scratchpad usando l'esempio Real-Time stilo (C#)
description: Esaminare un esempio Windows Touch Scratchpad C# (MTScratchpadRTStylus), che illustra come usare i messaggi Windows Touch per disegnare tracce dei punti di tocco in una finestra.
ms.assetid: 8e80672f-0780-4dec-a9b4-afec0f7782ad
keywords:
- Windows Touch,esempi di codice
- Windows Touch,codice di esempio
- Windows Touch,Esempi di Scratchpad
- Esempi di Scratchpad
- Windows Touch,Oggetto Stilo in tempo reale (RTS)
ms.topic: article
ms.date: 10/28/2019
ms.openlocfilehash: 3c30d3543024a48394ddd7b9b2b06a05b61f5025
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406314"
---
# <a name="windows-touch-scratchpad-using-the-real-time-stylus-sample-c"></a><span data-ttu-id="af846-108">Windows Touch Scratchpad usando l'esempio Real-Time stilo (C#)</span><span class="sxs-lookup"><span data-stu-id="af846-108">Windows Touch Scratchpad using the Real-Time Stylus Sample (C#)</span></span>

<span data-ttu-id="af846-109">L Windows Touch di esempio scratchpad ([MTScratchpadRTStylus](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTScratchpadRTStylus/CS)) illustra come usare i messaggi Windows Touch per disegnare tracce dei punti di tocco in una finestra.</span><span class="sxs-lookup"><span data-stu-id="af846-109">The Windows Touch Scratchpad sample ([MTScratchpadRTStylus](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTScratchpadRTStylus/CS)) shows how to use Windows Touch messages to draw traces of the touch points to a window.</span></span> <span data-ttu-id="af846-110">La traccia del dito primario, quella che è stata inserita per prima nel digitalizzatore, viene disegnata in nero.</span><span class="sxs-lookup"><span data-stu-id="af846-110">The trace of the primary finger, the one that was put on the digitizer first, is drawn in black.</span></span> <span data-ttu-id="af846-111">Le dita secondarie vengono disegnate in altri sei colori: rosso, verde, blu, ciano, magenta e giallo.</span><span class="sxs-lookup"><span data-stu-id="af846-111">Secondary fingers are drawn in six other colors: red, green, blue, cyan, magenta and yellow.</span></span> <span data-ttu-id="af846-112">La schermata seguente mostra l'aspetto dell'applicazione durante l'esecuzione.</span><span class="sxs-lookup"><span data-stu-id="af846-112">The following screen shot shows how the application could look while running.</span></span>

![Screenshot che mostra l'esempio di touch scratchpad di Windows con lo stilo in tempo reale in c sharp, con linee a righe rosse e nere sullo schermo](images/mtscratchpadrtstyluscs.png)

<span data-ttu-id="af846-114">Per questo esempio viene creato l'Real-Time Stylus (RTS) e viene abilitato il supporto per più punti di contatto.</span><span class="sxs-lookup"><span data-stu-id="af846-114">For this sample, the Real-Time Stylus (RTS) object is created and support for multiple contact points is enabled.</span></span> <span data-ttu-id="af846-115">Un plug-in DynamicRenderer viene aggiunto a RTS per eseguire il rendering del contenuto.</span><span class="sxs-lookup"><span data-stu-id="af846-115">A DynamicRenderer plug-in is added to the RTS to render content.</span></span> <span data-ttu-id="af846-116">Un plug-in, EventHandlerPlugIn, viene implementato per tenere traccia del numero di dita e per modificare il colore che il renderer dinamico sta disegnando.</span><span class="sxs-lookup"><span data-stu-id="af846-116">A plug-in, EventHandlerPlugIn, is implemented to track down the number of fingers and to change the color that the dynamic renderer is drawing.</span></span> <span data-ttu-id="af846-117">Con entrambi i plug-in nello stack di plug-in RTS, l'applicazione Windows Touch Scratchpad eseguirà il rendering del contatto primario in nero e del resto dei contatti nei vari colori.</span><span class="sxs-lookup"><span data-stu-id="af846-117">With both plug-ins in the RTS plug-in stack, the Windows Touch Scratchpad application will render the primary contact in black and the rest of the contacts in the various colors.</span></span>

<span data-ttu-id="af846-118">Il codice seguente illustra come EventHandlerPlugIn incrementa e decrementa un conteggio del numero di contatti e imposta il colore del renderer dinamico.</span><span class="sxs-lookup"><span data-stu-id="af846-118">The following code shows how the EventHandlerPlugIn increments and decrements a count of the number of contacts and sets the color of the dynamic renderer.</span></span>

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

<span data-ttu-id="af846-119">Il codice seguente illustra come viene creato rts con più punti di contatto di supporto.</span><span class="sxs-lookup"><span data-stu-id="af846-119">The following code shows how the RTS is created with multiple contact point support.</span></span>

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

<span data-ttu-id="af846-120">Dopo che il colore dell'oggetto DynamicRenderer è stato modificato e i tratti sono stati disegnati, una chiamata a DynamicRenderer::Refresh causerà la visualizzazione dei nuovi tratti.</span><span class="sxs-lookup"><span data-stu-id="af846-120">After the DynamicRenderer object's color has changed and strokes have been drawn, a call to DynamicRenderer::Refresh will cause the new strokes to appear.</span></span> <span data-ttu-id="af846-121">Il codice seguente illustra come eseguire questa operazione nel metodo OnPaintHandler.</span><span class="sxs-lookup"><span data-stu-id="af846-121">The following code shows how this is performed in the OnPaintHandler method.</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="af846-122">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="af846-122">Related topics</span></span>

<span data-ttu-id="af846-123">[Multi-touch Scratchpad Application (RTS/C#)](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTScratchpadRTStylus/CS), [Multi-touch Scratchpad Application (RTS/C++)](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTScratchpadRTStylus/cpp), [Windows Touch Samples](windows-touch-samples.md)</span><span class="sxs-lookup"><span data-stu-id="af846-123">[Multi-touch Scratchpad Application (RTS/C#)](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTScratchpadRTStylus/CS), [Multi-touch Scratchpad Application (RTS/C++)](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTScratchpadRTStylus/cpp), [Windows Touch Samples](windows-touch-samples.md)</span></span>

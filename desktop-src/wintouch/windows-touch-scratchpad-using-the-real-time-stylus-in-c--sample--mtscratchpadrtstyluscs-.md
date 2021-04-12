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
# <a name="windows-touch-scratchpad-using-the-real-time-stylus-sample-c"></a>Windows Touch temporanei usando l'esempio Real-Time stilo (C#)

L'esempio Windows Touch temporanei ([MTScratchpadRTStylus](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTScratchpadRTStylus/CS)) Mostra come usare i messaggi Windows Touch per tracciare le tracce dei punti di tocco in una finestra. La traccia del dito principale, quella che è stata inserita prima sul digitalizzatore, viene disegnata in nero. Le dita secondarie sono disegnate in sei colori: rosso, verde, blu, ciano, magenta e giallo. Lo screenshot seguente mostra l'aspetto dell'applicazione durante l'esecuzione.

![screenshot che mostra l'esempio Windows Touch temporanei usando lo stilo in tempo reale in c Sharp, con controllo ortografia durante nero e rosso sullo schermo](images/mtscratchpadrtstyluscs.png)

Per questo esempio viene creato l'oggetto Real-Time stilo (RTS) e il supporto per più punti di contatto è abilitato. Un plug-in di DynamicRenderer viene aggiunto al RTS per eseguire il rendering del contenuto. Un plug-in, EventHandlerPlugIn, viene implementato per tenere traccia del numero di dita e per modificare il colore che il renderer dinamico sta disegnando. Con entrambi i plug-in nello stack di plug-in RTS, l'applicazione Windows Touch temporanei eseguirà il rendering del contatto principale in nero e il resto dei contatti nei vari colori.

Nel codice seguente viene illustrato il modo in cui EventHandlerPlugIn incrementa e decrementa un conteggio del numero di contatti e imposta il colore del renderer dinamico.

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

Il codice seguente illustra il modo in cui viene creato RTS con il supporto di più punti di contatto.

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

Dopo che il colore dell'oggetto DynamicRenderer è stato modificato e sono stati disegnati i tratti, una chiamata a DynamicRenderer:: Refresh provocherà la visualizzazione dei nuovi tratti. Nel codice seguente viene illustrato come eseguire questa operazione nel metodo OnPaintHandler.

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

## <a name="related-topics"></a>Argomenti correlati

[Applicazione temporanei multitocco (RTS/C#)](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTScratchpadRTStylus/CS), [applicazione temporanei multitocco (RTS/C++)](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTScratchpadRTStylus/cpp), esempi di [Windows Touch](windows-touch-samples.md)

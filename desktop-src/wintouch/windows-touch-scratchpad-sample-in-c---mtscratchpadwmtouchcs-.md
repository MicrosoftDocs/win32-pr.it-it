---
title: Windows Esempio di Touch Scratchpad in C (MTSocchpadWMTouchCS)
description: L'Windows Touch Scratchpad in C# illustra come usare i messaggi Windows Touch per disegnare tracce dei punti di tocco in una finestra.
ms.assetid: 652124be-01a8-4df4-b590-e5c2ca3f012c
keywords:
- Windows Tocco, esempi di codice
- Windows Tocco, codice di esempio
- Windows Esempi di Touch,Scratchpad
- Esempi di Scratchpad
ms.topic: article
ms.date: 10/28/2019
ms.openlocfilehash: 112f8446af4b845bfd36e4262a11da807535c93baaf6257a10a9a8d2b03374e9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120089847"
---
# <a name="windows-touch-scratchpad-sample-c"></a>Windows Esempio di Touch Scratchpad (C#)

[L'Windows touch scratchpad in C#](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTScratchpadWMTouch/CS) illustra come usare i messaggi Windows Touch per disegnare tracce dei punti di tocco in una finestra. La traccia del dito principale, quella che è stata inserita per prima sul digitalizzatore, viene disegnata in nero. Le dita secondarie vengono disegnate in altri sei colori: rosso, verde, blu, ciano, magenta e giallo. L'immagine seguente mostra l'aspetto dell'applicazione durante l'esecuzione.

![Screenshot che mostra l'esempio di scratchpad tocco di Windows in c sharp, con linee a linee a righe nere, verdi, blu e rosse sullo schermo](images/mtscratchpadwmtouchcs.png)

Per questo esempio, viene creato un form toccabile per gestire i [**WM_TOUCH**](wm-touchdown.md) messaggi. Questo modulo viene ereditato per abilitare Windows Touch nell'applicazione scratchpad. Quando i **WM_TOUCH** vengono visualizzati nel form, vengono interpretati in punti e aggiunti alla raccolta di tratti. Il rendering della raccolta strokes viene eseguito nell'oggetto Graphics. Nel codice seguente viene illustrato come il form  toccabile si registra per la gestione WM_TOUCH messaggi e come gestisce i **WM_TOUCH** personalizzati.

```CSharp
        private void OnLoadHandler(Object sender, EventArgs e)
        {
            try
            {
                // Registering the window for multi-touch, using the default settings.
                // p/invoking into user32.dll
                if (!RegisterTouchWindow(this.Handle, 0))
                {
                    Debug.Print("ERROR: Could not register window for multi-touch");
                }
            }
            catch (Exception exception)
            {
                Debug.Print("ERROR: RegisterTouchWindow API not available");
                Debug.Print(exception.ToString());
                MessageBox.Show("RegisterTouchWindow API not available", "MTScratchpadWMTouch ERROR",
                    MessageBoxButtons.OK, MessageBoxIcon.Error, MessageBoxDefaultButton.Button1, 0);
            }
        }
(...)
        [PermissionSet(SecurityAction.Demand, Name = "FullTrust")]
        protected override void WndProc(ref Message m)
        {
            // Decode and handle WM_TOUCH message.
            bool handled;
            switch (m.Msg)
            {
                case WM_TOUCH:
                    handled = DecodeTouch(ref m);
                    break;
                default:
                    handled = false;
                    break;
            }

            // Call parent WndProc for default message processing.
            base.WndProc(ref m);

            if (handled)
            {
                // Acknowledge event if handled.
                m.Result = new System.IntPtr(1);
            }
        }
```

Il codice seguente illustra come viene interpretato il Windows Touch e i dati vengono aggiunti alle raccolte di tratti.

```CSharp
        private bool DecodeTouch(ref Message m)
        {
            // More than one touchinput may be associated with a touch message,
            // so an array is needed to get all event information.
            int inputCount = LoWord(m.WParam.ToInt32()); // Number of touch inputs, actual per-contact messages

            TOUCHINPUT[] inputs; // Array of TOUCHINPUT structures
            inputs = new TOUCHINPUT[inputCount]; // Allocate the storage for the parameters of the per-contact messages

            // Unpack message parameters into the array of TOUCHINPUT structures, each
            // representing a message for one single contact.
            if (!GetTouchInputInfo(m.LParam, inputCount, inputs, touchInputSize))
            {
                // Get touch info failed.
                return false;
            }

            // For each contact, dispatch the message to the appropriate message
            // handler.
            bool handled = false; // Boolean, is message handled
            for (int i = 0; i < inputCount; i++)
            {
                TOUCHINPUT ti = inputs[i];

                // Assign a handler to this message.
                EventHandler<WMTouchEventArgs> handler = null;     // Touch event handler
                if ((ti.dwFlags & TOUCHEVENTF_DOWN) != 0)
                {
                    handler = Touchdown;
                }
                else if ((ti.dwFlags & TOUCHEVENTF_UP) != 0)
                {
                    handler = Touchup;
                }
                else if ((ti.dwFlags & TOUCHEVENTF_MOVE) != 0)
                {
                    handler = TouchMove;
                }

                // Convert message parameters into touch event arguments and handle the event.
                if (handler != null)
                {
                    // Convert the raw touchinput message into a touchevent.
                    WMTouchEventArgs te = new WMTouchEventArgs(); // Touch event arguments

                    // TOUCHINFO point coordinates and contact size is in 1/100 of a pixel; convert it to pixels.
                    // Also convert screen to client coordinates.
                    te.ContactY = ti.cyContact/100;
                    te.ContactX = ti.cxContact/100;
                    te.Id = ti.dwID;
                    {
                        Point pt = PointToClient(new Point(ti.x/100, ti.y/100));
                        te.LocationX = pt.X;
                        te.LocationY = pt.Y;
                    }
                    te.Time = ti.dwTime;
                    te.Mask = ti.dwMask;
                    te.Flags = ti.dwFlags;

                    // Invoke the event handler.
                    handler(this, te);

                    // Mark this event as handled.
                    handled = true;
                }
            }

            CloseTouchInputHandle(m.LParam);

            return handled;
        }
    }
```

Il codice seguente illustra come viene visualizzata una raccolta di tratti.

```CSharp
        public void Draw(Graphics graphics)
        {
            if ((points.Count < 2) || (graphics == null))
            {
                return;
            }

            Pen pen = new Pen(color, penWidth);
            graphics.DrawLines(pen, (Point[]) points.ToArray(typeof(Point)));
        }
```

Il codice seguente mostra come i singoli oggetti stroke vengono visualizzati con un oggetto Graphics.

```CSharp
        public void Draw(Graphics graphics)
        {
            if(points.Count < 2 || graphics == null)
            {
                return;
            }

            Pen pen = new Pen(color, penWidth);
            graphics.DrawLines(pen, (Point[]) points.ToArray(typeof(Point)));
        }
```

## <a name="related-topics"></a>Argomenti correlati

[Windows Touch Scratchpad (C++)](windows-touch-scratchpad-sample--mtscratchpadwmtouch-.md), [Multi-Touch Scratchpad Application (WM_TOUCH/C#)](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTScratchpadWMTouch/CS), [Multi-Touch Scratchpad Application (WM_TOUCH/C++)](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTScratchpadWMTouch/cpp), [Windows Touch Samples](windows-touch-samples.md)


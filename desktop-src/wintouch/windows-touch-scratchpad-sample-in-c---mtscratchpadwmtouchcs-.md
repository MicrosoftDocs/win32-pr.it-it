---
title: Esempio di Windows Touch temporanei in C (MTScratchpadWMTouchCS)
description: L'esempio Windows Touch temporanei in C# Mostra come usare i messaggi tocco di Windows per tracciare i punti di tocco in una finestra.
ms.assetid: 652124be-01a8-4df4-b590-e5c2ca3f012c
keywords:
- Windows Touch, esempi di codice
- Windows Touch, codice di esempio
- Windows Touch, esempi temporanei
- Esempi di temporanei
ms.topic: article
ms.date: 10/28/2019
ms.openlocfilehash: 2d91c08c55f0d5b29a170a3a01c6ee882fad765f
ms.sourcegitcommit: c7fa8fc137714433c8d18b1bf71e9cf0b5bf5e80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/25/2020
ms.locfileid: "104047479"
---
# <a name="windows-touch-scratchpad-sample-c"></a>Esempio di Windows Touch temporanei (C#)

L' [esempio Windows Touch temporanei in C#](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTScratchpadWMTouch/CS) Mostra come usare i messaggi tocco di Windows per tracciare i punti di tocco in una finestra. La traccia del dito principale, quella che è stata inserita prima sul digitalizzatore, viene disegnata in nero. Le dita secondarie sono disegnate in sei colori: rosso, verde, blu, ciano, magenta e giallo. Nell'immagine seguente viene illustrato l'aspetto dell'applicazione durante l'esecuzione.

![screenshot che mostra l'esempio Windows Touch temporanei in c Sharp, con la controllo ortografia durante nera, verde, blu e rossa sullo schermo](images/mtscratchpadwmtouchcs.png)

Per questo esempio viene creato un form toccabile per gestire i messaggi di [**WM_TOUCH**](wm-touchdown.md) . Questo modulo viene ereditato per abilitare Windows Touch nell'applicazione temporanei. Quando i messaggi di **WM_TOUCH** arrivano al modulo, vengono interpretati in punti e vengono aggiunti alla raccolta di tratti. Viene eseguito il rendering della raccolta Strokes nell'oggetto Graphics. Nel codice seguente viene illustrato il modo in cui il form toccabile si registra per la gestione dei messaggi **WM_TOUCH** e il modo in cui gestisce i messaggi di **WM_TOUCH** .

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

Il codice seguente illustra come viene interpretato il messaggio Windows Touch e i dati vengono aggiunti alle raccolte Stroke.

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

Il codice seguente illustra il modo in cui i singoli oggetti Stroke vengono visualizzati con un oggetto Graphics.

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

[Windows Touch temporanei Sample (C++)](windows-touch-scratchpad-sample--mtscratchpadwmtouch-.md), [applicazione temporanei multitocco (WM_TOUCH/c #)](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTScratchpadWMTouch/CS), [applicazione temporanei multitocco (WM_TOUCH/C + +)](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTScratchpadWMTouch/cpp), esempi di [Windows Touch](windows-touch-samples.md)


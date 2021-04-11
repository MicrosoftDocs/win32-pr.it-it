---
description: In questo esempio viene illustrato come utilizzare l'analisi dell'input penna per creare un'applicazione di riempimento del modulo, in cui il modulo è basato su un modulo cartaceo digitalizzato.
ms.assetid: 1eae5962-b4e0-4947-a6d2-63713a68198c
title: Modulo cartaceo analizzato analisi input penna
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e94d366c77e19bd5c32d3d1e4efa286cb3b089ae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104225917"
---
# <a name="ink-analysis-scanned-paper-form"></a>Modulo cartaceo analizzato analisi input penna

In questo esempio viene illustrato come utilizzare l'analisi dell'input penna per creare un'applicazione di riempimento del modulo, in cui il modulo è basato su un modulo cartaceo digitalizzato.

## <a name="features-demonstrated"></a>Funzionalità illustrate

Questa applicazione di esempio illustra le seguenti funzionalità dell'API di analisi dell'input penna e dei controlli Windows Form input penna:

-   Caricamento di un modulo cartaceo scansionato. L'esempio importa il form da un'immagine in formato png.
-   Raccolta e rendering dell'input penna sopra il modulo sottoposti a scansione.
-   Uso di un oggetto [InkAnalyzer](/previous-versions/ms583671(v=vs.100)) per analizzare la grafia.
-   Generazione di oggetti [AnalysisHintNode](/previous-versions/ms573018(v=vs.100)) per migliorare i risultati della grafia.
-   Popolamento di caselle di testo da hint di analisi.
-   Creazione di un'esperienza di correzione del testo di base.

## <a name="project-references"></a>Riferimenti al progetto

L'esempio è disponibile come applicazione Windows Form o Windows Presentation Foundation. Riferimenti alla versione Windows Form:

-   Microsoft.Ink.dll
-   Microsoft.Ink.Analysis.dll

La versione Windows Presentation Foundation fa riferimento IAWinFX.dll oltre alle DLL core Windows Presentation Foundation.

> [!Note]  
> Per la versione Windows Presentation Foundation di questo esempio, disponibile nella directory XAML, è necessario che nel sistema siano installate le estensioni Windows Presentation Foundation per Microsoft Visual Studio 2005.

 

## <a name="user-interface"></a>Interfaccia utente

L'interfaccia utente per questa applicazione è costituita da un oggetto [TabControl](/dotnet/api/system.windows.forms.tabcontrol?view=netcore-3.1) con due oggetti [TabPage](/dotnet/api/system.windows.forms.tabpage?view=netcore-3.1) associati: form input penna e formato testo convertito. La scheda modulo input penna contiene

-   Pannello che contiene un'immagine di un modulo cartaceo digitalizzato utilizzato per l'esecuzione di messaggi telefonici.
-   Una casella di controllo con l'applicazione Mostra i limiti dell'hint di analisi quando è selezionata.
-   Una coppia di pulsanti, Clear e Analyze, che cancellano l'input penna dal form e inizializzano l'analisi dell'input penna.

Il formato di testo convertito contiene la stessa immagine e è la pagina in cui l'applicazione Visualizza il testo riconosciuto. Quando si fa clic su analizza, l'applicazione esegue l'analisi dell'input penna in modo sincrono e i risultati del riconoscimento vengono visualizzati nella scheda formato testo convertito.

## <a name="functionality"></a>Funzionalità

Questa applicazione usa un oggetto [InkOverlay](/previous-versions/ms552322(v=vs.100)) per abilitare la scrittura. L'oggetto InkOverlay è particolarmente adatto per l'acquisizione di note e per la creazione di un scarabocchio di base. L'utilizzo previsto principale di questo oggetto consiste nel visualizzare input penna come input penna. La classe principale per l'analisi dell'input penna è la classe [InkAnalyzer](/previous-versions/ms583671(v=vs.100)) . Quando si chiama il metodo [Analyze](/previous-versions/ms568971(v=vs.100)) dell'oggetto InkAnalyzer, l'analisi dell'input penna viene eseguita in modo sincrono.

L'applicazione Inizializza due matrici, una delle stringhe e uno dei rettangoli. La matrice di stringhe, `factoidStrings` , è costituita da oggetti del controllo del controllo che vengono passati in [InkAnalyzer](/previous-versions/ms583671(v=vs.100)) come oggetti [AnalysisHintNode](/previous-versions/ms573018(v=vs.100)) . [](/previous-versions/ms583657(v=vs.100)) Gli oggetti AnalysisHintNode polarizzano l'oggetto InkAnalyzer verso un input specifico. In questo esempio vengono utilizzati gli hint per la data, l'ora e il telefono, nonché altri.

Ogni elemento [AnalysisHintNode](/previous-versions/ms573018(v=vs.100)) è associato a un'area specifica del modulo. Le aree sono rappresentate dalla matrice di rettangoli, `rects` . Creando una [casella](/dotnet/api/system.windows.forms.textbox?view=netcore-3.1) di testo per ogni rettangolo, l'esempio restituisce il testo riconosciuto nella posizione corretta.


```C++
        private void InitHints()
        {
            // Instantiate the collection of TextBoxes.
            this.textBoxes = new ArrayList();

            // For each Rectangle in Rectangles
            for (int i = 0; i < rects.Length; i++)
            {

                Rectangle rectangle = rects[i];

                // Create an AnalysisHintNode with the bounds of the Rectangle.  The bounds
                // of an AnalysisHintNode gives clues to the handwriting recognizer about
                // the way Strokes are grouped together.
                AnalysisHintNode hint = this.analyzer.CreateAnalysisHint(rectangle);

                // Set the corresponding Factoid on the AnalysisHintNode.  This gives the 
                // recognizer clues about the meaning of the strokes within the 
                // AnalysisHintNode's region.
                hint.Factoid = factoidStrings[i];

                // Create a corresponding TextBox where the results of the analysis
                // associated with this AnalysisHintNode will be displayed.  Store the reference
                // to the TextBox in the textBoxes Collection.
                this.textBoxes.Add(InitTextBox(hint));
            }
        }
```



Successivamente, è sufficiente creare un gestore eventi che attiva l'analisi dell'input penna quando l'utente fa clic su analizza.


```C++
        private void UpdateTextBoxes()
        {
            // Get the AnalysisHintNodes that we previously added to the InkAnalyzer.
            ContextNodeCollection hints = this.analyzer.GetAnalysisHints();

            for (int i = 0; i < hints.Count; i++)
            {
                // Get the recognized string from the AnalysisHintNode
                string analyzedString = ((AnalysisHintNode)hints[i]).GetRecognizedString();

                // If we found a string, set the contents of the TextBox
                // to that string.
                if (analyzedString != null)
                {
                    ((TextBox)this.textBoxes[i]).Text = analyzedString;
                }
            }
        }
```



 

 

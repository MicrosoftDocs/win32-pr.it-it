---
description: Questo esempio illustra come usare Analisi input penna per creare un'applicazione per la compilazione di moduli, in cui il modulo è basato su un modulo cartaceo digitalizzato.
ms.assetid: 1eae5962-b4e0-4947-a6d2-63713a68198c
title: Modulo della carta digitalizzata di Analisi input penna
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4069efd5ba8763e00e9b3170ffb0a39a4a70c4d66d07d3c8bf08bc3688f57ed0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118718647"
---
# <a name="ink-analysis-scanned-paper-form"></a>Modulo della carta digitalizzata di Analisi input penna

Questo esempio illustra come usare Analisi input penna per creare un'applicazione per la compilazione di moduli, in cui il modulo è basato su un modulo cartaceo digitalizzato.

## <a name="features-demonstrated"></a>Funzionalità illustrate

Questa applicazione di esempio illustra le funzionalità seguenti dell'API Analisi input penna e dei controlli input Windows Form:

-   Caricamento di un modulo cartaceo digitalizzato. L'esempio importa il form da un'immagine in .png formato.
-   Raccolta e rendering dell'input penna sopra il modulo digitalizzato.
-   Uso di [un oggetto InkAnalyzer](/previous-versions/ms583671(v=vs.100)) per analizzare la grafia.
-   Generazione di [oggetti AnalysisHintNode](/previous-versions/ms573018(v=vs.100)) per migliorare i risultati della grafia.
-   Popolamento delle caselle di testo dai suggerimenti di analisi.
-   Creazione di un'esperienza di correzione del testo di base.

## <a name="project-references"></a>Riferimenti al progetto

L'esempio è disponibile come Windows Form o Windows Presentation Foundation applicazione. I riferimenti Windows versioni di Forms seguenti:

-   Microsoft.Ink.dll
-   Microsoft.Ink.Analysis.dll

Oltre alle Windows Presentation Foundation di IAWinFX.dll, la versione di base Windows Presentation Foundation dll.

> [!Note]  
> La Windows Presentation Foundation di questo esempio (disponibile nella directory XAML) richiede che le estensioni Windows Presentation Foundation per Microsoft Visual Studio 2005 siano installate nel sistema.

 

## <a name="user-interface"></a>Interfaccia utente

L'interfaccia utente per questa applicazione è costituita da un [controllo TabControl](/dotnet/api/system.windows.forms.tabcontrol?view=netcore-3.1) a cui sono associati due oggetti [TabPage:](/dotnet/api/system.windows.forms.tabpage?view=netcore-3.1) Ink Form e Converted Text Form. La scheda Modulo input penna contiene

-   Pannello che contiene un'immagine di un modulo cartaceo digitalizzato usato per l'invio di messaggi telefonici.
-   Casella di controllo in cui l'applicazione visualizza i limiti dei suggerimenti di analisi quando questa opzione è selezionata.
-   Coppia di pulsanti, Clear e Analyze, che cancellano l'input penna dal modulo e inizializzano l'analisi dell'input penna.

Il modulo di testo convertito contiene la stessa immagine ed è la pagina in cui l'applicazione visualizza il testo riconosciuto. Quando si fa clic su Analizza, l'applicazione esegue l'analisi dell'input penna in modo sincrono e i risultati del riconoscimento vengono visualizzati nella scheda Modulo di testo convertito.

## <a name="functionality"></a>Funzionalità

Questa applicazione usa [inkOverlay per](/previous-versions/ms552322(v=vs.100)) abilitare la scrittura. L'oggetto InkOverlay è particolarmente adatto per l'acquisizione di note e lo scribbling di base. L'uso principale previsto di questo oggetto è la visualizzazione dell'input penna come input penna. La classe principale per l'analisi dell'input penna [è la classe InkAnalyzer.](/previous-versions/ms583671(v=vs.100)) Quando si chiama il metodo Analyze [](/previous-versions/ms568971(v=vs.100)) dell'oggetto InkAnalyzer, l'analisi dell'input penna viene eseguita in modo sincrono.

L'applicazione inizializza due matrici, una di stringhe e una di rettangoli. La matrice di stringhe, , è costituito da `factoidStrings` [oggetti Factoid](/previous-versions/ms583657(v=vs.100)) passati in [InkAnalyzer](/previous-versions/ms583671(v=vs.100)) come [oggetti AnalysisHintNode.](/previous-versions/ms573018(v=vs.100)) Gli oggetti AnalysisHintNode orientano InkAnalyzer verso un input specifico. In questo esempio vengono utilizzati i suggerimenti per data, ora e telefono, oltre ad altri.

Ogni [analysisHintNode](/previous-versions/ms573018(v=vs.100)) è associato a un'area specifica del form. Le aree sono rappresentate dalla matrice di rettangoli, `rects` . Creando un [controllo TextBox](/dotnet/api/system.windows.forms.textbox?view=netcore-3.1) per ogni rettangolo, l'esempio restituisce il testo riconosciuto nella posizione corretta.


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



Successivamente, si tratta semplicemente di creare un gestore eventi che attiva l'analisi dell'input penna quando l'utente fa clic su Analizza.


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



 

 

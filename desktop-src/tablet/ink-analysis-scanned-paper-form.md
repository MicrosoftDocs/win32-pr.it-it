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
# <a name="ink-analysis-scanned-paper-form"></a><span data-ttu-id="aa0a1-103">Modulo cartaceo analizzato analisi input penna</span><span class="sxs-lookup"><span data-stu-id="aa0a1-103">Ink Analysis Scanned Paper Form</span></span>

<span data-ttu-id="aa0a1-104">In questo esempio viene illustrato come utilizzare l'analisi dell'input penna per creare un'applicazione di riempimento del modulo, in cui il modulo è basato su un modulo cartaceo digitalizzato.</span><span class="sxs-lookup"><span data-stu-id="aa0a1-104">This sample shows how to use Ink Analysis to create a form-filling application, where the form is based on a scanned paper form.</span></span>

## <a name="features-demonstrated"></a><span data-ttu-id="aa0a1-105">Funzionalità illustrate</span><span class="sxs-lookup"><span data-stu-id="aa0a1-105">Features Demonstrated</span></span>

<span data-ttu-id="aa0a1-106">Questa applicazione di esempio illustra le seguenti funzionalità dell'API di analisi dell'input penna e dei controlli Windows Form input penna:</span><span class="sxs-lookup"><span data-stu-id="aa0a1-106">This sample application demonstrates the following features of the Ink Analysis API and the Windows Forms Ink Controls:</span></span>

-   <span data-ttu-id="aa0a1-107">Caricamento di un modulo cartaceo scansionato.</span><span class="sxs-lookup"><span data-stu-id="aa0a1-107">Loading a scanned paper form.</span></span> <span data-ttu-id="aa0a1-108">L'esempio importa il form da un'immagine in formato png.</span><span class="sxs-lookup"><span data-stu-id="aa0a1-108">The sample imports the form from an image in .png format.</span></span>
-   <span data-ttu-id="aa0a1-109">Raccolta e rendering dell'input penna sopra il modulo sottoposti a scansione.</span><span class="sxs-lookup"><span data-stu-id="aa0a1-109">Collecting and rendering ink on top of the scanned form.</span></span>
-   <span data-ttu-id="aa0a1-110">Uso di un oggetto [InkAnalyzer](/previous-versions/ms583671(v=vs.100)) per analizzare la grafia.</span><span class="sxs-lookup"><span data-stu-id="aa0a1-110">Using an [InkAnalyzer](/previous-versions/ms583671(v=vs.100)) object to parse handwriting.</span></span>
-   <span data-ttu-id="aa0a1-111">Generazione di oggetti [AnalysisHintNode](/previous-versions/ms573018(v=vs.100)) per migliorare i risultati della grafia.</span><span class="sxs-lookup"><span data-stu-id="aa0a1-111">Generating [AnalysisHintNode](/previous-versions/ms573018(v=vs.100)) objects to improve handwriting results.</span></span>
-   <span data-ttu-id="aa0a1-112">Popolamento di caselle di testo da hint di analisi.</span><span class="sxs-lookup"><span data-stu-id="aa0a1-112">Populating text boxes from analysis hints.</span></span>
-   <span data-ttu-id="aa0a1-113">Creazione di un'esperienza di correzione del testo di base.</span><span class="sxs-lookup"><span data-stu-id="aa0a1-113">Creating a basic text correction experience.</span></span>

## <a name="project-references"></a><span data-ttu-id="aa0a1-114">Riferimenti al progetto</span><span class="sxs-lookup"><span data-stu-id="aa0a1-114">Project References</span></span>

<span data-ttu-id="aa0a1-115">L'esempio è disponibile come applicazione Windows Form o Windows Presentation Foundation.</span><span class="sxs-lookup"><span data-stu-id="aa0a1-115">The sample is available as a Windows Forms or Windows Presentation Foundation application.</span></span> <span data-ttu-id="aa0a1-116">Riferimenti alla versione Windows Form:</span><span class="sxs-lookup"><span data-stu-id="aa0a1-116">The Windows Forms version references:</span></span>

-   <span data-ttu-id="aa0a1-117">Microsoft.Ink.dll</span><span class="sxs-lookup"><span data-stu-id="aa0a1-117">Microsoft.Ink.dll</span></span>
-   <span data-ttu-id="aa0a1-118">Microsoft.Ink.Analysis.dll</span><span class="sxs-lookup"><span data-stu-id="aa0a1-118">Microsoft.Ink.Analysis.dll</span></span>

<span data-ttu-id="aa0a1-119">La versione Windows Presentation Foundation fa riferimento IAWinFX.dll oltre alle DLL core Windows Presentation Foundation.</span><span class="sxs-lookup"><span data-stu-id="aa0a1-119">The Windows Presentation Foundation version references IAWinFX.dll in addition to the core Windows Presentation Foundation dlls.</span></span>

> [!Note]  
> <span data-ttu-id="aa0a1-120">Per la versione Windows Presentation Foundation di questo esempio, disponibile nella directory XAML, è necessario che nel sistema siano installate le estensioni Windows Presentation Foundation per Microsoft Visual Studio 2005.</span><span class="sxs-lookup"><span data-stu-id="aa0a1-120">The Windows Presentation Foundation version of this sample (found in the XAML directory) requires that the Windows Presentation Foundation extensions for Microsoft Visual Studio 2005 is installed on the system.</span></span>

 

## <a name="user-interface"></a><span data-ttu-id="aa0a1-121">Interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="aa0a1-121">User Interface</span></span>

<span data-ttu-id="aa0a1-122">L'interfaccia utente per questa applicazione è costituita da un oggetto [TabControl](/dotnet/api/system.windows.forms.tabcontrol?view=netcore-3.1) con due oggetti [TabPage](/dotnet/api/system.windows.forms.tabpage?view=netcore-3.1) associati: form input penna e formato testo convertito.</span><span class="sxs-lookup"><span data-stu-id="aa0a1-122">The UI for this application consists of a [TabControl](/dotnet/api/system.windows.forms.tabcontrol?view=netcore-3.1) with two [TabPage](/dotnet/api/system.windows.forms.tabpage?view=netcore-3.1) objects associated with it: Ink Form and Converted Text Form.</span></span> <span data-ttu-id="aa0a1-123">La scheda modulo input penna contiene</span><span class="sxs-lookup"><span data-stu-id="aa0a1-123">The Ink Form tab contains</span></span>

-   <span data-ttu-id="aa0a1-124">Pannello che contiene un'immagine di un modulo cartaceo digitalizzato utilizzato per l'esecuzione di messaggi telefonici.</span><span class="sxs-lookup"><span data-stu-id="aa0a1-124">A panel that contains an image of a scanned paper form used for taking telephone messages.</span></span>
-   <span data-ttu-id="aa0a1-125">Una casella di controllo con l'applicazione Mostra i limiti dell'hint di analisi quando è selezionata.</span><span class="sxs-lookup"><span data-stu-id="aa0a1-125">A check box that has the application show the analysis hint bounds when selected.</span></span>
-   <span data-ttu-id="aa0a1-126">Una coppia di pulsanti, Clear e Analyze, che cancellano l'input penna dal form e inizializzano l'analisi dell'input penna.</span><span class="sxs-lookup"><span data-stu-id="aa0a1-126">A pair of buttons, Clear and Analyze, that clear the ink from the form and initialize ink analysis.</span></span>

<span data-ttu-id="aa0a1-127">Il formato di testo convertito contiene la stessa immagine e è la pagina in cui l'applicazione Visualizza il testo riconosciuto.</span><span class="sxs-lookup"><span data-stu-id="aa0a1-127">The Converted Text Form contains the same image and is the page on which the application displays the recognized text.</span></span> <span data-ttu-id="aa0a1-128">Quando si fa clic su analizza, l'applicazione esegue l'analisi dell'input penna in modo sincrono e i risultati del riconoscimento vengono visualizzati nella scheda formato testo convertito.</span><span class="sxs-lookup"><span data-stu-id="aa0a1-128">When you click Analyze, the application performs ink analysis synchronously, and the recognition results appear on the Converted Text Form tab.</span></span>

## <a name="functionality"></a><span data-ttu-id="aa0a1-129">Funzionalità</span><span class="sxs-lookup"><span data-stu-id="aa0a1-129">Functionality</span></span>

<span data-ttu-id="aa0a1-130">Questa applicazione usa un oggetto [InkOverlay](/previous-versions/ms552322(v=vs.100)) per abilitare la scrittura.</span><span class="sxs-lookup"><span data-stu-id="aa0a1-130">This application uses an [InkOverlay](/previous-versions/ms552322(v=vs.100)) to enable writing.</span></span> <span data-ttu-id="aa0a1-131">L'oggetto InkOverlay è particolarmente adatto per l'acquisizione di note e per la creazione di un scarabocchio di base.</span><span class="sxs-lookup"><span data-stu-id="aa0a1-131">The InkOverlay object is well suited for note taking and basic scribbling.</span></span> <span data-ttu-id="aa0a1-132">L'utilizzo previsto principale di questo oggetto consiste nel visualizzare input penna come input penna.</span><span class="sxs-lookup"><span data-stu-id="aa0a1-132">The primary intended use of this object is to display ink as ink.</span></span> <span data-ttu-id="aa0a1-133">La classe principale per l'analisi dell'input penna è la classe [InkAnalyzer](/previous-versions/ms583671(v=vs.100)) .</span><span class="sxs-lookup"><span data-stu-id="aa0a1-133">The main class for ink analysis is the [InkAnalyzer](/previous-versions/ms583671(v=vs.100)) class.</span></span> <span data-ttu-id="aa0a1-134">Quando si chiama il metodo [Analyze](/previous-versions/ms568971(v=vs.100)) dell'oggetto InkAnalyzer, l'analisi dell'input penna viene eseguita in modo sincrono.</span><span class="sxs-lookup"><span data-stu-id="aa0a1-134">When you call the InkAnalyzer object's [Analyze](/previous-versions/ms568971(v=vs.100)) method, the ink analysis occurs synchronously.</span></span>

<span data-ttu-id="aa0a1-135">L'applicazione Inizializza due matrici, una delle stringhe e uno dei rettangoli.</span><span class="sxs-lookup"><span data-stu-id="aa0a1-135">The application initializes two arrays, one of strings and one of rectangles.</span></span> <span data-ttu-id="aa0a1-136">La matrice di stringhe, `factoidStrings` , è costituita da oggetti del controllo del controllo che vengono passati in [InkAnalyzer](/previous-versions/ms583671(v=vs.100)) come oggetti [AnalysisHintNode](/previous-versions/ms573018(v=vs.100)) . [](/previous-versions/ms583657(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="aa0a1-136">The string array, `factoidStrings`, is made of [Factoid](/previous-versions/ms583657(v=vs.100)) objects that are passed into the [InkAnalyzer](/previous-versions/ms583671(v=vs.100)) as [AnalysisHintNode](/previous-versions/ms573018(v=vs.100)) objects.</span></span> <span data-ttu-id="aa0a1-137">Gli oggetti AnalysisHintNode polarizzano l'oggetto InkAnalyzer verso un input specifico.</span><span class="sxs-lookup"><span data-stu-id="aa0a1-137">The AnalysisHintNode objects bias the InkAnalyzer toward particular input.</span></span> <span data-ttu-id="aa0a1-138">In questo esempio vengono utilizzati gli hint per la data, l'ora e il telefono, nonché altri.</span><span class="sxs-lookup"><span data-stu-id="aa0a1-138">This sample uses the date, time, and telephone hints, as well as some others.</span></span>

<span data-ttu-id="aa0a1-139">Ogni elemento [AnalysisHintNode](/previous-versions/ms573018(v=vs.100)) è associato a un'area specifica del modulo.</span><span class="sxs-lookup"><span data-stu-id="aa0a1-139">Each [AnalysisHintNode](/previous-versions/ms573018(v=vs.100)) is associated with a specific area of the form.</span></span> <span data-ttu-id="aa0a1-140">Le aree sono rappresentate dalla matrice di rettangoli, `rects` .</span><span class="sxs-lookup"><span data-stu-id="aa0a1-140">The areas are represented by the array of rectangles, `rects`.</span></span> <span data-ttu-id="aa0a1-141">Creando una [casella](/dotnet/api/system.windows.forms.textbox?view=netcore-3.1) di testo per ogni rettangolo, l'esempio restituisce il testo riconosciuto nella posizione corretta.</span><span class="sxs-lookup"><span data-stu-id="aa0a1-141">By creating a [TextBox](/dotnet/api/system.windows.forms.textbox?view=netcore-3.1) for each rectangle, the sample outputs the recognized text in the correct location.</span></span>


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



<span data-ttu-id="aa0a1-142">Successivamente, è sufficiente creare un gestore eventi che attiva l'analisi dell'input penna quando l'utente fa clic su analizza.</span><span class="sxs-lookup"><span data-stu-id="aa0a1-142">After that, it is merely a matter of creating an event handler that triggers the ink analysis when the user clicks Analyze.</span></span>


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



 

 

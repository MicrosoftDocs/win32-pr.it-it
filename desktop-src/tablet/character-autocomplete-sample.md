---
description: Nell'esempio di completamento automatico viene illustrato come implementare il completamento automatico dei caratteri in giapponese usando le API (Application Programming Interface) di riconoscimento.
ms.assetid: 237e33bc-3708-4128-8749-d3d031f7237a
title: Esempio di completamento automatico di caratteri
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4853cdef72a087aff3b9b726f0c83af9038ef5bc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524401"
---
# <a name="character-autocomplete-sample"></a><span data-ttu-id="acdad-103">Esempio di completamento automatico di caratteri</span><span class="sxs-lookup"><span data-stu-id="acdad-103">Character Autocomplete Sample</span></span>

<span data-ttu-id="acdad-104">Nell'esempio di completamento automatico viene illustrato come implementare il completamento automatico dei caratteri in giapponese usando le API (Application Programming Interface) di riconoscimento.</span><span class="sxs-lookup"><span data-stu-id="acdad-104">The Autocomplete sample demonstrates how to implement character Autocomplete in Japanese by using the recognition application programming interfaces (APIs).</span></span>

<span data-ttu-id="acdad-105">In questo esempio vengono usate le funzionalità seguenti:</span><span class="sxs-lookup"><span data-stu-id="acdad-105">The following features are used in this sample:</span></span>

-   <span data-ttu-id="acdad-106">Uso di un *agente di raccolta input penna*</span><span class="sxs-lookup"><span data-stu-id="acdad-106">Using an *ink collector*</span></span>
-   <span data-ttu-id="acdad-107">Uso di un *contesto di riconoscimento*</span><span class="sxs-lookup"><span data-stu-id="acdad-107">Using a *recognizer context*</span></span>

## <a name="initializing-the-ink-collector-and-recognizer-context"></a><span data-ttu-id="acdad-108">Inizializzazione dell'agente di raccolta input penna e del contesto di riconoscimento</span><span class="sxs-lookup"><span data-stu-id="acdad-108">Initializing the Ink Collector and Recognizer Context</span></span>

<span data-ttu-id="acdad-109">Gli oggetti [**InkCollector**](inkcollector-class.md) e [**InkRecognizerContext**](inkrecognizercontext-class.md) vengono dichiarati come classi che possono generare eventi.</span><span class="sxs-lookup"><span data-stu-id="acdad-109">The [**InkCollector**](inkcollector-class.md) and [**InkRecognizerContext**](inkrecognizercontext-class.md) objects are declared as classes that can raise events.</span></span>


```C++
Dim WithEvents ic As InkCollector
Dim WithEvents rc As InkRecognizerContext
```



<span data-ttu-id="acdad-110">Il gestore dell'evento Load del form crea un agente di raccolta input penna, associa l'agente di raccolta input penna alla casella immagine e Abilita la raccolta di input penna.</span><span class="sxs-lookup"><span data-stu-id="acdad-110">The form's Load event handler creates an ink collector, associates the ink collector to picture box, and enables ink collection.</span></span> <span data-ttu-id="acdad-111">Il gestore eventi carica quindi il riconoscimento giapponese predefinito e inizializza le proprietà guide e Strokes del contesto di riconoscimento.</span><span class="sxs-lookup"><span data-stu-id="acdad-111">The event handler then loads the default Japanese recognizer, and initializes the recognizer context 's Guide and Strokes properties.</span></span>


```C++
Private Sub Form_Load()
   ' Set the ink collector to work in the small frame window
    Set ic = New InkCollector    ic.hWnd = fraBox.hWnd    ic.Enabled = True
    
    ' Get the Japanese recognizer
    LoadRecognizer

    ' Initialize the recognizer context
    Dim Guide As New InkRecognizerGuide
    Dim FrameRectangle As New InkRectangle
    Dim Top As Long
    Dim Bottom As Long
    Dim Left As Long
    Dim Right As Long
    Top = 0
    Left = 0
    Bottom = fraBox.ScaleHeight
    Right = fraBox.ScaleWidth
    ic.Renderer.PixelToInkSpace Me.hdc, Top, Left
    ic.Renderer.PixelToInkSpace Me.hdc, Bottom, Right
    FrameRectangle.Bottom = Bottom
    FrameRectangle.Top = Top
    FrameRectangle.Left = Left
    FrameRectangle.Right = Right
    Guide.Columns = 1
    Guide.Rows = 1
    Guide.Midline = -1 ' Do not use midline
    Guide.DrawnBox = FrameRectangle
    Guide.WritingBox = FrameRectangle
    Set rc.Guide = Guide
    
    ' Set the strokes collection on the recognizer context
    Set ink = ic.ink    Set rc.Strokes = ic.ink.Strokes
End Sub
```



## <a name="loading-the-default-japanese-recognizer"></a><span data-ttu-id="acdad-112">Caricamento del riconoscimento giapponese predefinito</span><span class="sxs-lookup"><span data-stu-id="acdad-112">Loading the Default Japanese Recognizer</span></span>

<span data-ttu-id="acdad-113">Il metodo [**GetDefaultRecognizer**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizers-getdefaultrecognizer) di [**dagli oggetti InkRecognizer**](/previous-versions/windows/desktop/legacy/ms702438(v=vs.85)) viene chiamato per recuperare il riconoscimento predefinito per la lingua giapponese.</span><span class="sxs-lookup"><span data-stu-id="acdad-113">The [**GetDefaultRecognizer**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizers-getdefaultrecognizer) method of the [**InkRecognizers**](/previous-versions/windows/desktop/legacy/ms702438(v=vs.85)) is called to retrieve the default recognizer for the Japanese language.</span></span> <span data-ttu-id="acdad-114">Successivamente, viene verificata la proprietà [**Languages**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizer-get_languages) dell'oggetto IInkRecognizer per determinare se il riconoscimento supporta la lingua giapponese.</span><span class="sxs-lookup"><span data-stu-id="acdad-114">Next, the IInkRecognizer object's [**Languages**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizer-get_languages) property is checked to determine if the recognizer supports the Japanese language.</span></span> <span data-ttu-id="acdad-115">In caso contrario, viene usato il metodo [**CreateRecognizerContext**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizer-createrecognizercontext) del riconoscitore per generare un contesto di riconoscimento per il form.</span><span class="sxs-lookup"><span data-stu-id="acdad-115">If it does, then the recognizer's [**CreateRecognizerContext**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizer-createrecognizercontext) method is used to generate a recognizer context for the form.</span></span>


```C++
Private Sub LoadRecognizer()
    On Error GoTo NoRecognizer
    ' Get a Japanese recognizer context
    Dim recos As New InkRecognizers
    Dim JapaneseReco As IInkRecognizer
    Set JapaneseReco = recos.GetDefaultRecognizer(&H411)
    If JapaneseReco Is Nothing Then
        MsgBox "Japanese Recognizers are not installed on this system. Exiting."
        End
    End If
    
    ' Check that this is indeed a Japanese recognizer
    Dim IsJapanese As Boolean
    Dim lan As Integer
    IsJapanese = False
    For lan = LBound(JapaneseReco.Languages) To UBound(JapaneseReco.Languages)
        If JapaneseReco.Languages(lan) = &H411 Then
            IsJapanese = True
        End If
    Next lan
    If Not IsJapanese Then
        MsgBox "Japanese Recognizers are not installed on this system. Exiting."
        End
    End If
    Set rc = JapaneseReco.CreateRecognizerContext
    Exit Sub
NoRecognizer:
    MsgBox "Japanese Recognizers are not installed on this system. Exiting."
    End
End Sub
```



## <a name="handling-the-stroke-event"></a><span data-ttu-id="acdad-116">Gestione dell'evento Stroke</span><span class="sxs-lookup"><span data-stu-id="acdad-116">Handling the Stroke Event</span></span>

<span data-ttu-id="acdad-117">Il gestore dell'evento [**Stroke**](inkcollector-stroke.md) interrompe innanzitutto il riconoscimento in background nel contesto del riconoscimento.</span><span class="sxs-lookup"><span data-stu-id="acdad-117">The [**Stroke**](inkcollector-stroke.md) event handler first halts background recognition on the recognizer context.</span></span> <span data-ttu-id="acdad-118">Aggiunge quindi il nuovo tratto alla proprietà [**Strokes**](/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionresult-get_strokes) del contesto del riconoscitore.</span><span class="sxs-lookup"><span data-stu-id="acdad-118">Then, it adds the new stroke to the recognizer context's [**Strokes**](/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionresult-get_strokes) property.</span></span> <span data-ttu-id="acdad-119">Infine, imposta la proprietà [**InkRecognizerCharacterAutoCompletionMode**](/windows/desktop/api/msinkaut/ne-msinkaut-inkrecognizercharacterautocompletionmode) del contesto del riconoscitore e chiama il metodo [**BackgroundRecognizeWithAlternates**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognizewithalternates) del contesto del riconoscitore per ognuna delle tre modalità di completamento automatico dei tre caratteri.</span><span class="sxs-lookup"><span data-stu-id="acdad-119">Finally, it sets the recognizer context's [**InkRecognizerCharacterAutoCompletionMode**](/windows/desktop/api/msinkaut/ne-msinkaut-inkrecognizercharacterautocompletionmode) property and calls the recognizer context's [**BackgroundRecognizeWithAlternates**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognizewithalternates) method for each of the three character Autocomplete modes.</span></span> <span data-ttu-id="acdad-120">Il parametro *CustomData* della chiamata al metodo **BackgroundRecognizeWithAlternates** viene usato per identificare i risultati del riconoscimento restituiti nell'evento [**RecognitionWithAlternates**](inkrecognizercontext-recognitionwithalternates.md) .</span><span class="sxs-lookup"><span data-stu-id="acdad-120">The *CustomData* parameter of the **BackgroundRecognizeWithAlternates** method call is used to identify which recognition results are returned in the [**RecognitionWithAlternates**](inkrecognizercontext-recognitionwithalternates.md) event.</span></span>


```C++
Private Sub ic_Stroke(ByVal Cursor As MSINKAUTLib.IInkCursor, ByVal Stroke As MSINKAUTLib.IInkStrokeDisp, Cancel As Boolean)

    ' Stop the unfinished recognition processes
    rc.StopBackgroundRecognition

    ' Add the new stroke
    rc.Strokes.Add Stroke

    ' Get a result for all three CAC modes
    rc.CharacterAutoCompletionMode = IRCACM_Full rc.BackgroundRecognizeWithAlternates 0 rc.CharacterAutoCompletionMode = IRCACM_Prefix rc.BackgroundRecognizeWithAlternates 1 rc.CharacterAutoCompletionMode = IRCACM_Random rc.BackgroundRecognizeWithAlternates 2
End Sub
```



## <a name="handling-the-recognition-with-alternates-event"></a><span data-ttu-id="acdad-121">Gestione dell'evento di riconoscimento con alternative</span><span class="sxs-lookup"><span data-stu-id="acdad-121">Handling the Recognition with Alternates Event</span></span>

<span data-ttu-id="acdad-122">Il gestore per l'evento [**RecognitionWithAlternates**](inkrecognizercontext-recognitionwithalternates.md) verifica innanzitutto il parametro *RecognitionStatus* .</span><span class="sxs-lookup"><span data-stu-id="acdad-122">The handler for the [**RecognitionWithAlternates**](inkrecognizercontext-recognitionwithalternates.md) event first checks the *RecognitionStatus* parameter.</span></span> <span data-ttu-id="acdad-123">Se si verifica un errore di riconoscimento, il gestore dell'evento ignora i risultati del riconoscimento.</span><span class="sxs-lookup"><span data-stu-id="acdad-123">If there is an error in recognition, the event handler ignores the recognition results.</span></span> <span data-ttu-id="acdad-124">In caso contrario, il gestore eventi aggiunge il parametro *RecognitionResult* alla casella immagine appropriata e salva la stringa di risultato.</span><span class="sxs-lookup"><span data-stu-id="acdad-124">Otherwise, the event handler adds the *RecognitionResult* parameter to the appropriate picture box and saves the result string.</span></span> <span data-ttu-id="acdad-125">Il parametro *CustomData* viene impostato nella chiamata al metodo [**BackgroundRecognizeWithAlternates**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognizewithalternates) e identifica la modalità di completamento automatico dei caratteri utilizzata dal contesto del riconoscimento.</span><span class="sxs-lookup"><span data-stu-id="acdad-125">The *CustomData* parameter is set in the call to the [**BackgroundRecognizeWithAlternates**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognizewithalternates) method and identifies which character Autocomplete mode was used by the recognizer context.</span></span>


```C++
Private Sub rc_RecognitionWithAlternates(ByVal RecognitionResult As MSINKAUTLib.IInkRecognitionResult, ByVal vCustomParam As Variant, ByVal RecognitionStatus As MSINKAUTLib.InkRecognitionStatus)
    ' Get the alternates from the recognition result
    ' and display them in the right place
    Dim ResultString As String
    Dim alts As IInkRecognitionAlternates
    Dim alt As IInkRecognitionAlternate
        
    On Error GoTo EndFunc

    If RecognitionStatus = IRS_NoError Then
        ' Fill a string with all the characters for this CAC mode
        Set alts = RecognitionResult.AlternatesFromSelection
        For Each alt In alts
            ResultString = ResultString + alt.String
        Next alt
        ' Display the string
        Dim r As RECT
        r.Left = 0
        r.Top = 0
        r.Right = 1000
        r.Bottom = 1000
        PctResult(vCustomParam).Cls
        DrawText PctResult(vCustomParam).hdc, StrPtr(ResultString), Len(ResultString), r, 0
        If vCustomParam = 0 Then
            FullCACText = ResultString
        Else
            If vCustomParam = 1 Then
                PrefixCACText = ResultString
            Else
                If vCustomParam = 2 Then
                    RandomCACText = ResultString
                End If
            End If
        End If
    End If
    Exit Sub
EndFunc:
    MsgBox Err.Description
End Sub
```



## <a name="painting-the-form"></a><span data-ttu-id="acdad-126">Disegno del form</span><span class="sxs-lookup"><span data-stu-id="acdad-126">Painting the Form</span></span>

<span data-ttu-id="acdad-127">Il gestore eventi Paint Cancella le caselle immagine dei risultati e aggiunge i risultati del riconoscimento salvati.</span><span class="sxs-lookup"><span data-stu-id="acdad-127">The Paint event handler clears the results picture boxes and adds the saved recognition results to them.</span></span>

## <a name="deleting-the-strokes"></a><span data-ttu-id="acdad-128">Eliminazione dei tratti</span><span class="sxs-lookup"><span data-stu-id="acdad-128">Deleting the Strokes</span></span>

<span data-ttu-id="acdad-129">Il metodo del modulo `CmdClear_Click` gestisce il comando Cancella.</span><span class="sxs-lookup"><span data-stu-id="acdad-129">The form's `CmdClear_Click` method handles the Clear command.</span></span> <span data-ttu-id="acdad-130">Se l'oggetto [**InkCollector**](inkcollector-class.md) sta attualmente raccogliendo l'input penna, viene visualizzata una finestra di messaggio e il comando viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="acdad-130">If the [**InkCollector**](inkcollector-class.md) is currently collecting ink, then a message box is displayed and the command is ignored.</span></span> <span data-ttu-id="acdad-131">In caso contrario, il gestore eventi interrompe il riconoscimento in background, cancella la proprietà [**Strokes**](/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionresult-get_strokes) del contesto di riconoscimento ed Elimina i tratti dall'oggetto [**InkDisp**](inkdisp-class.md) del form.</span><span class="sxs-lookup"><span data-stu-id="acdad-131">Otherwise, the event handler stops background recognition, clears the [**Strokes**](/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionresult-get_strokes) property of the recognizer context, and deletes the strokes from the form's [**InkDisp**](inkdisp-class.md) object.</span></span> <span data-ttu-id="acdad-132">Il gestore eventi ridisegno quindi la casella immagine a cui è associato l'agente di raccolta input penna e cancella le stringhe di riconoscimento e le caselle immagine.</span><span class="sxs-lookup"><span data-stu-id="acdad-132">Then, the event handler redraws the picture box to which the ink collector is associated, and clears the recognition strings and picture boxes.</span></span>


```C++
If Not (ic.CollectingInk) Then

    ' Stop the unfinished recognition processes
    rc.StopBackgroundRecognition

    ' ...
    Set rc.Strokes = Nothing

    ' Delete all the strokes from the ink object
    ic.Ink.DeleteStrokes strokesToDelete

    ' Refresh the window
    fraBox.Refresh

    ' refresh the recognizer context
    Set rc.Strokes = ic.Ink.Strokes

    ' Clear the result strings
    FullCACText = ""
    PrefixCACText = ""
    RandomCACText = ""

    ' Clear the result windows
    PctResult(0).Cls
    PctResult(1).Cls
    PctResult(2).Cls

Else
    MsgBox "Cannot clear ink while the ink collector is busy."
End If
```



 

 

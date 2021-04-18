---
description: In questo esempio vengono illustrate le funzionalità avanzate del Application Programming Interface di automazione del PC MicrosoftTablet (API) utilizzato per il riconoscimento della grafia.
ms.assetid: c9e6613c-5797-44c3-8ce1-92d4d1459ecf
title: Esempio di più riconoscitori
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a21d24001e3544be16dde4d288a8adc7ea0081f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315563"
---
# <a name="multiple-recognizers-sample"></a><span data-ttu-id="ff3a6-103">Esempio di più riconoscitori</span><span class="sxs-lookup"><span data-stu-id="ff3a6-103">Multiple Recognizers Sample</span></span>

<span data-ttu-id="ff3a6-104">In questo esempio vengono illustrate le funzionalità avanzate del Application Programming Interface di automazione del PC MicrosoftTablet (API) utilizzato per il riconoscimento della *grafia* .</span><span class="sxs-lookup"><span data-stu-id="ff3a6-104">This sample demonstrates advanced features of the MicrosoftTablet PC Automation application programming interface (API) used for *handwriting* recognition.</span></span>

<span data-ttu-id="ff3a6-105">Include quanto segue:</span><span class="sxs-lookup"><span data-stu-id="ff3a6-105">It includes the following:</span></span>

-   <span data-ttu-id="ff3a6-106">Enumerazione dei riconoscitori installati</span><span class="sxs-lookup"><span data-stu-id="ff3a6-106">Enumerating the installed recognizers</span></span>
-   <span data-ttu-id="ff3a6-107">Creazione di un *contesto di riconoscimento* con un riconoscimento lingua specifico</span><span class="sxs-lookup"><span data-stu-id="ff3a6-107">Creating a *recognizer context* with a specific language recognizer</span></span>
-   <span data-ttu-id="ff3a6-108">Serializzazione dei risultati del riconoscimento con una raccolta Stroke</span><span class="sxs-lookup"><span data-stu-id="ff3a6-108">Serializing recognition results with a stroke collection</span></span>
-   <span data-ttu-id="ff3a6-109">Organizzazione delle raccolte di tratti in una raccolta personalizzata all'interno dell'oggetto [**InkDisp**](inkdisp-class.md)</span><span class="sxs-lookup"><span data-stu-id="ff3a6-109">Organizing stroke collections into a custom collection within the [**InkDisp**](inkdisp-class.md) object</span></span>
-   <span data-ttu-id="ff3a6-110">Serializzazione e recupero di oggetti *Ink* da un file di *formato ISF (Ink Serialized Format)*</span><span class="sxs-lookup"><span data-stu-id="ff3a6-110">Serializing *ink* objects to and retrieving them from an *ink serialized format (ISF)* file</span></span>
-   <span data-ttu-id="ff3a6-111">Impostazione delle guide di input del riconoscimento</span><span class="sxs-lookup"><span data-stu-id="ff3a6-111">Setting recognizer input guides</span></span>
-   <span data-ttu-id="ff3a6-112">Uso del riconoscimento sincrono e asincrono</span><span class="sxs-lookup"><span data-stu-id="ff3a6-112">Using synchronous and asynchronous recognition</span></span>

## <a name="ink-headers"></a><span data-ttu-id="ff3a6-113">Intestazioni Ink</span><span class="sxs-lookup"><span data-stu-id="ff3a6-113">Ink Headers</span></span>

<span data-ttu-id="ff3a6-114">Includere innanzitutto le intestazioni per le interfacce di automazione dei Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="ff3a6-114">First, include the headers for Tablet PC Automation interfaces.</span></span> <span data-ttu-id="ff3a6-115">Vengono installati con il Software Development Kit (SDK) di Microsoft Windows XP Tablet PC Edition.</span><span class="sxs-lookup"><span data-stu-id="ff3a6-115">These are installed with the Microsoft Windows XP Tablet PC Edition Software Development Kit (SDK).</span></span>


```C++
#include <msinkaut.h>
#include <msinkaut_i.c>
```



<span data-ttu-id="ff3a6-116">Il file EventSinks. h definisce le interfacce IInkEventsImpl e IInkRecognitionEventsImpl.</span><span class="sxs-lookup"><span data-stu-id="ff3a6-116">The EventSinks.h file defines the IInkEventsImpl and IInkRecognitionEventsImpl interfaces.</span></span>


```C++
#include "EventSinks.h"
```



## <a name="enumerating-the-installed-recognizers"></a><span data-ttu-id="ff3a6-117">Enumerazione dei riconoscitori installati</span><span class="sxs-lookup"><span data-stu-id="ff3a6-117">Enumerating the Installed Recognizers</span></span>

<span data-ttu-id="ff3a6-118">Il metodo LoadMenu dell'applicazione popola il menu Crea nuovi tratti con i riconoscitori disponibili.</span><span class="sxs-lookup"><span data-stu-id="ff3a6-118">The application's LoadMenu method populates the Create New Strokes menu with the available recognizers.</span></span> <span data-ttu-id="ff3a6-119">Viene creato un [**dagli oggetti InkRecognizer**](/previous-versions/windows/desktop/legacy/ms702438(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="ff3a6-119">An [**InkRecognizers**](/previous-versions/windows/desktop/legacy/ms702438(v=vs.85)) is created.</span></span> <span data-ttu-id="ff3a6-120">Se la proprietà [**Languages**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizer-get_languages) di un oggetto **dagli oggetti InkRecognizer** non è vuota, il riconoscimento è un riconoscimento di *testo* e il valore della proprietà [**Name**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizer-get_name) viene aggiunto al menu.</span><span class="sxs-lookup"><span data-stu-id="ff3a6-120">If the [**Languages**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizer-get_languages) property of an **InkRecognizers** object is not empty, then the recognizer is a *text recognizer*, and the value of its [**Name**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizer-get_name) property is added to the menu.</span></span>


```C++
// Create the enumerator for the installed recognizers
hr = m_spIInkRecognizers.CoCreateInstance(CLSID_InkRecognizers);
...
    // Filter out non-language recognizers by checking for
    // the languages supported by the recognizer - there is not
    // any if it is a gesture or object recognizer.
    CComVariant vLanguages;
    if (SUCCEEDED(spIInkRecognizer->get_Languages(&vLanguages)))
    {
        if ((VT_ARRAY == (VT_ARRAY & vLanguages.vt))           // it should be an array
            && (NULL != vLanguages.parray)
            && (0 < vLanguages.parray->rgsabound[0].cElements)) // with at least one element
        {
            // This is a language recognizer. Add its name to the menu.
            CComBSTR bstrName;
            if (SUCCEEDED(spIInkRecognizer->get_Name(&bstrName)))
                ...
        }
    }
```



## <a name="creating-an-ink-collector"></a><span data-ttu-id="ff3a6-121">Creazione di un agente di raccolta input penna</span><span class="sxs-lookup"><span data-stu-id="ff3a6-121">Creating an Ink Collector</span></span>

<span data-ttu-id="ff3a6-122">Il metodo OnCreate dell'applicazione crea un oggetto [**InkCollector**](inkcollector-class.md) , lo connette alla relativa origine eventi e Abilita la raccolta di input penna.</span><span class="sxs-lookup"><span data-stu-id="ff3a6-122">The application's OnCreate method creates an [**InkCollector**](inkcollector-class.md) object, connects it to its event source, and enables ink collection.</span></span>


```C++
// Create an ink collector object.
hr = m_spIInkCollector.CoCreateInstance(CLSID_InkCollector);

// Establish a connection to the collector's event source.
hr = IInkCollectorEventsImpl<CMultiRecoApp>::DispEventAdvise(m_spIInkCollector);

// Enable ink input in the m_wndInput window
hr = m_spIInkCollector->put_hWnd((long)m_wndInput.m_hWnd);
hr = m_spIInkCollector->put_Enabled(VARIANT_TRUE);
```



## <a name="creating-a-recognizer-context"></a><span data-ttu-id="ff3a6-123">Creazione di un contesto di riconoscimento</span><span class="sxs-lookup"><span data-stu-id="ff3a6-123">Creating a Recognizer Context</span></span>

<span data-ttu-id="ff3a6-124">Il metodo CreateRecoContext dell'applicazione crea e Inizializza un nuovo contesto di riconoscimento e configura le guide supportate dal linguaggio associato.</span><span class="sxs-lookup"><span data-stu-id="ff3a6-124">The application's CreateRecoContext method creates and initializes a new recognizer context, and sets up the guides supported by the associated language.</span></span> <span data-ttu-id="ff3a6-125">Il metodo [**CreateRecognizerContext**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizer-createrecognizercontext) dell'oggetto [**IInkRecognizer**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer) crea un oggetto [**IInkRecognizerContext2**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizercontext2) per la lingua.</span><span class="sxs-lookup"><span data-stu-id="ff3a6-125">The [**IInkRecognizer**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer) object's [**CreateRecognizerContext**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizer-createrecognizercontext) method creates a [**IInkRecognizerContext2**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizercontext2) object for the language.</span></span> <span data-ttu-id="ff3a6-126">Se necessario, il contesto del riconoscimento precedente viene sostituito.</span><span class="sxs-lookup"><span data-stu-id="ff3a6-126">If necessary, the old recognizer context is replaced.</span></span> <span data-ttu-id="ff3a6-127">Il contesto è connesso alla relativa origine evento.</span><span class="sxs-lookup"><span data-stu-id="ff3a6-127">The context is connected to its event source.</span></span> <span data-ttu-id="ff3a6-128">Infine, viene verificata la proprietà [**capabilities**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizer-get_capabilities) del contesto di riconoscimento per la quale è supportata la guida del contesto di riconoscimento.</span><span class="sxs-lookup"><span data-stu-id="ff3a6-128">Finally, the [**Capabilities**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizer-get_capabilities) property of the recognizer context is checked for which guides the recognizer context supports.</span></span>


```C++
// Create a recognizer context
CComPtr<IInkRecognizerContext2> spNewContext;
if (FAILED(pIInkRecognizer2->CreateRecognizerContext(&spNewContext)))
    return false;

// Replace the current context with the new one
if (m_spIInkRecoContext != NULL)
{
    // Close the connection to the recognition events source
    IInkRecognitionEventsImpl<CMultiRecoApp>::DispEventUnadvise(m_spIInkRecoContext);
}
m_spIInkRecoContext.Attach(spNewContext.Detach());

// Establish a connection with the recognizer context's event source
if (FAILED(IInkRecognitionEventsImpl<CMultiRecoApp>::DispEventAdvise(m_spIInkRecoContext)))
    ...

// Set the guide if it's supported by the recognizer and has been created 
int cRows = 0, cColumns = 0;
InkRecognizerCapabilities dwCapabilities = IRC_DontCare;
if (SUCCEEDED(pIInkRecognizer->get_Capabilities(&dwCapabilities)))
    ...
```



## <a name="collecting-strokes-and-displaying-recognition-results"></a><span data-ttu-id="ff3a6-129">Raccolta di tratti e visualizzazione dei risultati del riconoscimento</span><span class="sxs-lookup"><span data-stu-id="ff3a6-129">Collecting Strokes and Displaying Recognition Results</span></span>

<span data-ttu-id="ff3a6-130">Il metodo OnStroke dell'applicazione aggiorna il [**InkStrokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) dell'agente di raccolta input penna, Annulla le richieste di riconoscimento asincrone esistenti e crea una richiesta di riconoscimento nel contesto del riconoscimento.</span><span class="sxs-lookup"><span data-stu-id="ff3a6-130">The application's OnStroke method updates the [**InkStrokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) of the ink collector, cancels existing asynchronous recognition requests, and creates a recognition request on the recognizer context.</span></span>


```C++
// Add the new stroke to the current collection
hr = m_spIInkStrokes->Add(pIInkStroke);

if (SUCCEEDED(hr))
{
    // Cancel the previous background recognition requests
    // which have not been processed yet
    m_spIInkRecoContext->StopBackgroundRecognition();

    // Ask the context to update the recognition results with newly added strokes
    // When the results are ready, the recognizer context returns them
    // through the corresponding event RecognitionWithAlternates
    CComVariant vCustomData;
    m_spIInkRecoContext->BackgroundRecognize(vCustomData);
}
```



<span data-ttu-id="ff3a6-131">Il metodo dell'applicazione `OnRecognition` Invia i risultati della richiesta di riconoscimento al metodo della finestra di output `UpdateString` .</span><span class="sxs-lookup"><span data-stu-id="ff3a6-131">The application's `OnRecognition` method sends the results of the recognition request to the output window's `UpdateString` method.</span></span>


```C++
// Update the output window with the new results
m_wndResults.UpdateString(bstrRecognizedString);
```



## <a name="deleting-strokes-and-recognition-results"></a><span data-ttu-id="ff3a6-132">Eliminazione di tratti e risultati del riconoscimento</span><span class="sxs-lookup"><span data-stu-id="ff3a6-132">Deleting Strokes and Recognition Results</span></span>

<span data-ttu-id="ff3a6-133">Il metodo OnClear dell'applicazione elimina tutti i tratti e i risultati di riconoscimento dall'oggetto [**InkDisp**](inkdisp-class.md) e cancella le finestre.</span><span class="sxs-lookup"><span data-stu-id="ff3a6-133">The application's OnClear method deletes all strokes and recognition results from the [**InkDisp**](inkdisp-class.md) object and clears the windows.</span></span> <span data-ttu-id="ff3a6-134">L'associazione del contesto del riconoscimento con la relativa raccolta [**InkStrokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) è stata rimossa.</span><span class="sxs-lookup"><span data-stu-id="ff3a6-134">The recognizer context's association with its [**InkStrokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) collection is removed.</span></span>


```C++
// Detach the current stroke collection from the recognizer context and release it
if (m_spIInkRecoContext != NULL)
    m_spIInkRecoContext->putref_Strokes(NULL);

m_spIInkStrokes.Release();

// Clear the custom strokes collection
if (m_spIInkCustomStrokes != NULL)
    m_spIInkCustomStrokes->Clear();

// Delete all strokes from the Ink object
// Passing NULL as a stroke collection pointer means asking to delete all strokes
m_spIInkDisp->DeleteStrokes(NULL);

// Get a new stroke collection from the ink object
...
// Ask for an empty collection by passing an empty variant 
if (SUCCEEDED(m_spIInkDisp->CreateStrokes(v, &m_spIInkStrokes)))
{
    // Attach it to the recognizer context
    if (FAILED(m_spIInkRecoContext->putref_Strokes(m_spIInkStrokes)))
        ...
}
```



## <a name="changing-recognizer-contexts"></a><span data-ttu-id="ff3a6-135">Modifica di contesti di riconoscimento</span><span class="sxs-lookup"><span data-stu-id="ff3a6-135">Changing Recognizer Contexts</span></span>

<span data-ttu-id="ff3a6-136">Il metodo OnNewStrokes dell'applicazione viene chiamato quando l'utente seleziona un riconoscimento nel menu Crea nuovi tratti.</span><span class="sxs-lookup"><span data-stu-id="ff3a6-136">The application's OnNewStrokes method is called when the user selects a recognizer in the Create New Strokes menu.</span></span> <span data-ttu-id="ff3a6-137">Il [**InkStrokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) corrente viene salvato.</span><span class="sxs-lookup"><span data-stu-id="ff3a6-137">The current [**InkStrokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) is saved.</span></span> <span data-ttu-id="ff3a6-138">Se è stato selezionato un riconoscimento lingua diverso, viene creato un nuovo contesto di riconoscimento.</span><span class="sxs-lookup"><span data-stu-id="ff3a6-138">If a different language recognizer was selected, a new recognizer context is created.</span></span> <span data-ttu-id="ff3a6-139">Viene quindi collegato un nuovo **InkStrokes** al nuovo contesto del riconoscimento.</span><span class="sxs-lookup"><span data-stu-id="ff3a6-139">Then, a new **InkStrokes** is attached to the new recognizer context.</span></span>


```C++
// Save the current stroke collection if there is any
if (m_spIInkRecoContext != NULL)
{
    // Cancel the previous background recognition requests
    // which have not been processed yet
    m_spIInkRecoContext->StopBackgroundRecognition();
    
    // Let the context know that there'll be no more input 
    // for the attached stroke collection
    m_spIInkRecoContext->EndInkInput();

    // Add the stroke collection to the Ink object's CustomStrokes collection
    SaveStrokeCollection();
}
...
// If a different recognizer was selected, create a new recognizer context
// Else, reuse the same recognizer context
if (wID != m_nCmdRecognizer)
{
    // Get a pointer to the recognizer object from the recognizer collection  
    CComPtr<IInkRecognizer> spIInkRecognizer;
    if ((m_spIInkRecognizers == NULL)
        || FAILED(m_spIInkRecognizers->Item(wID - ID_RECOGNIZER_FIRST,
                                             &spIInkRecognizer))
        || (false == CreateRecoContext(spIInkRecognizer)))
    {
        // restore the cursor
        ::SetCursor(hCursor);
        return 0;
    }

    // Update the status bar
    m_bstrCurRecoName.Empty();
    spIInkRecognizer->get_Name(&m_bstrCurRecoName);
    UpdateStatusBar();

    // Store the selected recognizer's command id
    m_nCmdRecognizer = wID;
}
```



<span data-ttu-id="ff3a6-140">Chiama quindi StartNewStrokeCollection, che crea un [**InkStrokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) vuoto e lo connette al contesto del riconoscitore.</span><span class="sxs-lookup"><span data-stu-id="ff3a6-140">It then calls StartNewStrokeCollection, which creates an empty [**InkStrokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) and attaches it to the recognizer context.</span></span>

## <a name="saving-the-strokes-collection-for-a-recognizer-context"></a><span data-ttu-id="ff3a6-141">Salvataggio della raccolta Strokes per un contesto di riconoscimento</span><span class="sxs-lookup"><span data-stu-id="ff3a6-141">Saving the Strokes Collection for a Recognizer Context</span></span>

<span data-ttu-id="ff3a6-142">Il metodo dell'applicazione verifica la presenza di `SaveStrokeCollection` un contesto di riconoscimento esistente e finalizza il riconoscimento della raccolta Strokes corrente.</span><span class="sxs-lookup"><span data-stu-id="ff3a6-142">The application's `SaveStrokeCollection` method checks for an existing recognizer context, and finalizes the recognition of the current strokes collection.</span></span> <span data-ttu-id="ff3a6-143">La raccolta [**InkStrokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) viene quindi aggiunta all'oggetto [**CustomStrokes**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-get_customstrokes) dell'oggetto Ink.</span><span class="sxs-lookup"><span data-stu-id="ff3a6-143">Then the [**InkStrokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) collection is added to the [**CustomStrokes**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-get_customstrokes) of the ink object.</span></span>


```C++
if (m_spIInkRecoContext != NULL)
{
    if (SUCCEEDED(m_spIInkStrokes->get_Count(&lCount)) && 0 != lCount)
    {
        CComPtr<IInkRecognitionResult> spIInkRecoResult;
        InkRecognitionStatus RecognitionStatus;
        if (SUCCEEDED(m_spIInkRecoContext->Recognize(&RecognitionStatus, &spIInkRecoResult)))
        {
            if (SUCCEEDED(spIInkRecoResult->SetResultOnStrokes()))
            {
                CComBSTR bstr;
                spIInkRecoResult->get_TopString(&bstr);
                m_wndResults.UpdateString(bstr);
            }
            ...
        }
    }
    // Detach the stroke collection from the old recognizer context
    m_spIInkRecoContext->putref_Strokes(NULL);
}

// Now add it to the ink's custom strokes collection
// Each item (stroke collection) of the custom strokes must be identified
// by a unique string. Here we generate a GUID for this.
if ((0 != lCount) && (m_spIInkCustomStrokes != NULL))
{
    GUID guid;
    WCHAR szGuid[40]; // format: "{xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}"
    if (SUCCEEDED(::CoCreateGuid(&guid)) 
        && (::StringFromGUID2(guid, szGuid, countof(szGuid)) != 0))
    {
        CComBSTR bstrGuid(szGuid);
        if (FAILED(m_spIInkCustomStrokes->Add(bstrGuid, m_spIInkStrokes)))
            ...
```



 

 

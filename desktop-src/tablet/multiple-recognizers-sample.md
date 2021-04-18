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
# <a name="multiple-recognizers-sample"></a>Esempio di più riconoscitori

In questo esempio vengono illustrate le funzionalità avanzate del Application Programming Interface di automazione del PC MicrosoftTablet (API) utilizzato per il riconoscimento della *grafia* .

Include quanto segue:

-   Enumerazione dei riconoscitori installati
-   Creazione di un *contesto di riconoscimento* con un riconoscimento lingua specifico
-   Serializzazione dei risultati del riconoscimento con una raccolta Stroke
-   Organizzazione delle raccolte di tratti in una raccolta personalizzata all'interno dell'oggetto [**InkDisp**](inkdisp-class.md)
-   Serializzazione e recupero di oggetti *Ink* da un file di *formato ISF (Ink Serialized Format)*
-   Impostazione delle guide di input del riconoscimento
-   Uso del riconoscimento sincrono e asincrono

## <a name="ink-headers"></a>Intestazioni Ink

Includere innanzitutto le intestazioni per le interfacce di automazione dei Tablet PC. Vengono installati con il Software Development Kit (SDK) di Microsoft Windows XP Tablet PC Edition.


```C++
#include <msinkaut.h>
#include <msinkaut_i.c>
```



Il file EventSinks. h definisce le interfacce IInkEventsImpl e IInkRecognitionEventsImpl.


```C++
#include "EventSinks.h"
```



## <a name="enumerating-the-installed-recognizers"></a>Enumerazione dei riconoscitori installati

Il metodo LoadMenu dell'applicazione popola il menu Crea nuovi tratti con i riconoscitori disponibili. Viene creato un [**dagli oggetti InkRecognizer**](/previous-versions/windows/desktop/legacy/ms702438(v=vs.85)) . Se la proprietà [**Languages**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizer-get_languages) di un oggetto **dagli oggetti InkRecognizer** non è vuota, il riconoscimento è un riconoscimento di *testo* e il valore della proprietà [**Name**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizer-get_name) viene aggiunto al menu.


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



## <a name="creating-an-ink-collector"></a>Creazione di un agente di raccolta input penna

Il metodo OnCreate dell'applicazione crea un oggetto [**InkCollector**](inkcollector-class.md) , lo connette alla relativa origine eventi e Abilita la raccolta di input penna.


```C++
// Create an ink collector object.
hr = m_spIInkCollector.CoCreateInstance(CLSID_InkCollector);

// Establish a connection to the collector's event source.
hr = IInkCollectorEventsImpl<CMultiRecoApp>::DispEventAdvise(m_spIInkCollector);

// Enable ink input in the m_wndInput window
hr = m_spIInkCollector->put_hWnd((long)m_wndInput.m_hWnd);
hr = m_spIInkCollector->put_Enabled(VARIANT_TRUE);
```



## <a name="creating-a-recognizer-context"></a>Creazione di un contesto di riconoscimento

Il metodo CreateRecoContext dell'applicazione crea e Inizializza un nuovo contesto di riconoscimento e configura le guide supportate dal linguaggio associato. Il metodo [**CreateRecognizerContext**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizer-createrecognizercontext) dell'oggetto [**IInkRecognizer**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer) crea un oggetto [**IInkRecognizerContext2**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizercontext2) per la lingua. Se necessario, il contesto del riconoscimento precedente viene sostituito. Il contesto è connesso alla relativa origine evento. Infine, viene verificata la proprietà [**capabilities**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizer-get_capabilities) del contesto di riconoscimento per la quale è supportata la guida del contesto di riconoscimento.


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



## <a name="collecting-strokes-and-displaying-recognition-results"></a>Raccolta di tratti e visualizzazione dei risultati del riconoscimento

Il metodo OnStroke dell'applicazione aggiorna il [**InkStrokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) dell'agente di raccolta input penna, Annulla le richieste di riconoscimento asincrone esistenti e crea una richiesta di riconoscimento nel contesto del riconoscimento.


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



Il metodo dell'applicazione `OnRecognition` Invia i risultati della richiesta di riconoscimento al metodo della finestra di output `UpdateString` .


```C++
// Update the output window with the new results
m_wndResults.UpdateString(bstrRecognizedString);
```



## <a name="deleting-strokes-and-recognition-results"></a>Eliminazione di tratti e risultati del riconoscimento

Il metodo OnClear dell'applicazione elimina tutti i tratti e i risultati di riconoscimento dall'oggetto [**InkDisp**](inkdisp-class.md) e cancella le finestre. L'associazione del contesto del riconoscimento con la relativa raccolta [**InkStrokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) è stata rimossa.


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



## <a name="changing-recognizer-contexts"></a>Modifica di contesti di riconoscimento

Il metodo OnNewStrokes dell'applicazione viene chiamato quando l'utente seleziona un riconoscimento nel menu Crea nuovi tratti. Il [**InkStrokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) corrente viene salvato. Se è stato selezionato un riconoscimento lingua diverso, viene creato un nuovo contesto di riconoscimento. Viene quindi collegato un nuovo **InkStrokes** al nuovo contesto del riconoscimento.


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



Chiama quindi StartNewStrokeCollection, che crea un [**InkStrokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) vuoto e lo connette al contesto del riconoscitore.

## <a name="saving-the-strokes-collection-for-a-recognizer-context"></a>Salvataggio della raccolta Strokes per un contesto di riconoscimento

Il metodo dell'applicazione verifica la presenza di `SaveStrokeCollection` un contesto di riconoscimento esistente e finalizza il riconoscimento della raccolta Strokes corrente. La raccolta [**InkStrokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) viene quindi aggiunta all'oggetto [**CustomStrokes**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-get_customstrokes) dell'oggetto Ink.


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



 

 

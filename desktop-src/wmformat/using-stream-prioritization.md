---
title: Uso della priorità di flusso
description: Uso della priorità di flusso
ms.assetid: 5fff212e-b47b-49a6-817f-f0e09c895b3a
keywords:
- Windows Media Format SDK, assegnazione di priorità al flusso
- profili, assegnazione di priorità al flusso
- flussi, priorità
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99a6b0bd3d49db9523ef9ea5585803b4c703c279
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "103956169"
---
# <a name="using-stream-prioritization"></a><span data-ttu-id="c6fcf-106">Uso della priorità di flusso</span><span class="sxs-lookup"><span data-stu-id="c6fcf-106">Using Stream Prioritization</span></span>

<span data-ttu-id="c6fcf-107">La definizione delle priorità del flusso consente di avere un maggiore controllo sulla riproduzione del contenuto consentendo di specificare l'ordine di priorità per i flussi in un profilo.</span><span class="sxs-lookup"><span data-stu-id="c6fcf-107">Stream prioritization enables you to have more control over the playback of content by allowing you to specify priority order for the streams in a profile.</span></span> <span data-ttu-id="c6fcf-108">Quando il lettore e il server di streaming riscontrano una carenza di larghezza di banda durante la riproduzione, potrebbe essere necessario eliminare alcuni esempi per fornire la riproduzione senza interruzioni.</span><span class="sxs-lookup"><span data-stu-id="c6fcf-108">When the reader and streaming server encounter a bandwidth shortage during playback, samples may have to be dropped to provide uninterrupted playback.</span></span> <span data-ttu-id="c6fcf-109">Se si specifica un ordine di priorità con un oggetto di assegnazione di priorità del flusso nel profilo, gli esempi verranno eliminati prima dei flussi con priorità più bassa.</span><span class="sxs-lookup"><span data-stu-id="c6fcf-109">If you specify a priority order with a stream prioritization object in the profile, samples will be dropped from the lowest priority streams first.</span></span>

<span data-ttu-id="c6fcf-110">Diversamente dalla condivisione della larghezza di banda e dagli oggetti di esclusione reciproca, un oggetto di assegnazione di priorità del flusso non usa l'interfaccia [**IWMStreamList**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamlist) per tenere traccia dell'elenco dei flussi.</span><span class="sxs-lookup"><span data-stu-id="c6fcf-110">Unlike bandwidth sharing and mutual exclusion objects, a stream prioritization object does not use the [**IWMStreamList**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamlist) interface to keep track of the list of streams.</span></span> <span data-ttu-id="c6fcf-111">È invece necessario usare una matrice di strutture [**di \_ \_ \_ record di priorità di flusso WM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_stream_priority_record) .</span><span class="sxs-lookup"><span data-stu-id="c6fcf-111">Instead, you must use an array of [**WM\_STREAM\_PRIORITY\_RECORD**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_stream_priority_record) structures.</span></span> <span data-ttu-id="c6fcf-112">Le strutture devono essere organizzate nella matrice in ordine decrescente di priorità.</span><span class="sxs-lookup"><span data-stu-id="c6fcf-112">The structures must be organized in the array in descending order of priority.</span></span> <span data-ttu-id="c6fcf-113">Oltre a contenere un numero di flusso, la struttura di priorità del flusso consente inoltre di specificare se un flusso è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="c6fcf-113">In addition to holding a stream number, the stream priority structure also enables you to specify whether a stream is mandatory.</span></span> <span data-ttu-id="c6fcf-114">I flussi obbligatori non verranno eliminati, indipendentemente dalla loro posizione nell'elenco.</span><span class="sxs-lookup"><span data-stu-id="c6fcf-114">Mandatory streams will not be dropped, regardless of their position in the list.</span></span>

<span data-ttu-id="c6fcf-115">Nell'esempio di codice seguente viene illustrato come includere una priorità di flusso in un profilo.</span><span class="sxs-lookup"><span data-stu-id="c6fcf-115">The following example code shows how to include a stream prioritization in a profile.</span></span> <span data-ttu-id="c6fcf-116">Questo profilo è per una presentazione in aula, con un flusso audio del docente, un flusso video del docente e un flusso video che acquisisce le diapositive della presentazione.</span><span class="sxs-lookup"><span data-stu-id="c6fcf-116">This profile is for a classroom presentation, with an audio stream of the lecturer speaking, a video stream of the lecturer, and a video stream capturing the presentation slides.</span></span> <span data-ttu-id="c6fcf-117">Il flusso audio è il più importante e sarà obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="c6fcf-117">The audio stream is the most important and will be mandatory.</span></span> <span data-ttu-id="c6fcf-118">Le diapositive della presentazione avranno la priorità più bassa in quanto l'immagine sarà piuttosto costante, quindi alcuni frame andranno persi e non ci sarà molta differenza.</span><span class="sxs-lookup"><span data-stu-id="c6fcf-118">The presentation slides will have the lowest priority because the image will be pretty constant, so a few frames lost here and there won't make much difference.</span></span>


```C++
IWMProfileManager*       pProfileMgr = NULL;
IWMProfile*              pProfileTmp = NULL;
IWMProfile3*             pProfile    = NULL;
IWMStreamPrioritization* pPriority   = NULL;

WM_STREAM_PRIORITY_RECORD StreamArray[3];
HRESULT hr = S_OK;

// Initialize COM.
hr = CoInitialize(NULL);

// Create a profile manager object.
hr = WMCreateProfileManager(&pProfileMgr);

// Create an empty profile.
hr = pProfileMgr->CreateEmptyProfile(WMT_VER_9_0, &pProfileTmp)

// Get the IWMProfile3 for the new profile, then release the old one.
hr = pProfileTmp->QueryInterface(IID_IWMProfile3, (void**)&pProfile);
pProfileTmp->Release();
pProfileTmp = NULL;

// Give the new profile a name and description.
hr = pProfile->SetName(L"Prioritization_Example");
hr = pProfile->SetDescription(L"Only for use with example code.");

// Create the first stream.
hr = pProfile->CreateNewStream(WMMEDIATYPE_Audio, &pStream);

// TODO: configure the stream as needed for the scenario.

// Set the stream number.
hr = pStream->SetStreamNumber(1);

// Give the stream a name for clarity.
hr = pStream->SetStreamName(L"Lecturer_Audio");

// Include the new stream in the profile.
hr = pProfile->AddStream(pStream);

// Release the stream configuration interface.
pStream->Release();
pStream = NULL;

// Repeat for the other two streams.
hr = pProfile->CreateNewStream(WMMEDIATYPE_Video, &pStream);

// TODO: configure the stream as needed for the scenario.
hr = pStream->SetStreamNumber(2);
hr = pStream->SetStreamName(L"Lecturer_Video");
hr = pProfile->AddStream(pStream);
pStream->Release();
pStream = NULL;

hr = pProfile->CreateNewStream(WMMEDIATYPE_Video, &pStream);

// TODO: configure the stream as needed for the scenario.
hr = pStream->SetStreamNumber(3);
hr = pStream->SetStreamName(L"Slide_Video");
hr = pProfile->AddStream(pStream);
pStream->Release();
pStream = NULL;

// Create a stream prioritization object.
hr = pProfile->CreateNewStreamPrioritization(&pPriority);

// Fill the array with data.
StreamArray[0].wStreamNum = 1;
StreamArray[0].fMandatory = TRUE;

StreamArray[1].wStreamNum = 2;
StreamArray[1].fMandatory = FALSE;

StreamArray[2].wStreamNum = 3;
StreamArray[2].fMandatory = FALSE;

// Assign the stream array to the stream prioritization object.
hr = pPriority->SetPriorityRecords(StreamArray, 3);

// Add the stream prioritization to the profile.
hr = pProfile->SetStreamPrioritization(pPriority);

// Release the stream prioritization object.
pPriority->Release();
pPriority = NULL;

// TODO: Save the profile to a string, and save the string to a file.
// For more information, see To Save a Custom Profile.

// Release the remaining interfaces.
pProfile->Release();
pProfile = NULL;

pProfileMgr->Release();
pProfileMgr = NULL;
```



## <a name="related-topics"></a><span data-ttu-id="c6fcf-119">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c6fcf-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c6fcf-120">**Utilizzo dei profili**</span><span class="sxs-lookup"><span data-stu-id="c6fcf-120">**Working with Profiles**</span></span>](working-with-profiles.md)
</dt> </dl>

 

 





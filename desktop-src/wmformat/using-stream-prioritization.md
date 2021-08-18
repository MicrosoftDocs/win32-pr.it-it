---
title: Uso della priorità del flusso
description: Uso della priorità del flusso
ms.assetid: 5fff212e-b47b-49a6-817f-f0e09c895b3a
keywords:
- Windows MEDIA Format SDK, definizione della priorità dei flussi
- profili,definizione della priorità dei flussi
- flussi, assegnazione di priorità
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3db00466eb27685a33851f7bffa5133e1d94a203985b1a0a56b110a09ad88ab6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118963950"
---
# <a name="using-stream-prioritization"></a>Uso della priorità del flusso

La priorità dei flussi consente di avere un maggiore controllo sulla riproduzione del contenuto consentendo di specificare l'ordine di priorità per i flussi in un profilo. Quando il lettore e il server di streaming riscontrano una mancanza di larghezza di banda durante la riproduzione, potrebbe essere necessario eliminare i campioni per fornire una riproduzione ininterrotta. Se si specifica un ordine di priorità con un oggetto di priorità del flusso nel profilo, gli esempi verranno eliminati prima dai flussi con priorità più bassa.

A differenza degli oggetti di condivisione della larghezza di banda e di esclusione reciproca, un oggetto di priorità del flusso non usa [**l'interfaccia IWMStreamList**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamlist) per tenere traccia dell'elenco di flussi. È invece necessario usare una matrice di [**strutture WM STREAM PRIORITY \_ \_ \_ RECORD.**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_stream_priority_record) Le strutture devono essere organizzate nella matrice in ordine di priorità decrescente. Oltre a contenere un numero di flusso, la struttura di priorità del flusso consente anche di specificare se un flusso è obbligatorio. I flussi obbligatori non verranno eliminati, indipendentemente dalla posizione nell'elenco.

Il codice di esempio seguente illustra come includere una priorità del flusso in un profilo. Questo profilo è per una presentazione in classe, con un flusso audio del docente che parla, un flusso video del docente e un flusso video che acquisisce le diapositive di presentazione. Il flusso audio è il più importante e sarà obbligatorio. Le diapositive della presentazione avranno la priorità più bassa perché l'immagine sarà piuttosto costante, quindi alcuni fotogrammi andranno persi qui e non vi sarà molta differenza.


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



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Uso dei profili**](working-with-profiles.md)
</dt> </dl>

 

 





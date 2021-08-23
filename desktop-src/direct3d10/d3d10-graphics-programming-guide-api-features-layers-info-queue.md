---
description: Personalizzare l'output di debug con ID3D10InfoQueue (Direct3D 10)
ms.assetid: 082c7783-c53a-4b73-b8f2-3f60e2c2689a
title: Personalizzare l'output di debug con ID3D10InfoQueue (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8212b78352ccc9139c069ca5d388993fd83aca6833d77547a91401bc40380fb8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119753831"
---
# <a name="customize-debug-output-with-id3d10infoqueue-direct3d-10"></a>Personalizzare l'output di debug con ID3D10InfoQueue (Direct3D 10)

La coda di informazioni è gestita da un'interfaccia (vedere [**ID3D10InfoQueue Interface**](/windows/desktop/api/D3D10SDKLayers/nn-d3d10sdklayers-id3d10infoqueue)) che archivia, recupera e filtra i messaggi di debug. La coda è costituita da: una coda di messaggi, uno stack di filtri di archiviazione facoltativo e uno stack di filtri di recupero facoltativo. Lo stack di filtri di archiviazione può essere usato per filtrare i messaggi da archiviare. lo stack retrieval-filter può essere usato per filtrare i messaggi da archiviare. Dopo aver filtrato un messaggio, il messaggio verrà stampato nella finestra di debug e archiviato nello stack appropriato.

In generale:

-   Chiamare [**ID3D10InfoQueue::AddApplicationMessage**](/windows/desktop/api/D3D10SDKLayers/nf-d3d10sdklayers-id3d10infoqueue-addapplicationmessage) per generare messaggi definiti dall'utente
-   Chiamare [**ID3D10InfoQueue::GetMessage**](/windows/desktop/api/D3D10SDKLayers/nf-d3d10sdklayers-id3d10infoqueue-getmessage) per ottenere i messaggi (che passano un filtro di recupero facoltativo).

## <a name="registry-controls"></a>Controlli del Registro di sistema

Usare le chiavi del Registro di sistema per modificare le impostazioni del filtro, regolare i punti di interruzione e disattivare l'output di debug. Il livello di debug controlla questi percorsi per le chiavi del Registro di sistema. verrà usato il primo percorso trovato.

1.  HKCU \\ Software \\ Microsoft \\ Direct3D<sottochiave definita \\ dall'utente>
2.  HKLM \\ Software \\ Microsoft \\ Direct3D<sottochiave definita \\ dall'utente>
3.  HKCU \\ Software \\ Microsoft \\ Direct3D

Dove:

-   HKCU sta per HKEY \_ CURRENT \_ USER e HKLM per HKEY \_ LOCAL \_ MACHINE.
-   <sottochiave definita dall'utente> un nome arbitrario per archiviare le impostazioni di debug per un'applicazione

### <a name="filtering-debug-messages-using-registry-keys"></a>Filtro dei messaggi di debug tramite chiavi del Registro di sistema

Se il Registro di sistema contiene una chiave InfoQueueStorageFilterOverride (ed è diverso da zero), i messaggi (e l'output di debug) possono essere filtrati aggiungendo i controlli del Registro di sistema seguenti.

-   DWORD Mute \_ CATEGORY : esegue il debug \_ \* dell'output se questa chiave è diverso da zero.
-   DWORD Mute \_ SEVERITY \_ \* : l'output di debug è disabilitato se questa chiave è diverso da zero.
-   ID mute DWORD: è possibile usare il nome o il numero del messaggio per (proprio come per \_ \_ \* \* l'ID BreakOn \_ descritto in \_ \* precedenza). L'output di debug è disabilitato se questa chiave è diverso da zero.
-   DWORD Unmute \_ SEVERITY \_ INFO : l'output di debug è ABILITATO se questa chiave è diverso da zero. Per impostazione predefinita, quando InfoQueueStorageFilterOverride è abilitato, i messaggi di debug con gravità INFO vengono disattivati, pertanto per questa chiave è possibile riattivare INFO.

Questi controlli modificano se un messaggio viene registrato o visualizzato; non influiscono sul passaggio o sull'esito negativo di un'API.

### <a name="setting-break-conditions-using-registry-keys"></a>Impostazione di condizioni di interruzione tramite chiavi del Registro di sistema

È possibile forzare l'interruzione delle applicazioni in un messaggio usando le chiavi del Registro di sistema seguenti.

**EnableBreakOnMessage:** questa chiave consente l'interruzione dei messaggi e fa sì che le impostazioni setBreakOnCategory()/SetBreakOnSeverity()/SetBreakOnID() di i siano ignorate. I messaggi effettivi da interrompere vengono definiti usando uno o più valori BreakOn \_ \* definiti di seguito.

-   **BreakOn \_ \_CATEGORY \** _ : interrompe qualsiasi messaggio che passa attraverso i filtri di archiviazione. \_ è uno dei messaggi D3D10 \_ MESSAGE \_ CATEGORY.
-   **BreakOn \_ SEVERITY \_ \** _ : interrompe qualsiasi messaggio che passa attraverso i filtri di archiviazione. \_ è uno dei messaggi D3D10 \_ MESSAGE \_ \_ SEVERITY.
-   **BreakOn \_ \_ID \** _ - Interruzione di qualsiasi messaggio che passa attraverso i filtri di archiviazione. \_ è uno dei messaggi D3D10 \_ MESSAGE ID o può essere il valore numerico \_ \_ dell'enumerazione degli errori. Si supponga, ad esempio, che il messaggio con ID "D3D10 MESSAGE ID HYPOTHETICAL" abbia il valore \_ \_ \_ 123 nell'enumerazione D3D10 \_ MESSAGE \_ ID. In questo caso, la creazione del valore BreakOn \_ ID HYPOTHETICAL=1 o BreakOn ID 123=1 commesse entrambe la stessa operazione: interrompere quando viene rilevato un messaggio con \_ \_ ID \_ D3D10 \_ MESSAGE ID \_ \_ HYPOTHETICAL.

### <a name="muting-debug-output-using-registry-keys"></a>Modifica dell'output di debug tramite chiavi del Registro di sistema

L'output di debug può essere disattivato usando una chiave MuteDebugOutput. La presenza di questo valore nel Registro di sistema forza l'override del metodo [**ID3D10InfoQueue::SetMuteDebugOutput di**](/windows/desktop/api/D3D10SDKLayers/nf-d3d10sdklayers-id3d10infoqueue-setmutedebugoutput) InfoQueue. MuteDebugOutput arresta i messaggi che passano il filtro di archiviazione dall'invio all'output di debug.

## <a name="disabling-debug-layer-messages"></a>Disabilitazione dei messaggi del livello di debug

I messaggi del livello di debug possono essere disabilitati singolarmente o come gruppo in fase di esecuzione specificando filtri [**tramite ID3D10InfoQueue::AddStorageFilterEntries**](/windows/desktop/api/D3D10SDKLayers/nf-d3d10sdklayers-id3d10infoqueue-addstoragefilterentries). L'argomento *pFilter* **per ID3D10InfoQueue::AddStorageFilterEntries** accetta una struttura [**D3D10 \_ INFO QUEUE \_ \_ FILTER**](/windows/desktop/api/d3d10sdklayers/ns-d3d10sdklayers-d3d10_info_queue_filter) che contiene un elenco di elementi consentiti e un elenco di elementi non consentiti. Gli elenchi consentiti e non consentiti sono descritti dalle strutture [**\_ \_ \_ \_ DESC D3D10 INFO QUEUE FILTER**](/windows/desktop/api/d3d10sdklayers/ns-d3d10sdklayers-d3d10_info_queue_filter_desc) che consentono di impostare il filtro in base a catergory, severity e ID singolo messaggio.

Il codice seguente è un esempio di configurazione dell'interfaccia [**ID3D10InfoQueue**](/windows/desktop/api/D3D10SDKLayers/nn-d3d10sdklayers-id3d10infoqueue) per negare il messaggio D3D10 \_ MESSAGE ID DEVICE DRAW INDEX BUFFER TOO \_ \_ \_ \_ \_ \_ \_ SMALL.


```
  //retrieve the ID3D10InfoQueue from a Direct3D device created with the D3D10_CREATE_DEVICE_DEBUG flag
  ID3D10InfoQueue * pInfoQueue;
    g_pd3dDevice->QueryInterface( __uuidof(ID3D10InfoQueue),  (void **)&pInfoQueue );
    
  //set up the list of messages to filter
    D3D10_MESSAGE_ID messageIDs [] = { D3D10_MESSAGE_ID_DEVICE_DRAW_INDEX_BUFFER_TOO_SMALL };
    
  //set the DenyList to use the list of messages
    D3D10_INFO_QUEUE_FILTER filter = { 0 };
    filter.DenyList.NumIDs = 1;
    filter.DenyList.pIDList = messageIDs;
    
  //apply the filter to the info queue
    pInfoQueue->AddStorageFilterEntries( &filter );  
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Livelli API](d3d10-graphics-programming-guide-api-features-layers.md)
</dt> <dt>

[Funzionalità API (Direct3D 10)](d3d10-graphics-programming-guide-api-features.md)
</dt> </dl>

 

 




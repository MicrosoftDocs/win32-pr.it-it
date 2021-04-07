---
description: Personalizzare l'output di debug con ID3D10InfoQueue (Direct3D 10)
ms.assetid: 082c7783-c53a-4b73-b8f2-3f60e2c2689a
title: Personalizzare l'output di debug con ID3D10InfoQueue (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 843ac7dd34b19cfe1fc7835a2026ae2dd28b9dcd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049222"
---
# <a name="customize-debug-output-with-id3d10infoqueue-direct3d-10"></a>Personalizzare l'output di debug con ID3D10InfoQueue (Direct3D 10)

La coda di informazioni viene gestita da un'interfaccia (vedere [**interfaccia ID3D10InfoQueue**](/windows/desktop/api/D3D10SDKLayers/nn-d3d10sdklayers-id3d10infoqueue)) che archivia, recupera e filtra i messaggi di debug. La coda è costituita da una coda di messaggi, da uno stack di filtri di archiviazione facoltativo e da uno stack di filtri di recupero facoltativo. Lo stack del filtro di archiviazione può essere usato per filtrare i messaggi che si desidera archiviare. lo stack del filtro di recupero può essere utilizzato per filtrare i messaggi che si desidera archiviare. Dopo aver filtrato un messaggio, il messaggio verrà stampato nella finestra di debug e archiviato nello stack appropriato.

In generale:

-   Chiamare [**ID3D10InfoQueue:: AddApplicationMessage**](/windows/desktop/api/D3D10SDKLayers/nf-d3d10sdklayers-id3d10infoqueue-addapplicationmessage) per generare messaggi definiti dall'utente
-   La chiamata [**ID3D10InfoQueue:: GetMessage**](/windows/desktop/api/D3D10SDKLayers/nf-d3d10sdklayers-id3d10infoqueue-getmessage) viene utilizzata per ottenere i messaggi (che passano un filtro di recupero facoltativo).

## <a name="registry-controls"></a>Controlli registro di sistema

Usare le chiavi del registro di sistema per modificare le impostazioni di filtro, modificare i punti di rottura e disattivare l'output di debug. Il livello di debug verificherà questi percorsi per le chiavi del registro di sistema. verrà usato il primo percorso trovato.

1.  HKCU \\ software \\ Microsoft \\ Direct3D \\<sottochiave definita dall'utente>
2.  HKLM \\ software \\ Microsoft \\ Direct3D \\<sottochiave definita dall'utente>
3.  HKCU \\ software \\ Microsoft \\ Direct3D

Dove:

-   HKCU sta per l' \_ utente corrente di HKEY \_ e HKLM è il \_ computer locale HKEY \_ .
-   <sottochiave definita dall'utente> è un nome arbitrario per archiviare le impostazioni di debug per un'applicazione

### <a name="filtering-debug-messages-using-registry-keys"></a>Filtro dei messaggi di debug con chiavi del registro di sistema

Se il registro di sistema contiene una chiave InfoQueueStorageFilterOverride (e è diverso da zero), i messaggi (e l'output di debug) possono essere filtrati aggiungendo i controlli del registro di sistema seguenti.

-   Categoria silenziamento \_ DWORD \_ \* : output di debug se questa chiave è diversa da zero.
-   Gravità del silenziamento DWORD \_ \_ \* : l'output di debug è disabilitato se questa chiave è diversa da zero.
-   ID silenziamento \_ DWORD \_ \* : il nome o il numero del messaggio può essere usato per \* (proprio come per l' \_ ID BreakOn descritto in \_ \* precedenza). L'output di debug è disabilitato se questa chiave è diversa da zero.
-   Informazioni sulla gravità dello stato di inattivazione DWORD \_ \_ : l'output di debug è abilitato se questa chiave è diversa da zero. Per impostazione predefinita, quando InfoQueueStorageFilterOverride è abilitato, i messaggi di debug con informazioni di gravità vengono disabilitati. Pertanto, per questa chiave è possibile riattivare le informazioni.

Questi controlli modificano se un messaggio viene registrato o visualizzato; non influiscono sull'eventuale esito positivo o negativo di un'API.

### <a name="setting-break-conditions-using-registry-keys"></a>Impostazione delle condizioni di interruzioni tramite chiavi del registro di sistema

Le applicazioni possono essere forzate a interrompere un messaggio usando le seguenti chiavi del registro di sistema.

**EnableBreakOnMessage** : questa chiave consente di suddividere i messaggi (e determina l'Ignorazione delle impostazioni di SetBreakOnCategory ()/SetBreakOnSeverity ()/SetBreakOnID (). I messaggi effettivi da interrompere vengono definiti usando uno o più \_ \* valori BreakOn definiti di seguito.

-   **BreakOn \_ \_Categoria \** _-Interrompi in tutti i messaggi che passano attraverso i filtri di archiviazione. \_ è uno dei messaggi di \_ categoria del messaggio D3D10 \_ .
-   **BreakOn \_ \_Gravità \** _-Interrompi in tutti i messaggi che passano attraverso i filtri di archiviazione. \_ è uno dei messaggi di \_ gravità del messaggio D3D10 \_ \_ .
-   **BreakOn \_ \_ID \** _-Interrompi in tutti i messaggi che passano attraverso i filtri di archiviazione. \_ è uno dei \_ \_ messaggi ID messaggio D3D10 \_ o può essere il valore numerico dell'enumerazione Error. Si supponga, ad esempio, che il messaggio con ID "D3D10 \_ message \_ ID \_ ipotetico" disponga del valore 123 nell' \_ enumerazione D3D10 message \_ ID. In questo caso, la creazione del valore BreakOn \_ ID \_ ipotetico = 1 o BreakOn \_ ID \_ 123 = 1 avrebbe lo stesso risultato quando viene rilevato un messaggio con ID D3D10 \_ messaggio \_ ID \_ ipotetico.

### <a name="muting-debug-output-using-registry-keys"></a>Silenziamento dell'output di debug con chiavi del registro di sistema

L'output di debug può essere disattivato usando una chiave di MuteDebugOutput. La presenza di questo valore nel registro di sistema impone l'override del metodo [**ID3D10InfoQueue:: SetMuteDebugOutput**](/windows/desktop/api/D3D10SDKLayers/nf-d3d10sdklayers-id3d10infoqueue-setmutedebugoutput) di InfoQueue. MuteDebugOutput interrompe l'invio dei messaggi che passano il filtro di archiviazione all'output di debug.

## <a name="disabling-debug-layer-messages"></a>Disabilitazione dei messaggi del livello di debug

I messaggi del livello di debug possono essere disabilitati singolarmente o come gruppo in fase di esecuzione specificando filtri con [**ID3D10InfoQueue:: AddStorageFilterEntries**](/windows/desktop/api/D3D10SDKLayers/nf-d3d10sdklayers-id3d10infoqueue-addstoragefilterentries). L'argomento *pFilter* di **ID3D10InfoQueue:: AddStorageFilterEntries** accetta una struttura di filtro della [**\_ \_ coda \_ di informazioni D3D10**](/windows/desktop/api/d3d10sdklayers/ns-d3d10sdklayers-d3d10_info_queue_filter) che contiene un elenco Consenti e un elenco di accesso negato. Gli elenchi Consenti e nega sono descritti da [**D3D10 \_ info \_ Queue \_ Filter strutture \_ desc**](/windows/desktop/api/d3d10sdklayers/ns-d3d10sdklayers-d3d10_info_queue_filter_desc) che consentono di specificare il filtro in base a pullula, gravità e singolo ID messaggio.

Il codice seguente è un esempio di configurazione dell' [**interfaccia ID3D10InfoQueue**](/windows/desktop/api/D3D10SDKLayers/nn-d3d10sdklayers-id3d10infoqueue) per negare un messaggio di errore del buffer dell'indice del messaggio D3D10 message \_ ID del \_ \_ dispositivo \_ \_ \_ \_ \_ .


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

 

 




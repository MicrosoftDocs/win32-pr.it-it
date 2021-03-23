---
title: Usare eseguire per diagnosticare gli errori della GPU
description: Il dispositivo ha rimosso i dati estesi (eseguire) è un set di funzionalità di diagnostica in continua evoluzione progettato per identificare la cause di errori imprevisti di rimozione del dispositivo.
ms.custom: 19H1
ms.localizationpriority: high
ms.topic: article
ms.date: 04/19/2019
ms.openlocfilehash: bbc754239210899e804d41a294e8c9f47967fb25
ms.sourcegitcommit: 780d4b1601c45658ef0b799b80d13f45a53d808d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/26/2020
ms.locfileid: "104548811"
---
# <a name="use-dred-to-diagnose-gpu-faults"></a>Usare eseguire per diagnosticare gli errori della GPU
ESEGUIRE sta per i dati estesi del dispositivo rimossi. ESEGUIRE è un set di funzionalità di diagnostica in evoluzione progettato per facilitare l'identificazione della cause di errori imprevisti di rimozione dei dispositivi. Nell'hardware che supporta le funzionalità necessarie (come definito di seguito), eseguire offre la navigazione automatica, nonché la segnalazione degli errori di pagina GPU.

## <a name="auto-breadcrumbs"></a>Percorsi di navigazione automatici
Per impostare la scena per la navigazione automatica, è necessario accennare alla varietà manuale. Per tenere traccia dello stato di avanzamento della GPU, è possibile usare il [Metodo ID3D12GraphicsCommandList2:: WriteBufferImmediate](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist2-writebufferimmediate) per inserire i percorsi di *navigazione* nel flusso di comandi della GPU, in previsione dell'eventuale [rilevamento e ripristino del timeout](/windows-hardware/drivers/display/timeout-detection-and-recovery).

Si tratta di un approccio ragionevole se si vuole creare un'implementazione personalizzata con sovraccarico ridotto. Potrebbe tuttavia mancare la versatilità di una soluzione standardizzata, ad esempio le estensioni del debugger o la creazione di report tramite [segnalazione errori Windows (WER)](/windows/desktop/wer/windows-error-reporting) , nota anche come Watson.

Quindi, i percorsi automatici di eseguire chiamano **WriteBufferImmediate** per inserire i contatori di stato nel flusso di comandi della GPU. ESEGUIRE inserisce un percorso di navigazione dopo ogni operazione di *rendering,* &mdash; ovvero ogni operazione che comporta il lavoro della GPU, ad esempio **disegnare**, **inviare**, **copiare**, **risolvere** e altro ancora. Se il dispositivo viene rimosso al centro di un carico di lavoro GPU, il valore di navigazione eseguire è essenzialmente una raccolta di operazioni di rendering completate prima dell'errore.

Il buffer circolare della cronologia di navigazione mantiene le operazioni 64KB in un elenco di comandi specificato. Se sono presenti più di 65536 operazioni in un elenco di comandi, solo le ultime operazioni 64KB vengono archiviate per &mdash; prima cosa sovrascrivendo le operazioni meno recenti. Tuttavia, il valore del contatore di navigazione continua a contare fino a `UINT_MAX` . Pertanto, LastOpIndex = (BreadcrumbCount-1) %65536.

ESEGUIRE 1,0 è stato disponibile per la prima volta in Windows 10, versione 1809 (aggiornamento di Windows 10 ottobre 2018) ed espone il rudimentale spostamento automatico. Tuttavia, non sono presenti API per l'IT e l'unico modo per abilitare eseguire 1,0 consiste nell'usare l' **Hub di feedback** per acquisire una riproduzione TDR (riproduzione) per le **app & giochi** e la compatibilità dei giochi di \> **gioco**. Lo scopo principale di eseguire 1,0 è stato quello di aiutare la causa principale dell'analisi degli arresti anomali del gioco tramite commenti dei clienti.
### <a name="caveats"></a>Precisazioni
- Poiché una GPU è molto pipeline, non c'è alcuna garanzia che il contatore di navigazione indichi l'esatta operazione non riuscita. In alcuni dispositivi di rendering posticipati basati sul riquadro è infatti possibile che il contatore di navigazione sia una risorsa completa o una barriera di visualizzazione accesso non ordinato (UAV) dietro lo stato della GPU effettivo.
- Un driver di visualizzazione può riordinare i comandi, eseguire il recupero preliminare dall'area memoria della risorsa prima di eseguire un comando oppure svuotare bene la memoria memorizzata nella cache dopo il completamento di un comando. Uno di questi può produrre un errore della GPU. In questi casi, i contatori di navigazione automatica possono risultare meno utili o fuorvianti.
### <a name="performance"></a>Prestazioni
Sebbene i percorsi di navigazione automatica siano progettati per un sovraccarico ridotto, non sono gratuiti. Le misurazioni empiriche mostrano un calo delle prestazioni del 2-5% in un tipico motore di gioco di grafica AAA Direct3D 12. Per questo motivo, la navigazione automatica è disattivata per impostazione predefinita.
### <a name="hardware-requirements"></a>Requisiti hardware
Poiché i valori del contatore di navigazione devono essere conservati dopo la rimozione del dispositivo, la risorsa che contiene i percorsi di navigazione deve esistere nella memoria di sistema e deve essere mantenuta in caso di rimozione del dispositivo. Questo significa che il driver di visualizzazione deve supportare [**D3D12_FEATURE_EXISTING_HEAPS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_feature). Fortunatamente, questo è il caso per la maggior parte dei driver di visualizzazione di Direct3D 12 in Windows 10, versione 1903.
## <a name="gpu-page-fault-reporting"></a>Segnalazione errori pagina GPU
Una funzionalità nuova per eseguire 1,1 è la segnalazione degli errori di pagina GPU di eseguire. Un errore di pagina GPU si verifica in genere in una di queste condizioni.

1. Un'applicazione esegue erroneamente il lavoro sulla GPU che fa riferimento a un oggetto eliminato. Questo è uno dei motivi principali per una rimozione imprevista del dispositivo.
2. Un'applicazione esegue erroneamente il lavoro sulla GPU che accede a una risorsa rimossa o a un riquadro non residente.
3. Uno shader fa riferimento A un descrittore non inizializzato o non aggiornato.
3. Indici shader oltre la fine di un'associazione radice.

ESEGUIRE tenta di risolvere alcuni di questi scenari segnalando i nomi e i tipi di oggetti API esistenti o recentemente liberati che corrispondono all'indirizzo virtuale (VA) dell'errore di pagina segnalato dalla GPU.

### <a name="caveat"></a>Avviso
Non tutte le GPU supportano errori di pagina (sebbene molte operazioni). Alcune GPU rispondono a errori di memoria per: Scritture di bit-bucket; lettura di dati simulati (ad esempio, zeri); o semplicemente sospesi. Sfortunatamente, nei casi in cui la GPU non si blocca immediatamente, il [rilevamento e il ripristino del timeout](/windows-hardware/drivers/display/timeout-detection-and-recovery) possono verificarsi in un secondo momento nella pipe, rendendo ancora più difficile l'individuazione della causa radice.

### <a name="performance"></a>Prestazioni
Il runtime di Direct3D 12 deve curare attivamente una raccolta di oggetti API esistenti e eliminati di recente indicizzabili dall'indirizzo virtuale (VA). In questo modo si aumenta l'overhead della memoria di sistema e si introduce un lieve impatto sulle prestazioni per la creazione e la distruzione di oggetti. Per questo motivo, questo comportamento è disattivato per impostazione predefinita.

### <a name="hardware-requirements"></a>Requisiti hardware
Una GPU che non supporta errori di pagina può comunque trarre vantaggio dalla funzionalità di navigazione automatica.

## <a name="setting-up-dred-in-code"></a>Configurazione di eseguire nel codice
Le impostazioni di eseguire sono globali per il processo ed è necessario configurarle prima di creare un dispositivo Direct3D 12. A tale scopo, chiamare la funzione [**D3D12GetDebugInterface**](/windows/desktop/api/d3d12/nf-d3d12-d3d12getdebuginterface) per recuperare un [**ID3D12DeviceRemovedExtendedDataSettings**](/windows/desktop/api/d3d12/nn-d3d12-id3d12deviceremovedextendeddatasettings).

```cpp
CComPtr<ID3D12DeviceRemovedExtendedDataSettings> pDredSettings;
VERIFY_SUCCEEDED(D3D12GetDebugInterface(IID_PPV_ARGS(&pDredSettings)));

// Turn on auto-breadcrumbs and page fault reporting.
pDredSettings->SetAutoBreadcrumbsEnablement(D3D12_DRED_ENABLEMENT_FORCED_ON);
pDredSettings->SetPageFaultEnablement(D3D12_DRED_ENABLEMENT_FORCED_ON);
```

> [!NOTE]
> Le modifiche alle impostazioni di eseguire non hanno alcun effetto sui dispositivi già creati. Tuttavia, le chiamate successive a [**D3D12CreateDevice**](/windows/desktop/api/d3d12/nf-d3d12-d3d12createdevice) usano le impostazioni eseguire più recenti.

## <a name="accessing-dred-data-in-code"></a>Accesso ai dati di eseguire nel codice
Una volta rilevata la rimozione del dispositivo (ad esempio, **present** restituisce [**DXGI_ERROR_DEVICE_REMOVED**](/windows/desktop/com/com-error-codes-10)), usare i metodi dell'interfaccia [**ID3D12DeviceRemovedExtendedData**](/windows/desktop/api/d3d12/nn-d3d12-id3d12deviceremovedextendeddata) per accedere ai dati di eseguire per il dispositivo rimosso.

Per recuperare l'interfaccia **ID3D12DeviceRemovedExtendedData** , chiamare [QueryInterface](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(refiid_void)) su un'interfaccia [ID3D12Device](/windows/win32/api/d3d12/nn-d3d12-id3d12device) (o derivata), passando l'identificatore di interfaccia (IID) di **ID3D12DeviceRemovedExtendedData**.

```cpp
void MyDeviceRemovedHandler(ID3D12Device * pDevice)
{
    CComPtr<ID3D12DeviceRemovedExtendedData> pDred;
    VERIFY_SUCCEEDED(pDevice->QueryInterface(IID_PPV_ARGS(&pDred)));
    D3D12_DRED_AUTO_BREADCRUMBS_OUTPUT DredAutoBreadcrumbsOutput;
    D3D12_DRED_PAGE_FAULT_OUTPUT DredPageFaultOutput;
    VERIFY_SUCCEEDED(pDred->GetAutoBreadcrumbsOutput(&DredAutoBreadcrumbsOutput));
    VERIFY_SUCCEEDED(pDred->GetPageFaultAllocationOutput(&DredPageFaultOutput));
    // Custom processing of DRED data can be done here.
    // Produce telemetry...
    // Log information to console...
    // break into a debugger...
}
```

## <a name="debugger-access-to-dred"></a>Accesso del debugger a eseguire
I debugger hanno accesso ai dati di eseguire tramite **d3d12!** Esportazione dei dati D3D12DeviceRemovedExtendedData.

## <a name="dred-telemetry"></a>Telemetria eseguire
L'applicazione può usare le API eseguire per controllare le funzionalità di eseguire e raccogliere dati di telemetria per consentire l'analisi dei problemi. In questo modo si ottiene una rete molto più ampia per intercettare i TDRs di difficile riproduzione.

A partire da Windows 10, versione 1903, tutti gli eventi rimossi dal dispositivo in modalità utente vengono segnalati a [segnalazione errori Windows (WER)](/windows/desktop/wer/windows-error-reporting), noto anche come Watson. Se una particolare combinazione di applicazione, GPU e driver di visualizzazione genera un numero sufficiente di eventi rimossi dal dispositivo, è possibile che eseguire sia temporaneamente abilitato per i clienti che avviano la stessa applicazione in una configurazione simile.

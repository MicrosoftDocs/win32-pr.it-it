---
title: Usare DRED per diagnosticare gli errori GPU
description: Device Removed Extended Data (DRED) è un set in evoluzione di funzionalità di diagnostica progettate per identificare la causa di errori imprevisti di rimozione del dispositivo.
ms.custom: 19H1
ms.localizationpriority: high
ms.topic: article
ms.date: 04/19/2019
ms.openlocfilehash: ecb18b81107123564e265e49fad61c004b17938f732b373311743bf64bd92fab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118097645"
---
# <a name="use-dred-to-diagnose-gpu-faults"></a>Usare DRED per diagnosticare gli errori GPU
DRED è l'acronimo di Device Removed Extended Data. DRED è un set in evoluzione di funzionalità di diagnostica progettate per identificare la causa di errori imprevisti di rimozione dei dispositivi. Nell'hardware che supporta le funzionalità necessarie (come definito di seguito), DRED offre breadcrumb automatici e la segnalazione degli errori di pagina GPU.

## <a name="auto-breadcrumbs"></a>Navigazione automatica
Per impostare la scena per le opzioni di navigazione automatica, è prima necessario menzionare la varietà manuale. In previsione dell'eventualità di un rilevamento e ripristino del [timeout (TDR, Timeout Detection and Recovery),](/windows-hardware/drivers/display/timeout-detection-and-recovery)è possibile usare  il metodo [ID3D12GraphicsCommandList2::WriteBufferImmediate](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist2-writebufferimmediate) per inserire le opzioni di navigazione nel flusso di comandi GPU, per tenere traccia dello stato di avanzamento della GPU.

Si tratta di un approccio ragionevole se si vuole creare un'implementazione personalizzata a basso sovraccarico. Potrebbe tuttavia mancare una certa versatilità di una soluzione standardizzata, ad esempio le estensioni del debugger o la creazione di report [tramite Segnalazione errori Windows (WER)](/windows/desktop/wer/windows-error-reporting) (noto anche come Watson).

Pertanto, gli strumenti di navigazione automatica di DRED chiamano **WriteBufferImmediate** per inserire i contatori di stato nel flusso di comandi GPU. DRED inserisce una barra di navigazione dopo ogni operazione di rendering, ovvero ogni operazione che comporta il funzionamento della GPU , ad esempio &mdash; **Draw**, **Dispatch**, **Copy**, **Resolve** e altre. Se il dispositivo viene rimosso nel mezzo di un carico di lavoro GPU, il valore di navigazione DRED è essenzialmente una raccolta delle operazioni di rendering completate prima dell'errore.

Il buffer circolare della cronologia di navigazione mantiene fino a 64 Operazioni DiB in un determinato elenco di comandi. Se in un elenco di comandi sono presenti più di 65536 operazioni, vengono archiviate prima solo le ultime 64 operazioni DiB sovrascrivendo le operazioni meno &mdash; recenti. Tuttavia, il valore del contatore breadcrumb continua a contare fino a `UINT_MAX` . LastOpIndex = (BreadcrumbCount - 1) % 65536.

DRED 1.0 è stato disponibile per la prima volta in Windows 10, versione 1809 (Aggiornamento di Windows 10 (ottobre 2018)) ed è stato esposto il percorso di navigazione automatico rudimentale. Tuttavia, non esistevano API e l'unico modo per abilitare DRED 1.0 era usare **Hub di Feedback** per acquisire una riproduzione TDR (repro) per le app **& Games Game** Performance and \> **Compatibility**. Lo scopo principale di DRED 1.0 era aiutare ad analizzare gli arresti anomali del gioco tramite commenti e suggerimenti dei clienti.
### <a name="caveats"></a>Precisazioni
- Poiché una GPU è molto pipeline, non esiste alcuna garanzia che il contatore breadcrumb indichi l'operazione esatta che ha avuto esito negativo. In alcuni dispositivi di rendering posticipati basati su riquadri è infatti possibile che il contatore breadcrumb sia una risorsa completa o una barriera di visualizzazione di accesso non ordinato dietro lo stato effettivo della GPU.
- Un driver di visualizzazione può riordinare i comandi, pre-recuperare dalla memoria delle risorse prima di eseguire un comando o scaricare la memoria memorizzata nella cache subito dopo il completamento di un comando. Uno di questi elementi può generare un errore GPU. In questi casi, i contatori con navigazione automatica possono essere meno utili o fuorvianti.
### <a name="performance"></a>Prestazioni
Anche se gli breadcrumb automatici sono progettati per essere a basso sovraccarico, non sono gratuiti. Le misurazioni empiriche mostrano una perdita di prestazioni del 2-5% in un tipico motore di gioco di grafica AAA Direct3D 12. Per questo motivo, le opzioni di navigazione automatica sono disattivate per impostazione predefinita.
### <a name="hardware-requirements"></a>Requisiti hardware
Poiché i valori del contatore breadcrumb devono essere mantenuti dopo la rimozione del dispositivo, la risorsa che contiene breadcrumb deve esistere nella memoria di sistema e deve essere mantenuta in caso di rimozione del dispositivo. Ciò significa che il driver di visualizzazione deve supportare [**D3D12_FEATURE_EXISTING_HEAPS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_feature). Fortunatamente, questo è il caso della maggior parte dei driver di visualizzazione Direct3D 12 Windows 10 versione 1903.
## <a name="gpu-page-fault-reporting"></a>Segnalazione degli errori di pagina GPU
Una funzionalità nuova per DRED 1.1 è la segnalazione degli errori di pagina DRED GPU. Un errore di pagina GPU si verifica in genere in una di queste condizioni.

1. Un'applicazione esegue erroneamente il lavoro sulla GPU che fa riferimento a un oggetto eliminato. Questo è uno dei motivi principali per cui si verifica una rimozione imprevista del dispositivo.
2. Un'applicazione esegue erroneamente il lavoro sulla GPU che accede a una risorsa sfrattata o a un riquadro non residente.
3. Uno shader fa riferimento a un descrittore non inizializzato o non obsoleto.
3. Uno shader indicizza oltre la fine di un'associazione radice.

DRED tenta di risolvere alcuni di questi scenari segnalando i nomi e i tipi di qualsiasi oggetto API esistente o liberato di recente che corrisponde all'indirizzo virtuale dell'errore di pagina segnalato dalla GPU.

### <a name="caveat"></a>Avviso
Non tutte le GPU supportano gli errori di pagina (anche se molti lo fanno). Alcune GPU rispondono agli errori di memoria in base a: scritture di bucket di bit; lettura di dati simulati (ad esempio, zeri); o semplicemente impiccando. Sfortunatamente, nei casi in cui la GPU non si blocca immediatamente, un timeout di rilevamento e ripristino [(TDR)](/windows-hardware/drivers/display/timeout-detection-and-recovery) può verificarsi in un secondo momento nella pipe, rendendo ancora più difficile individuare la causa radice.

### <a name="performance"></a>Prestazioni
Il runtime Direct3D 12 deve curare attivamente una raccolta di oggetti API esistenti e eliminati di recente indicizzabili in base all'indirizzo virtuale (VA). Ciò aumenta il sovraccarico della memoria di sistema e introduce un piccolo miglioramento delle prestazioni per la creazione e la distruzione di oggetti. Per questo motivo, questo comportamento è disattivato per impostazione predefinita.

### <a name="hardware-requirements"></a>Requisiti hardware
Una GPU che non supporta l'errore di pagina può comunque trarre vantaggio dalla funzionalità di navigazione automatica.

## <a name="setting-up-dred-in-code"></a>Configurazione di DRED nel codice
Le impostazioni DRED sono globali per il processo ed è necessario configurarle prima di creare un dispositivo Direct3D 12. A tale scopo, chiamare la [**funzione D3D12GetDebugInterface**](/windows/desktop/api/d3d12/nf-d3d12-d3d12getdebuginterface) per recuperare un [**ID3D12DeviceRemovedExtendedDataSettings.**](/windows/desktop/api/d3d12/nn-d3d12-id3d12deviceremovedextendeddatasettings)

```cpp
CComPtr<ID3D12DeviceRemovedExtendedDataSettings> pDredSettings;
VERIFY_SUCCEEDED(D3D12GetDebugInterface(IID_PPV_ARGS(&pDredSettings)));

// Turn on auto-breadcrumbs and page fault reporting.
pDredSettings->SetAutoBreadcrumbsEnablement(D3D12_DRED_ENABLEMENT_FORCED_ON);
pDredSettings->SetPageFaultEnablement(D3D12_DRED_ENABLEMENT_FORCED_ON);
```

> [!NOTE]
> Le modifiche alle impostazioni DRED non hanno alcun effetto sui dispositivi già creati. Ma le chiamate successive [**a D3D12CreateDevice**](/windows/desktop/api/d3d12/nf-d3d12-d3d12createdevice) usano le impostazioni DRED più recenti.

## <a name="accessing-dred-data-in-code"></a>Accesso ai dati DRED nel codice
Dopo aver rilevato la rimozione del dispositivo (ad esempio, **Present** restituisce [**DXGI_ERROR_DEVICE_REMOVED**](/windows/desktop/com/com-error-codes-10)), usare i metodi dell'interfaccia [**ID3D12DeviceRemovedExtendedData**](/windows/desktop/api/d3d12/nn-d3d12-id3d12deviceremovedextendeddata) per accedere ai dati dred per il dispositivo rimosso.

Per recuperare **l'interfaccia ID3D12DeviceRemovedExtendedData,** chiamare [QueryInterface](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(refiid_void)) su [un'interfaccia ID3D12Device](/windows/win32/api/d3d12/nn-d3d12-id3d12device) (o derivata), passando l'identificatore di interfaccia (IID) **di ID3D12DeviceRemovedExtendedData.**

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

## <a name="debugger-access-to-dred"></a>Accesso del debugger a DRED
I debugger hanno accesso ai dati DRED tramite **d3d12! Esportazione dei dati D3D12DeviceRemovedExtendedData.**

## <a name="dred-telemetry"></a>Telemetria DRED
L'applicazione può usare le API DRED per controllare le funzionalità dred e raccogliere dati di telemetria per analizzare i problemi. Ciò offre una rete molto più ampia per intercettare i TDR difficili da riprodurre.

A Windows 10 versione 1903, tutti gli eventi rimossi dal dispositivo in modalità utente vengono segnalati a [Segnalazione errori Windows (WER),](/windows/desktop/wer/windows-error-reporting)noto anche come Watson. Se una particolare combinazione di applicazione, GPU e driver video genera un numero sufficiente di eventi rimossi dal dispositivo, è possibile che DRED venga abilitato temporaneamente per i clienti che avviano la stessa applicazione in una configurazione simile.

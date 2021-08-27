---
title: API PAM
description: L'API Windows Filtering Platform (WFP) è suddivisa nei componenti seguenti.
ms.assetid: ff3f0d74-7e0b-4a3e-b66d-eaa61b89038a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9eadbb3fb6383999b2bb8ef14c99ecb8beab3f88
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122470148"
---
# <a name="wfp-api"></a>API PAM

L'API Windows Filtering Platform (WFP) è suddivisa nei componenti seguenti.




| Componente | Descrizione | File di intestazione | 
|-----------|-------------|--------------|
| <a href="/windows-hardware/drivers/ddi/_netvista/">API callout</a> (FWPS)${REMOVE}$<br /> | <a href="/windows-hardware/drivers/ddi/_netvista/">Tipi di</a> dati utilizzati dai callout. <strong>Nota</strong>  Questi tipi di dati sono documentati in Microsoft Windows Driver Development Kit (DDK).<br /> | <dl> fwpstypes.h<br />fwpstypes.idl<br /></dl> | 
| <a href="/windows-hardware/drivers/ddi/_netvista/">Funzioni</a> e <a href="/windows-hardware/drivers/ddi/_netvista/">tipi enumerati usati</a> per implementare i callout. <strong>Nota</strong>  Queste funzioni e i tipi enumerati sono documentati in DDK.<br /> | <dl> fwpsu.h<br />fwpsk.h<br /></dl> | 
| API IKE/AuthIP (IKEEXT)${REMOVE}$<br /> | <a href="fwp-enums.md">Tipi enumerati</a> e <a href="fwp-structs.md">strutture usati</a> per la gestione di associazioni di sicurezza e criteri in modalità principale IKE e AuthIP. | <dl> iketypes.h<br />iketypes.idl<br /></dl> | 
| <a href="fwp-ike-functions.md">Funzioni</a> usate per la gestione di associazioni di sicurezza e criteri IKE e AuthIP MM. | <dl> fwpmu.h<br />fwpmk.h<br /></dl> | 
| API IPsec (IPSEC)${REMOVE}$<br /> | <a href="fwp-enums.md">Tipi enumerati</a> e <a href="fwp-structs.md">strutture utilizzati</a> per la gestione dei criteri IPsec e delle associazioni di sicurezza. | <dl> ipsectypes.h<br />ipsectypes.idl<br /></dl> | 
| <a href="fwp-ipsec-functions.md">Funzioni</a> utilizzate per la gestione dei criteri IPsec e delle associazioni di sicurezza. | <dl> fwpmu.h<br />fwpmk.h<br /></dl> | 
| API Gestione (FWPM)${REMOVE}$<br /> | <a href="fwp-enums.md">Tipi enumerati</a> e <a href="fwp-structs.md">strutture utilizzati</a> per la gestione del motore di filtro. | <dl> fwpmtypes.h<br />fwpmtypes.idl<br /></dl> | 
| <a href="fwp-mgmt-functions.md">Funzioni</a> utilizzate per la gestione del motore di filtro. Queste funzioni vengono usate per eseguire le attività seguenti:<br /><ul><li>Impostare ed eseguire query su filtri, provider e callout.</li><li>Recuperare le statistiche IPsec.</li><li>Configurare la Windows di filtro dei dati.</li></ul> | <dl> fwpmu.h<br />fwpmk.h<br /></dl> | 
| API condivisa (FWP) | Tipi <a href="fwp-enums.md">e strutture enumerati</a> <a href="fwp-structs.md">fondamentali condivisi</a> in Windows Filtering Platform. | <dl> fwptypes.h<br />fwptypes.idl<br /></dl> | 




 

I nomi dei tipi di dati sono tutti delimitati da lettere maiuscole e caratteri di sottolineatura. Il nome inizia sempre con un prefisso che identifica il gruppo di componenti, ad esempio [**FWPM \_ PROVIDER0.**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_provider0)

I nomi delle funzioni sono con distinzione tra maiuscole e minuscole e tra maiuscole e minuscole. Il nome inizia sempre con un prefisso che identifica il gruppo di componenti, ad esempio [**FwpmProviderContextAdd0.**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmprovidercontextadd0)

La maggior parte dei nomi di dati e funzioni termina con un numero di versione. Il file di intestazione fwpvi.h esegue il mapping dei nomi di funzioni e dati indipendenti dalla versione alla versione appropriata per l'uso con un determinato sistema operativo. Per altre informazioni, vedere [l'Version-Independent e le versioni](wfp-version-independent-names-and-targeting-specific-versions-of-windows.md)specifiche di Windows .

Ogni componente non è autonomo. Ad esempio, i criteri della modalità principale (MM) IKE sono definiti nel componente IKEEXT, ma vengono archiviati in un contesto del provider e sono associati a un filtro che si trovano entrambi nel componente API FWPM.

## <a name="user-mode-and-kernel-mode-public-header-files"></a>User-Mode e Kernel-Mode di intestazione pubblica

La maggior parte delle funzioni WFP può essere chiamata dalla modalità utente o dalla modalità kernel. Tuttavia, le funzioni in modalità utente restituiscono un valore **DWORD** che rappresenta un codice di errore Win32, mentre le funzioni in modalità kernel restituiscono un **valore NTSTATUS** che rappresenta un codice di stato NT. Di conseguenza, i nomi e la semantica delle funzioni sono identici tra la modalità utente e la modalità kernel, ma le firme delle funzioni non lo sono. Questa operazione richiede intestazioni specifiche della modalità utente e della modalità kernel separate per i prototipi di funzione. I nomi dei file di intestazione in modalità utente terminano con "u" e i nomi dei file di intestazione in modalità kernel terminano con "k".

Nella tabella seguente sono elencati i file di intestazione Win32 che definiscono le funzioni WFP.

| File di intestazione | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|--------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| fwpmk.h      | Prototipi di funzioni in modalità kernel per i componenti FWPM, IPsec e IKEEXT. Disponibile solo nel DDK.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| fwpmu.h      | Prototipi di funzioni in modalità utente per i componenti FWPM, IPsec e IKEEXT. Disponibile solo in Microsoft Windows Software Development Kit (SDK).                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| fwpsk.h      | Prototipi di funzioni in modalità kernel e tipi enumerati per il componente FWPS. Disponibile solo nel DDK.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| fwpsu.h      | Prototipi di funzioni in modalità utente e tipi enumerati per il componente FWPS. Disponibile solo in Windows SDK. **Nota**  I tipi enumerati FWPS in modalità utente sono identici ai tipi enumerati FWPS in modalità kernel. Di conseguenza, questi tipi sono documentati solo nel DDK.<br/> **Nota**  I prototipi di funzione FWPS in modalità utente sono identici ai prototipi di funzione FWPS in modalità kernel, ad eccezione del codice restituito. Le funzioni FWPS in modalità utente restituiscono **un valore DWORD**, mentre le funzioni FWPS in modalità kernel restituiscono **ntSTATUS.** Di conseguenza, queste funzioni sono documentate solo nel DDK.<br/> |



 

Tutte le funzioni in modalità utente vengono esportate da fwpuclnt.dll. Tutte le funzioni in modalità kernel vengono esportate da fwpkclnt.sys.

### <a name="management-fwpm-and-callout-fwps-data-types"></a>Tipi di dati di gestione (FWPM) e callout (FWPS)

La maggior parte dei tipi di dati FWPM, usati per attività di gestione come l'aggiunta di filtri o callout da un'applicazione o un driver, ha controparti FWPS. I tipi di dati FWPS vengono usati durante il filtraggio effettivo del traffico di rete, nel contesto di una routine di callout per la classificazione.

Ad esempio, per aggiungere un filtro a un determinato livello del motore di filtro, il programmatore deve usare un tipo FWPM, ad esempio: `filter.layerKey = FWPM_LAYER_INBOUND_IPPACKET` . Per controllare il livello da cui viene chiamato un callout, il programmatore deve usare il tipo FWPS corrispondente: ` if (inFixedValues->layerId == FWPS_LAYER_INBOUND_IPPACKET)` .

Alcune controparti FWPS ai tipi di dati FWPM stanno espandendo i tipi di dati FWPM originali. Ad esempio, per aggiungere una condizione di filtro a molti livelli del motore di filtro, il programmatore specifica indipendentemente dal `filterCondition.fieldKey = FWPM_CONDITION_IP_PROTOCOL` livello del motore di filtro. Per trovare un valore di condizione di filtro, il programmatore specifica un tipo FWPS specifico del livello, ad esempio: `inFixedValues->incomingValue[FWPS_FIELD_ALE_FLOW_ESTABLISHED_V4_IP_PROTOCOL]` .

I tipi di dati FWPS sono in genere più piccoli rispetto alle controparti FWPM. Ad esempio, gli identificatori del livello di filtro [**FWPM**](management-filtering-layer-identifiers-.md) sono **GUID**(16 byte), mentre gli identificatori del livello di filtro [FWPS](/windows-hardware/drivers/network/management-filtering-layer-identifiers) **sono UINT16** (16 bit). Le dimensioni minori per i tipi di dati FWPS migliorano le prestazioni del sistema poiché i confronti di interi superano i **confronti di GUID** per il traffico in tempo reale. Inoltre, la memoria del kernel viene usata in modo efficiente perché i tipi FWPS vengono tutti usati nel kernel per la gestione dei filtri, mentre i tipi FWPM vengono archiviati in modalità utente per gestire i diversi livelli.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Modello a oggetti dell'API PAM](object-model.md)
</dt> <dt>

[Gestione oggetti dell'API PAM](object-management.md)
</dt> </dl>


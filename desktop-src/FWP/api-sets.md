---
title: API PAM
description: L'API Windows Filtering Platform (WFP) è divisa nei componenti seguenti.
ms.assetid: ff3f0d74-7e0b-4a3e-b66d-eaa61b89038a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4230c82105f85c36e6fb112508a7128758b2ad60
ms.sourcegitcommit: db89157e3be911fdce2e543e99faa31fb2403bc8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/18/2020
ms.locfileid: "106300720"
---
# <a name="wfp-api"></a>API PAM

L'API Windows Filtering Platform (WFP) è divisa nei componenti seguenti.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Componente</th>
<th>Descrizione</th>
<th>File di intestazione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td rowspan="2"><a href="/windows-hardware/drivers/ddi/_netvista/">API callout</a> (FWPS) $ {Remove} $<br />
</td>
<td><a href="/windows-hardware/drivers/ddi/_netvista/">Tipi di dati</a> utilizzati dai callout. <strong>Nota</strong>  Questi tipi di dati sono documentati in Microsoft Windows Driver Development Kit (DDK).<br/></td>
<td><dl> fwpstypes. h<br />
fwpstypes. idl<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="/windows-hardware/drivers/ddi/_netvista/">Funzioni</a> e <a href="/windows-hardware/drivers/ddi/_netvista/">tipi enumerati</a> usati per implementare i callout. <strong>Nota</strong>  Queste funzioni e i tipi enumerati sono documentati in DDK.<br/></td>
<td><dl> fwpsu. h<br />
fwpsk. h<br />
</dl></td>

</tr>
<tr class="odd">
<td rowspan="2">API IKE/AuthIP (IKEEXT) $ {REMOVE} $<br />
</td>
<td><a href="fwp-enums.md">Tipi enumerati</a> e <a href="fwp-structs.md">strutture</a> usati per gestire le associazioni di sicurezza e i criteri della modalità principale IKE e AuthIP (mm).</td>
<td><dl> iketypes. h<br />
iketypes. idl<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="fwp-ike-functions.md">Funzioni</a> usate per gestire i criteri e le associazioni di sicurezza di IKE e AuthIP mm.</td>
<td><dl> fwpmu. h<br />
fwpmk. h<br />
</dl></td>

</tr>
<tr class="odd">
<td rowspan="2">API IPsec (IPSEC) $ {REMOVE} $<br />
</td>
<td><a href="fwp-enums.md">Tipi enumerati</a> e <a href="fwp-structs.md">strutture</a> utilizzati per gestire i criteri IPSec e le associazioni di sicurezza.</td>
<td><dl> ipsectypes. h<br />
ipsectypes. idl<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="fwp-ipsec-functions.md">Funzioni</a> utilizzate per gestire i criteri IPSec e le associazioni di sicurezza.</td>
<td><dl> fwpmu. h<br />
fwpmk. h<br />
</dl></td>

</tr>
<tr class="odd">
<td rowspan="2">API di gestione (FWPM) $ {REMOVE} $<br />
</td>
<td><a href="fwp-enums.md">Tipi enumerati</a> e <a href="fwp-structs.md">strutture</a> utilizzati per gestire il motore di filtro.</td>
<td><dl> fwpmtypes. h<br />
fwpmtypes. idl<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="fwp-mgmt-functions.md">Funzioni</a> utilizzate per gestire il motore di filtro. Queste funzioni vengono usate per eseguire le attività seguenti:<br/>
<ul>
<li>Set ed esecuzione di query su filtri, provider e callout.</li>
<li>Recuperare le statistiche IPsec.</li>
<li>Configurare la piattaforma filtro Windows.</li>
</ul></td>
<td><dl> fwpmu. h<br />
fwpmk. h<br />
</dl></td>

</tr>
<tr class="odd">
<td>API condivisa (FWP)</td>
<td><a href="fwp-enums.md">Tipi enumerati</a> fondamentali e <a href="fwp-structs.md">strutture</a> condivise attraverso la piattaforma filtro Windows.</td>
<td><dl> fwptypes. h<br />
fwptypes. idl<br />
</dl></td>
</tr>
</tbody>
</table>



 

I nomi dei tipi di dati sono delimitati da caratteri maiuscoli e caratteri di sottolineatura. Il nome inizia sempre con un prefisso che identifica il gruppo di componenti, ad esempio [**FWPM \_ PROVIDER0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_provider0).

I nomi di funzione sono di combinazione tra maiuscole e minuscole. Il nome inizia sempre con un prefisso che identifica il gruppo di componenti, ad esempio [**FwpmProviderContextAdd0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmprovidercontextadd0).

La maggior parte dei nomi di funzione e di dati termina con un numero di versione. Il file di intestazione fwpvi. h esegue il mapping dei nomi delle funzioni e dei dati indipendenti dalla versione alla versione appropriata per l'uso con un determinato sistema operativo. Per ulteriori informazioni, vedere la pagina relativa ai [nomi Version-Independent WFP e alle versioni specifiche di Windows](wfp-version-independent-names-and-targeting-specific-versions-of-windows.md).

Ogni componente non è autonomo. Ad esempio, i criteri della modalità principale IKE (MM) sono definiti nel componente IKEEXT, ma vengono archiviati in un contesto del provider e sono associati a un filtro che si trovano nel componente API FWPM.

## <a name="user-mode-and-kernel-mode-public-header-files"></a>User-Mode e Kernel-Mode file di intestazione pubblica

La maggior parte delle funzioni PAM può essere chiamata dalla modalità utente o dalla modalità kernel. Tuttavia, le funzioni in modalità utente restituiscono un valore **DWORD** che rappresenta un codice di errore Win32, mentre le funzioni in modalità kernel restituiscono un valore **NTSTATUS** che rappresenta un codice di stato NT. Di conseguenza, i nomi di funzione e la semantica sono identici tra la modalità utente e la modalità kernel, ma le firme di funzione non lo sono. Questa operazione richiede intestazioni specifiche in modalità utente e kernel separate per i prototipi di funzione. I nomi dei file di intestazione in modalità utente terminano con "u" e i nomi dei file di intestazione in modalità kernel terminano con "k".

Nella tabella seguente sono elencati i file di intestazione Win32 che definiscono le funzioni Pam.

| File di intestazione | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|--------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| fwpmk. h      | Prototipi di funzioni in modalità kernel per i componenti FWPM, IPsec e IKEEXT. Disponibile solo nel DDK.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| fwpmu. h      | Prototipi di funzioni in modalità utente per i componenti FWPM, IPsec e IKEEXT. Disponibile solo in Microsoft Windows Software Development Kit (SDK).                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| fwpsk. h      | Prototipi di funzioni in modalità kernel e tipi enumerati per il componente FWPS. Disponibile solo nel DDK.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| fwpsu. h      | Prototipi di funzioni in modalità utente e tipi enumerati per il componente FWPS. Disponibile solo nel Windows SDK. **Nota**  I tipi enumerati FWPS in modalità utente sono identici ai tipi enumerati FWPS in modalità kernel. Di conseguenza, questi tipi sono documentati solo nel DDK.<br/> **Nota**  I prototipi di funzione FWPS in modalità utente sono identici ai prototipi di funzione FWPS in modalità kernel, ad eccezione del codice restituito. Le funzioni FWPS in modalità utente restituiscono un **valore DWORD**, mentre le funzioni FWPS in modalità kernel restituiscono un **NTSTATUS**. Di conseguenza, queste funzioni sono documentate solo nel DDK.<br/> |



 

Tutte le funzioni in modalità utente vengono esportate da fwpuclnt.dll. Tutte le funzioni in modalità kernel vengono esportate da fwpkclnt.sys.

### <a name="management-fwpm-and-callout-fwps-data-types"></a>Tipi di dati di gestione (FWPM) e callout (FWPS)

La maggior parte dei tipi di dati FWPM, usati per le attività di gestione, ad esempio l'aggiunta di filtri o callout da un'applicazione o un driver, hanno controparti FWPS. I tipi di dati FWPS vengono usati durante l'effettivo filtro del traffico di rete nel contesto di una routine di callout per la classificazione.

Per aggiungere un filtro a un determinato livello del motore di filtro, ad esempio, il programmatore deve usare un tipo FWPM, come: `filter.layerKey = FWPM_LAYER_INBOUND_IPPACKET` . Per verificare da quale livello viene chiamato un callout, il programmatore deve usare il tipo FWPS corrispondente: ` if (inFixedValues->layerId == FWPS_LAYER_INBOUND_IPPACKET)` .

Alcune controparti FWPS per i tipi di dati FWPM stanno espandendo i tipi di dati FWPM originali. Ad esempio, per aggiungere una condizione di filtro a molti livelli del motore di filtro, il programmatore specifica `filterCondition.fieldKey = FWPM_CONDITION_IP_PROTOCOL` indipendentemente dal livello del motore di filtraggio. Per trovare un valore della condizione di filtro, il programmatore specifica un tipo FWPS specifico del livello, ad esempio: `inFixedValues->incomingValue[FWPS_FIELD_ALE_FLOW_ESTABLISHED_V4_IP_PROTOCOL]` .

I tipi di dati FWPS sono in genere inferiori alle rispettive controparti FWPM. Ad esempio, gli [**identificatori del livello di filtro FWPM**](management-filtering-layer-identifiers-.md) sono **GUID** s (16 byte), mentre gli [identificatori del livello di filtro FWPS](/windows-hardware/drivers/network/management-filtering-layer-identifiers) sono **UInt16** (16 bit). Le dimensioni più piccole per i tipi di dati FWPS migliorano le prestazioni del sistema poiché i confronti integer superano i confronti **GUID** per il traffico in tempo reale Inoltre, la memoria del kernel viene usata in modo efficiente poiché i tipi FWPS sono tutti usati nel kernel per la gestione dei filtri, mentre i tipi FWPM vengono archiviati in modalità utente per gestire i diversi livelli.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Modello a oggetti dell'API WFP](object-model.md)
</dt> <dt>

[Gestione degli oggetti dell'API WFP](object-management.md)
</dt> </dl>


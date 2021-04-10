---
title: Configurazione del registro di sistema per le allocazioni delle porte e l'associazione selettiva
description: A partire da Windows 2000, per impostare le associazioni è necessario usare un'utilità nel Resource Kit di Windows denominata Rpccfg.exe. Per ulteriori informazioni, consultare il Resource Kit di Windows per la versione appropriata del sistema operativo.
ms.assetid: a33b51e7-2ded-46bd-aadb-27cbd99e1029
keywords:
- RPC, attività, configurazione del registro di sistema per le allocazioni delle porte e associazione selettiva
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ef1749fab1beb8e637d208a7d7af64577066fe6
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/08/2020
ms.locfileid: "103963534"
---
# <a name="configuring-the-registry-for-port-allocations-and-selective-binding"></a>Configurazione del registro di sistema per le allocazioni delle porte e l'associazione selettiva

A partire da Windows 2000, per impostare le associazioni è necessario usare un'utilità nel Resource Kit di Windows denominata Rpccfg.exe. Per ulteriori informazioni, consultare il Resource Kit di Windows per la versione appropriata del sistema operativo.

Per le versioni di Windows precedenti a Windows 2000, le chiavi del registro di sistema nella tabella seguente specificano le impostazioni predefinite del sistema per l'allocazione delle porte dinamiche e per l'associazione alle schede di rete nei computer multihomed. È necessario innanzitutto creare queste chiavi e quindi specificare le impostazioni appropriate.

L'utilizzo della funzione [**RpcServerUseProtseqEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqex) ha effetto su queste impostazioni. Gli sviluppatori devono avere familiarità con le impostazioni del registro di sistema descritte in questa sezione e la funzione **RpcServerUseProtseqEx** quando si gestiscono le allocazioni delle porte. Un esempio con tre applicazioni ipotetiche segue la tabella riportata di seguito e illustra il modo in cui queste impostazioni e la funzione **RpcServerUseProtseqEx** interagiscono.

Se manca una chiave o se contiene un valore non valido, l'intera configurazione viene contrassegnata come non valida e tutte le chiamate **RpcServerUseProtseq \*** su [**ncacn \_ IP \_ TCP**](/windows/desktop/Midl/ncacn-ip-tcp) o [**ncadg \_ \_ UDP**](/windows/desktop/Midl/ncadg-ip-udp) avranno esito negativo.

> [!Note]  
> Le porte allocate a un processo restano allocate fino al termine del processo. Se tutte le porte disponibili sono in uso, la funzione restituisce \_ le \_ risorse RPC esaurite \_ \_ .

 



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Chiave porta</th>
<th>Tipo di dati</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre data-space="preserve"><code>HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Rpc
            Internet
               Ports</code></pre></td>
<td><strong>REG_MULTI_SZ</strong></td>
<td>Specifica un set di intervalli di porte IP costituito da tutte le porte disponibili da Internet o da tutte le porte non disponibili in Internet. Ogni stringa rappresenta una singola porta o un set di porte inclusivo (ad esempio, 1000-1050, 1984). Se le voci non rientrano nell'intervallo compreso tra 0 e 65535 o se non è possibile interpretare una stringa, il tempo di esecuzione RPC considererà l'intera configurazione come non valida.</td>
</tr>
<tr class="even">
<td><pre data-space="preserve"><code>HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Rpc
            Internet
               PortsInternetAvailable</code></pre></td>
<td><strong>REG_SZ</strong></td>
<td>Y o N (senza distinzione tra maiuscole e minuscole). Se Y, le porte elencate nella chiave porte sono tutte le porte disponibili su Internet nel computer. Se N, le porte elencate nella chiave porte sono tutte le porte che non sono disponibili su Internet.</td>
</tr>
<tr class="odd">
<td><pre data-space="preserve"><code>HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Rpc
            Internet
               UseInternetPorts</code></pre></td>
<td><strong>REG_SZ</strong></td>
<td>Y o N (senza distinzione tra maiuscole e minuscole). Specifica i criteri predefiniti di sistema. Se Y, ai processi che usano l'impostazione predefinita verranno assegnate le porte dal set di porte disponibili per Internet, come definito in precedenza. Se N, i processi che utilizzano il valore predefinito verranno assegnati alle porte dal set di porte solo Intranet.</td>
</tr>
<tr class="even">
<td><pre data-space="preserve"><code>HKEY_LOCAL_MACHINE
   System
      CurrentControlSet
         Services
            Rpc
               Linkage
                  Bind</code></pre></td>
<td><strong>REG_MULTI_SZ</strong></td>
<td>Elenca i nomi dei dispositivi di tutte le schede di rete su cui eseguire il binding per impostazione predefinita (ad esempio, \Device\AMDPCN1). Se la chiave non esiste, il server eseguirà l'associazione a tutte le schede di rete. Se la chiave esiste, il server verrà associato alle schede di rete specificate nella chiave, a meno che il campo NICFlags non sia impostato su RPC_C_BIND_TO_ALL_NICS. Se la chiave ha un valore null ( &quot; &quot; ), la configurazione verrà contrassegnata come non valida e tutte le chiamate a <strong>RpcServerUseProtseq *</strong> over <a href="/windows/desktop/Midl/ncacn-ip-tcp"><strong>ncacn_ip_tcp</strong></a> o <a href="/windows/desktop/Midl/ncadg-ip-udp"><strong>ncadg_ip_udp</strong></a> avranno esito negativo.</td>
</tr>
</tbody>
</table>



 

La tabella seguente illustra il modo in cui le impostazioni definite nella tabella precedente hanno effetto su tre applicazioni di esempio e sulle modalità di utilizzo delle impostazioni applicate mediante la funzione [**RpcServerUseProtseqEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqex) .

In questo esempio vengono considerate tre applicazioni ipotetiche:

-   Internetapp: questa applicazione è destinata all'esposizione a Internet e ha specificato il linguaggio RPC C per l' \_ \_ utilizzo della \_ \_ porta Internet nel membro **EndpointFlags** della struttura dei [**\_ criteri RPC**](/windows/desktop/api/Rpcdce/ns-rpcdce-rpc_policy) passata alla funzione [**RpcServerUseProtseqEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqex) .
-   LocalApp: questa applicazione non è progettata per l'esposizione a Internet e ha specificato che RPC \_ C \_ Usa \_ la \_ porta Intranet nel membro **EndpointFlags** della struttura [**dei \_ criteri RPC**](/windows/desktop/api/Rpcdce/ns-rpcdce-rpc_policy) passata alla funzione [**RpcServerUseProtseqEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqex) .
-   File DefaultApp: questa applicazione specifica zero nel membro **EndpointFlags** della struttura dei [**\_ criteri RPC**](/windows/desktop/api/Rpcdce/ns-rpcdce-rpc_policy) passata alla funzione [**RpcServerUseProtseqEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqex) .

La tabella seguente illustra l'effetto di queste impostazioni in base ai valori specificati nelle voci del registro di sistema descritte nella tabella precedente. Per considerazioni sulla formattazione, vengono assegnati i codici seguenti:

PIA = valore chiave PortsInternetAvailable

UIP = valore chiave UseInternetPorts

Il valore della chiave Ports, a scopo di questo esempio, è 5000-5100 per ogni voce.



| Applicazione | PIA | UIP | Risultato                                  |
|-------------|-----|-----|-----------------------------------------|
| Internetapp | S   | S   | Usa le porte comprese tra 5000 e 5100        |
| LocalApp    | S   | S   | Usa una porta al di fuori dell'intervallo 5000-5100 |
| File DefaultApp  | S   | S   | Usa le porte comprese tra 5000 e 5100        |
| Internetapp | S   | N   | Usa le porte comprese tra 5000 e 5100        |
| LocalApp    | S   | N   | Usa una porta al di fuori dell'intervallo 5000-5100 |
| File DefaultApp  | S   | N   | Usa una porta al di fuori dell'intervallo 5000-5100 |
| Internetapp | N   | S   | Usa una porta al di fuori dell'intervallo 5000-5100 |
| LocalApp    | N   | S   | Usa le porte comprese tra 5000 e 5100        |
| File DefaultApp  | N   | S   | Usa una porta al di fuori dell'intervallo 5000-5100 |
| Internetapp | N   | N   | Usa una porta al di fuori dell'intervallo 5000-5100 |
| LocalApp    | N   | N   | Usa le porte comprese tra 5000 e 5100        |
| File DefaultApp  | N   | N   | Usa le porte comprese tra 5000 e 5100        |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**\_criterio RPC**](/windows/desktop/api/Rpcdce/ns-rpcdce-rpc_policy)
</dt> <dt>

[**RpcServerUseAllProtseqsEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseallprotseqsex)
</dt> <dt>

[**RpcServerUseAllProtseqsIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseallprotseqsifex)
</dt> <dt>

[**RpcServerUseProtseqEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqex)
</dt> <dt>

[**RpcServerUseProtseqEpEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqepex)
</dt> <dt>

[**RpcServerUseProtseqIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqifex)
</dt> <dt>

[**\_TCP IP \_ ncacn**](/windows/desktop/Midl/ncacn-ip-tcp)
</dt> <dt>

[**\_UDP IP \_ ncadg**](/windows/desktop/Midl/ncadg-ip-udp)
</dt> </dl>

 

 
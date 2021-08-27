---
title: Configurazione del Registro di sistema per allocazioni di porte e associazione selettiva
description: A partire Windows 2000, è necessario usare un'utilità nel Resource Kit Windows denominata Rpccfg.exe per impostare le associazioni. Per altre informazioni, vedere Windows Resource Kit per la versione del sistema operativo appropriata.
ms.assetid: a33b51e7-2ded-46bd-aadb-27cbd99e1029
keywords:
- RPC Remote Procedure Call , attività, configurazione del Registro di sistema per allocazioni di porte e associazione selettiva
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b220e0e3415b7906c847c0f1196fbc815521dee0
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122465478"
---
# <a name="configuring-the-registry-for-port-allocations-and-selective-binding"></a>Configurazione del Registro di sistema per allocazioni di porte e associazione selettiva

A partire Windows 2000, è necessario usare un'utilità nel Resource Kit Windows denominata Rpccfg.exe per impostare le associazioni. Per altre informazioni, vedere Windows Resource Kit per la versione del sistema operativo appropriata.

Per le versioni di Windows precedenti a Windows 2000, le chiavi del Registro di sistema nella tabella seguente specificano le impostazioni predefinite di sistema per l'allocazione dinamica delle porte e per l'associazione alle schede di interfaccia di rete nei computer multihomed. È prima necessario creare queste chiavi e quindi specificare le impostazioni appropriate.

[**L'uso della funzione RpcServerUseProtseqEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqex) influisce su queste impostazioni. Gli sviluppatori devono avere familiarità con le impostazioni del Registro di sistema illustrate in questa sezione e con la **funzione RpcServerUseProtseqEx** durante la gestione delle allocazioni delle porte. Un esempio con tre applicazioni ipotetiche segue la tabella seguente e illustra l'interoperabilità di queste impostazioni e della funzione **RpcServerUseProtseqEx.**

Se manca una chiave o contiene un valore non valido, l'intera configurazione viene contrassegnata come non valida e tutte le chiamate **RpcServerUseProtseq \** _ [su _ *ncacn \_ ip \_ tcp* *](/windows/desktop/Midl/ncacn-ip-tcp) o [**ncadg \_ ip \_ udp**](/windows/desktop/Midl/ncadg-ip-udp) avranno esito negativo.

> [!Note]  
> Le porte allocate a un processo rimangono allocate fino al termine del processo. Se tutte le porte disponibili sono in uso, la funzione restituisce RPC \_ S \_ OUT OF \_ \_ RESOURCES.

 




| Chiave di porta | Tipo di dati | Descrizione | 
|----------|-----------|-------------|
| <pre data-space="preserve"><code>HKEY_LOCAL_MACHINE   Software      Microsoft         Rpc            Internet               Ports</code></pre> | <strong>REG_MULTI_SZ</strong> | Specifica un set di intervalli di porte IP costituito da tutte le porte disponibili da Internet o da tutte le porte non disponibili da Internet. Ogni stringa rappresenta una singola porta o un set inclusivo di porte (ad esempio, 1000-1050, 1984). Se una voce non rientra nell'intervallo compreso tra 0 e 65535 o se una stringa non può essere interpretata, la fase di esecuzione RPC considera l'intera configurazione come non valida. | 
| <pre data-space="preserve"><code>HKEY_LOCAL_MACHINE   Software      Microsoft         Rpc            Internet               PortsInternetAvailable</code></pre> | <strong>REG_SZ</strong> | Y o N (senza distinzione tra maiuscole e minuscole). Se Y, le porte elencate nella chiave Porte sono tutte le porte disponibili per Internet nel computer. Se N, le porte elencate nella chiave Porte sono tutte quelle non disponibili per Internet. | 
| <pre data-space="preserve"><code>HKEY_LOCAL_MACHINE   Software      Microsoft         Rpc            Internet               UseInternetPorts</code></pre> | <strong>REG_SZ</strong> | Y o N (senza distinzione tra maiuscole e minuscole). Specifica i criteri predefiniti del sistema. Se Y, ai processi che usano l'impostazione predefinita verranno assegnate porte del set di porte disponibili per Internet, come definito in precedenza. Se N, ai processi che usano l'impostazione predefinita verranno assegnate porte del set di porte solo Intranet. | 
| <pre data-space="preserve"><code>HKEY_LOCAL_MACHINE   System      CurrentControlSet         Services            Rpc               Linkage                  Bind</code></pre> | <strong>REG_MULTI_SZ</strong> | Elenca i nomi di dispositivo di tutte le schede di interfaccia di rete da associare per impostazione predefinita (ad esempio, \Device\AMDPCN1). Se la chiave non esiste, il server verrà associato a tutte le schede di interfaccia di rete. Se la chiave esiste, il server verrà associato alle schede di interfaccia di rete specificate nella chiave, a meno che il campo NICFlags non sia impostato su RPC_C_BIND_TO_ALL_NICS. Se la chiave ha un valore null (""), la configurazione verrà contrassegnata come non <a href="/windows/desktop/Midl/ncacn-ip-tcp"><strong></strong></a> valida e tutte le chiamate a <strong>RpcServerUseProtseq*</strong> su ncacn_ip_tcp o ncadg_ip_udp <a href="/windows/desktop/Midl/ncadg-ip-udp"><strong>avranno</strong></a> esito negativo. | 




 

La tabella seguente illustra come tre applicazioni di esempio sono interessate dalle impostazioni definite nella tabella precedente e come vengono interessate anche le impostazioni applicate tramite la funzione [**RpcServerUseProtseqEx.**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqex)

In questo esempio vengono considerate tre applicazioni ipotetiche:

-   InternetApp: questa applicazione è destinata all'esposizione a Internet e ha specificato RPC C USE INTERNET PORT nel membro EndpointFlags della struttura RPC POLICY passata alla funzione \_ \_ \_ \_ [**RpcServerUseProtseqEx.**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqex) [**\_**](/windows/desktop/api/Rpcdce/ns-rpcdce-rpc_policy) 
-   LocalApp: questa applicazione non è destinata all'esposizione a Internet e ha specificato RPC C USE INTRANET PORT nel membro EndpointFlags della struttura RPC POLICY passata alla funzione \_ \_ \_ \_ [**RpcServerUseProtseqEx.**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqex) [**\_**](/windows/desktop/api/Rpcdce/ns-rpcdce-rpc_policy) 
-   DefaultApp: questa applicazione specifica zero nel membro **EndpointFlags** della struttura [**\_ RPC POLICY**](/windows/desktop/api/Rpcdce/ns-rpcdce-rpc_policy) passata alla funzione [**RpcServerUseProtseqEx.**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqex)

La tabella seguente illustra l'impatto di queste impostazioni sui valori specificati nelle voci del Registro di sistema illustrate nella tabella precedente. Per considerazioni sulla formattazione, vengono assegnati i codici seguenti:

PIA = PortsInternetAvailable Key value

UIP = Valore chiave UseInternetPorts

Il valore della chiave Ports, ai fini di questo esempio, è 5000-5100 per ogni voce.



| Applicazione | PIA | UIP | Risultato                                  |
|-------------|-----|-----|-----------------------------------------|
| InternetApp | S   | S   | Usa porte tra 5000 e 5100        |
| LocalApp    | S   | S   | Usa una porta esterna all'intervallo 5000-5100 |
| App predefinita  | S   | S   | Usa porte tra 5000 e 5100        |
| InternetApp | S   | N   | Usa porte tra 5000 e 5100        |
| LocalApp    | S   | N   | Usa una porta esterna all'intervallo 5000-5100 |
| App predefinita  | S   | N   | Usa una porta esterna all'intervallo 5000-5100 |
| InternetApp | N   | S   | Usa una porta esterna all'intervallo 5000-5100 |
| LocalApp    | N   | S   | Usa porte tra 5000 e 5100        |
| App predefinita  | N   | S   | Usa una porta esterna all'intervallo 5000-5100 |
| InternetApp | N   | N   | Usa una porta esterna all'intervallo 5000-5100 |
| LocalApp    | N   | N   | Usa porte tra 5000 e 5100        |
| App predefinita  | N   | N   | Usa porte tra 5000 e 5100        |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**CRITERI \_ RPC**](/windows/desktop/api/Rpcdce/ns-rpcdce-rpc_policy)
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

[**ncacn \_ ip \_ tcp**](/windows/desktop/Midl/ncacn-ip-tcp)
</dt> <dt>

[**ncadg \_ ip \_ udp**](/windows/desktop/Midl/ncadg-ip-udp)
</dt> </dl>

 

 

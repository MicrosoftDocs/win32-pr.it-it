---
title: Configurazione del bilanciamento del carico
description: Configurazione del bilanciamento del carico
ms.assetid: c78ffde1-1811-4065-941f-c24692eb144c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3560359bd5ad064dc270e0840845674b97b093af66796dc92f31f7a15170f467
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118931694"
---
# <a name="configuring-load-balancing"></a>Configurazione del bilanciamento del carico

Ogni computer proxy RPC che deve fungere da servizio server di bilanciamento del carico (LBS) deve essere configurato come servizio LBS con conoscenza dei server nella server farm. Facoltativamente, è possibile impostare la risorsa predefinita ed è possibile impostare la sicurezza delle chiamate RPC da proxy a LBS e da LBS a LBS. Queste impostazioni sono configurate da un set di chiavi del **Registro di sistema obbligatorie** e chiavi del Registro **di sistema facoltative,** come descritto di seguito.

## <a name="required-registry-keys"></a>Chiavi del Registro di sistema necessarie

Sono necessari diversi valori e chiavi del Registro di sistema per configurare un server LBS. Se mancano chiavi o vengono immesse in errore, viene registrato Windows evento. Per informazioni sull'evento registrato, vedere la descrizione di ogni chiave e valore.

Per configurare il server farm, è necessario creare una chiave del Registro di sistema **HKLM \\ SOFTWARE Microsoft Rpc \\ \\ \\ RpcProxy** denominata **LBSConfiguration.** Sotto la **chiave LBSConfiguration** viene creata una chiave per ogni risorsa nel server farm. Il nome della chiave è la rappresentazione di stringa del GUID per la risorsa. Deve esistere almeno una chiave di risorsa e questa risorsa è identica [**all'UUID**](./rpcdce/ns-rpcdce-uuid.md) impostato dai client nell'handle di associazione, [**RPC BINDING \_ \_ HANDLE,**](rpc-binding-handle.md)quando creano l'associazione RPC/HTTP .Per altre informazioni, vedere [**RpcBindingSetObject.**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetobject) In ogni chiave UUID della risorsa deve esistere un valore DWORD denominato **ConfigurationType** che descrive la configurazione usata. Deve esistere anche un **reg \_ SZ** di identificatori di server delimitati da punto e virgola denominato **ServerFarm**. I server identificati nella chiave **ServerFarm** sono i server membri del servizio di bilanciamento del carico server farm.

Di seguito è riportata una suddivisione dettagliata delle chiavi e dei valori del Registro di sistema necessari:

**HKLM \\ SOFTWARE \\ Microsoft \\ Rpc \\ RpcProxy \\ LBSConfiguration**

Chiave del Registro di sistema. La **chiave LBSConfiguration** è la chiave del Registro di sistema che contiene la configurazione di LBS. Sono inclusi gli [**UUID**](./rpcdce/ns-rpcdce-uuid.md) delle risorse di cui eseguire il bilanciamento del carico, il tipo di configurazione per ogni risorsa e i server nelle server farm che partecipano al bilanciamento del carico. Se questa chiave è mancante o non valida, LBS non verrà considerato configurato e il servizio LBS non verrà eseguito.

\-

**HKLM \\ SOFTWARE \\ Microsoft \\ Rpc \\ RpcProxy \\ LBSConfiguration \\ XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX**

Chiave del Registro di sistema. La **chiave UUID della risorsa** identifica l'UUID della risorsa di cui eseguire il bilanciamento del carico. L'UUID della risorsa corrisponde [**all'UUID**](./rpcdce/ns-rpcdce-uuid.md) impostato dai client sull'handle di associazione, [**RPC BINDING \_ \_ HANDLE**](rpc-binding-handle.md). Per eseguire il bilanciamento del carico, è necessario che sia presente almeno un UUID della risorsa. È possibile che siano presenti più UUID di risorsa. Può essere presente un solo server farm e tutti gli endpoint devono essere in tutti i server all'interno del server farm. Se questa chiave non può essere analizzata in un UUID valido, l'evento **RPCPROXY \_ EVENTLOG \_ LB \_ INVALID KEY \_ (0xC0000006)** verrà registrato nel registro eventi di Windows.

\-

**HKLM \\ SOFTWARE \\ Microsoft \\ Rpc \\ RpcProxy \\ LBSConfiguration \\ XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX \\ ConfigurationType**

DWORD. Il valore DWORD **ConfigurationType** viene archiviato nella **chiave UUID della** risorsa. L'unico valore consentito è 1. Se questo valore è diverso da 1, l'evento **RPCPROXY \_ EVENTLOG \_ LB \_ UNKNOWN \_ CFG \_ TYPE (0xC0000007)** verrà registrato nel registro Windows eventi.

\-

**HKLM \\ SOFTWARE \\ Microsoft \\ Rpc \\ RpcProxy \\ LBSConfiguration \\ XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX \\ ServerFarm**

REG \_ SZ. Il valore del Registro di sistema **ServerFarm** contiene un elenco delimitato da punto e virgola di identificatori del server. Il formato per gli identificatori del server è:

"ServerID1,ServerPort1,LBSPort1, \[ LBSPort2, ... LBSPortN \] ;"

Nella chiave del Registro di sistema **ServerFarm** devono essere elencati più identificatori di server. Devono essere delimitati da un punto e virgola. I campi che fanno parte dell'identificatore del server sono descritti nella tabella seguente. Se questo campo non può essere analizzato correttamente, l'evento **RPCPROXY \_ EVENTLOG \_ LB \_ BAD CONFIG \_ ENTRY \_ (0xC0000008)** verrà registrato nel registro Windows eventi.



| Campo identificatore | Requisito | Descrizione                                                                                                                                                                                                                                                                        |
|------------------|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ServerID         | Necessario    | Nome di rete risolvibile per il server. Può trattarsi di un nome DNS, un nome Netbios o un indirizzo IP.                                                                                                                                                                                |
| ServerPort       | Facoltativo    | Se specificato, porta su cui il server è in ascolto per le connessioni RPC/HTTP. Se non specificato, viene usato il mapper di endpoint nel computer server per trovare la porta del server.                                                                                                         |
| LBSPort          | Facoltativo    | Se specificato, la porta su cui il server è in ascolto per LBS. Per usare questa chiave, le interfacce LBS devono essere impostate su un endpoint statico usando un comando netsh RPC firewall. Per esempi del comando netsh, vedere Load [Balancing Best Practices](load-balancing-best-practices.md) (Procedure consigliate per il bilanciamento del carico). |



 

## <a name="optional-registry-keys"></a>Chiavi del Registro di sistema facoltative

Sono disponibili tre valori facoltativi del Registro di sistema per configurare un server LBS. Le chiavi controllano principalmente il livello di sicurezza per le chiamate da e verso il servizio LBS e controllano anche l'UUID della risorsa predefinito da usare. Di seguito sono riportati i valori facoltativi:

Di seguito è riportata una suddivisione dettagliata delle chiavi e dei valori del Registro di sistema necessari:

**HKLM \\ SOFTWARE \\ Microsoft \\ Rpc \\ RpcProxy \\ LBSConfiguration \\ NoSecurity**

DWORD. Quando la DWORD **NoSecurity** non è presente o impostata su 0, le chiamate non protette in ingresso al servizio LBS vengono rifiutate. Quando è presente e non è 0, le chiamate non sicure in ingresso al servizio LBS non vengono rifiutate. Questa chiave viene letta una volta all'avvio del servizio LBS.

\-

**HKLM \\ SOFTWARE \\ Microsoft \\ Rpc \\ RpcProxy \\ LBSConfiguration \\ AssumeResourceUUID**

DWORD. Quando il **DWORD AssumeResourceUUID** non è presente, non si verifica alcuna modifica nel servizio Disaccostie di Archiviazione blob di Windows. Se presente, deve essere impostato con un [**UUID valido.**](./rpcdce/ns-rpcdce-uuid.md) Questo **UUID verrà** usato come UUID della risorsa per tutte le connessioni che non specificano un UUID della risorsa. Viene comunemente usato nei casi in cui i client non specificano un UUID risorsa quando creano l'associazione RPC/HTTP, ma un amministratore vuole bilanciare il carico del traffico RPC/HTTP verso un server farm. Se questa chiave non può essere analizzata in un UUID, viene generato un errore RPC interno, generando RPC [**\_ EXTENDED ERROR \_ \_ INFO**](/windows/win32/api/rpcasync/ns-rpcasync-rpc_extended_error_info) se è abilitata.

\-

**HKLM \\ Software \\ Microsoft \\ Rpc \\ RPCHTTPLBSServer \\ NoSecurity**

DWORD. Quando il valore DWORD **NoSecurity** non viene presentato o impostato su 0, tutte le chiamate in uscita effettuate ai servizi Disaccostie di Archiviazione di Microsoft Windows avranno sicurezza. Se è presente e non è impostato su 0, tutte le chiamate in uscita effettuate ai servizi LBS non avranno sicurezza. Verificare che questa impostazione corrisponda **all'impostazione HKLM \\ SOFTWARE \\ Microsoft \\ \\ RpcProxy \\ LBSConfiguration \\ NoSecurity.**

 

 
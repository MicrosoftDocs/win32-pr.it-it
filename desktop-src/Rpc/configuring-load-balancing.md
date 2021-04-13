---
title: Configurazione del bilanciamento del carico
description: Configurazione del bilanciamento del carico
ms.assetid: c78ffde1-1811-4065-941f-c24692eb144c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b82dbfc23e491d53a6687b50aa77b23878ce52ec
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104338950"
---
# <a name="configuring-load-balancing"></a>Configurazione del bilanciamento del carico

Ogni computer proxy RPC che funge da servizio di bilanciamento del carico (LBS) deve essere configurato come servizio LBS con informazioni sui server nell'server farm. Facoltativamente, è possibile impostare la risorsa predefinita e impostare la sicurezza del proxy su LIBBRe e LBS su LBS per le chiamate RPC. Queste impostazioni vengono configurate da un set di **chiavi del registro** di sistema obbligatorie e da **chiavi del registro di sistema facoltative** , come descritto

## <a name="required-registry-keys"></a>Chiavi del registro di sistema obbligatorie

Per configurare un server LBS sono necessari diversi valori e chiavi del registro di sistema. Se sono presenti chiavi mancanti o immesse in errore, viene registrato un evento di Windows. Per informazioni sull'evento registrato, vedere la descrizione di ogni chiave e valore.

Per configurare la server farm, è necessario creare una chiave del registro di sistema **HKLM \\ software \\ Microsoft \\ RPC \\ Rpcproxy** denominata **LBSConfiguration**. Sotto la chiave **LBSConfiguration** viene creata una chiave per ogni risorsa nel server farm. Il nome della chiave è la rappresentazione di stringa del GUID per la risorsa. È necessario che esista almeno una chiave di risorsa e che questa risorsa sia identica all' [**UUID**](./rpcdce/ns-rpcdce-uuid.md) impostato dai client nell'handle di binding, ovvero un [**\_ \_ handle di binding RPC**](rpc-binding-handle.md), quando crea l'associazione RPC/HTTP (per altre informazioni, vedere [**RpcBindingSetObject**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetobject)). In ogni chiave UUID della risorsa deve esistere un valore DWORD denominato **ConfigurationType** che descrive la configurazione usata. Deve esistere anche un **reg \_ SZ** di identificatori server delimitati da punti e virgola denominati **server farm**. I server identificati nella chiave **server farm** sono i server che sono membri del server farm di bilanciamento del carico.

Di seguito è riportata una suddivisione dettagliata delle chiavi e dei valori del registro di sistema necessari:

**HKLM \\ software \\ Microsoft \\ RPC \\ Rpcproxy \\ LBSConfiguration**

Chiave del registro di sistema. La chiave **LBSConfiguration** è la chiave del registro di sistema che include la configurazione lbs. Sono inclusi gli [**UUID**](./rpcdce/ns-rpcdce-uuid.md) delle risorse che devono essere sottoposte a bilanciamento del carico, il tipo di configurazione per ogni risorsa e i server nelle server farm che partecipano al bilanciamento del carico. Se questa chiave è mancante o non valida, i LBS non verranno considerati configurati e il servizio LBS non verrà eseguito.

\-

**HKLM \\ software \\ Microsoft \\ RPC \\ RPCPROXY \\ LBSCONFIGURATION \\ xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx**

Chiave del registro di sistema. La chiave **UUID della risorsa** identifica l'UUID della risorsa da sottoposta a bilanciamento del carico. Questo UUID della risorsa è identico a [**quello dei client**](./rpcdce/ns-rpcdce-uuid.md) impostati nell'handle di binding [**RPC \_ \_**](rpc-binding-handle.md). È necessario che sia presente almeno un UUID di risorsa per il bilanciamento del carico. possono essere presenti più UUID di risorsa. Può essere presente un solo server farm e tutti gli endpoint devono trovarsi in tutti i server all'interno del server farm. Se questa chiave non può essere analizzata in un UUID valido, la **chiave dell'evento RPCPROXY \_ EventLog \_ lb \_ non valido \_ (0XC0000006)** verrà registrata nel registro eventi di Windows.

\-

**HKLM \\ software \\ Microsoft \\ RPC \\ RPCPROXY \\ LBSCONFIGURATION \\ xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx \\ ConfigurationType**

DWORD. Il valore DWORD **ConfigurationType** viene archiviato nella chiave **UUID della risorsa** . L'unico valore consentito è 1. Se questo valore è diverso da 1, il tipo di evento **RPCPROXY \_ EventLog \_ lb \_ Unknown \_ cfg \_ (0XC0000007)** verrà registrato nel registro eventi di Windows.

\-

**HKLM \\ software \\ Microsoft \\ RPC \\ RPCPROXY \\ LBSCONFIGURATION \\ xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx \\ server farm**

REG \_ SZ. Il valore del registro di sistema **server farm** contiene un elenco delimitati punto e virgola di identificatori server. Il formato degli identificatori del server è:

"ServerID1, ServerPort1, LBSPort1, \[ LBSPort2,... LBSPortN \] ; "

Nella chiave del registro di sistema **server farm** devono essere elencati più identificatori server. Devono essere delimitati da un punto e virgola. I campi che fanno parte dell'identificatore del server sono descritti nella tabella seguente. Se questo campo non può essere analizzato correttamente, la **voce di configurazione Event RPCPROXY \_ EventLog \_ lb \_ \_ \_ (0XC0000008)** verrà registrata nel registro eventi di Windows.



| Campo identificatore | Requisito | Descrizione                                                                                                                                                                                                                                                                        |
|------------------|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ServerID         | Necessario    | Nome di rete risolvibile per il server. Può trattarsi di un nome DNS, un nome NetBIOS o un indirizzo IP.                                                                                                                                                                                |
| ServerPort       | Facoltativo    | Se specificato, la porta su cui il server è in ascolto per le connessioni RPC/HTTP. Se non specificato, viene utilizzato il mapper di endpoint nel computer server per trovare la porta del server.                                                                                                         |
| LBSPort          | Facoltativo    | Se specificato, la porta su cui il server è in ascolto per le LIBBRe. Per usare questa chiave, le interfacce LBS devono essere impostate su un endpoint statico usando un comando netsh RPC firewall. Per esempi del comando netsh, vedere [procedure consigliate di bilanciamento del carico](load-balancing-best-practices.md) . |



 

## <a name="optional-registry-keys"></a>Chiavi del registro di sistema facoltative

Per configurare un server LBS sono disponibili tre valori di registro facoltativi. Le chiavi controllano principalmente il livello di sicurezza per le chiamate da e verso il servizio LBS e controllano anche l'UUID delle risorse predefinito da usare. Di seguito sono riportati i valori facoltativi:

Di seguito è riportata una suddivisione dettagliata delle chiavi e dei valori del registro di sistema necessari:

**HKLM \\ software \\ Microsoft \\ RPC \\ Rpcproxy \\ LBSConfiguration \\ NoSecurity**

DWORD. Quando il valore DWORD **NoSecurity** non è presente o è impostato su 0, le chiamate non protette in ingresso al servizio lbs vengono rifiutate. Quando è presente e non 0, le chiamate non protette in ingresso al servizio LBS non vengono rifiutate. Questa chiave viene letta una volta all'avvio del servizio LBS.

\-

**HKLM \\ software \\ Microsoft \\ RPC \\ Rpcproxy \\ LBSConfiguration \\ AssumeResourceUUID**

DWORD. Quando il valore DWORD **AssumeResourceUUID** non è presente, non viene apportata alcuna modifica nel servizio lbs. Quando è presente, deve essere impostato con un [**UUID**](./rpcdce/ns-rpcdce-uuid.md)valido. Questo **UUID** verrà usato come UUID della risorsa per tutte le connessioni che non specificano un UUID di risorsa. Questa operazione viene in genere utilizzata nei casi in cui i client non specificano l'UUID di una risorsa durante la creazione dell'associazione RPC/HTTP, ma un amministratore desidera bilanciare il carico del traffico RPC/HTTP a una server farm. Se questa chiave non può essere analizzata in un UUID, viene presentato un errore interno di RPC, che genera [**\_ \_ \_ informazioni sugli errori estesi RPC**](/windows/win32/api/rpcasync/ns-rpcasync-rpc_extended_error_info) se è abilitato.

\-

**HKLM \\ software \\ Microsoft \\ RPC \\ RPCHTTPLBSServer \\ NoSecurity**

DWORD. Quando il valore DWORD **NoSecurity** non viene presentato o impostato su 0, tutte le chiamate in uscita effettuate ai servizi lbs avranno la sicurezza. Se presente e non impostato su 0, tutte le chiamate in uscita effettuate ai servizi LBS non avranno sicurezza. Verificare che questa impostazione corrisponda all'impostazione **HKLM \\ software \\ Microsoft \\ RPC \\ Rpcproxy \\ LBSConfiguration \\ NoSecurity** .

 

 
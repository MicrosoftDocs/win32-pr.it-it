---
title: Uso di RPC con proxy Winsock
description: Uso di RPC con proxy Winsock
ms.assetid: d36e2737-f6a0-40ce-92e0-058976c08eb6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b5f658cf60d7e530da99ee139dbcdcbb2c89685
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104047317"
---
# <a name="using-rpc-with-winsock-proxy"></a>Uso di RPC con proxy Winsock

Il rilascio di Microsoft Internet Access Server includeva il proxy Winsock, una versione migliorata di Windows Sockets API versione 1,1. Il proxy Winsock consente a un'applicazione Windows Sockets, in esecuzione in un client di rete privata, di comportarsi come se fosse connessa direttamente a un'applicazione server Internet remota. Il server proxy Microsoft funge da host per questa connessione. Ciò significa che tutte le comunicazioni a livello di applicazione sono canalizzate tramite un singolo computer protetto, ovvero il computer gateway che esegue Microsoft Proxy Server.

In genere, per i trasferimenti di pacchetti di datagramma, la DLL di trasporto RPC Ignora le funzioni [**SendTo**](/windows/desktop/api/winsock/nf-winsock-sendto) e [**recvfrom**](/windows/desktop/api/winsock/nf-winsock-recvfrom) fornite in Wsock32.dll e comunica direttamente con il driver di dispositivo sottostante. In questo modo si migliora la velocità dei trasferimenti di pacchetti ma le funzionalità del proxy Winsock non sono disponibili per l'applicazione.

Ogni provider di protocollo di rete deve disporre di un GUID associato. La libreria di runtime RPC confronta i GUID UDP e IPX con gli identificatori Microsoft noti. Se non corrispondono, RPC usa automaticamente Winsock.

Un'altra funzionalità del proxy Winsock è la possibilità di emulare il protocollo di trasporto TCP sul trasporto Novell SPX quando nel computer client SPX non è installato TCP. Per utilizzare questa funzionalità con le applicazioni RPC, modificare il registro di sistema in ogni computer client per aggiungere la voce seguente:

```
HKEY_LOCAL_MACHINE\Software\Microsoft\Rpc\ClientProtocols
   ncacn_ip_tcp = "rpcltccm.dll"<dl>
<dt>

   Data type
</dt>
<dd>   REG_SZ</dd>
</dl>
   ncadg_ip_udp = "rpcltccm.dll"<dl>
<dt>

   Data type
</dt>
<dd>   REG_SZ</dd>
</dl>
```

Modificare il registro di sistema in ogni computer server per aggiungere la voce seguente:

```
HKEY_LOCAL_MACHINE\Software\Microsoft\Rpc\ServerProtocols
   ncacn_ip_tcp = "rpcltscm.dll"<dl>
<dt>

   Data type
</dt>
<dd>   REG_SZ</dd>
</dl>
   ncadg_ip_udp = "rpcltscm.dll"<dl>
<dt>

   Data type
</dt>
<dd>   REG_SZ</dd>
</dl>
```

Per ulteriori informazioni sui protocolli di trasporto RPC, vedere [specifica delle sequenze di protocollo](specifying-protocol-sequences.md). Per ulteriori informazioni sul proxy Winsock, vedere la documentazione del prodotto per Microsoft Internet Access Server.

Windows 2000 non implementa le voci del registro di sistema **protocolli** e **ServerProtocols** . Microsoft fornisce tutti i trasporti noti come parte della libreria di Runtime. Pertanto, queste voci non sono necessarie.

 

 
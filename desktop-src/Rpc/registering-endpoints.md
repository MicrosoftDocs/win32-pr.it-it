---
title: Registrazione di endpoint
description: La registrazione del programma server nella mappa degli endpoint del computer host del server consente ai programmi client di determinare l'endpoint (in genere una porta TCP/IP o un named pipe) su cui è in ascolto il programma server.
ms.assetid: d09874f8-2b55-4af2-bfe1-8978301d6692
keywords:
- REMOTE Procedure Call RPC , attività, registrazione di endpoint
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6674d20eefa9ebd690f618c36f1dfe69f37dcf7743a0830e06cb38bc85ccfd56
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118926860"
---
# <a name="registering-endpoints"></a>Registrazione di endpoint

La registrazione del programma server nella mappa degli endpoint del computer host del server consente ai programmi client di determinare l'endpoint (in genere una porta TCP/IP o un named pipe) su cui è in ascolto il programma server. Per registrarsi nella mappa degli endpoint del sistema host del server, un programma server chiama la [**funzione RpcEpRegister**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcepregister) come illustrato nel frammento di codice seguente:


```C++
// This example assumes that MyInterface_v1_0_s_ifspec is a valid data
// structure that represents the interface being registered. The 
// variable is a valid pointer to a binding vector.
RPC_STATUS status;
status = RpcEpRegister(
    MyInterface_v1_0_s_ifspec,
    rpcBindingVector,
    NULL,
    NULL);
```



Il primo parametro di [**RpcEpRegister**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcepregister) è la struttura che rappresenta l'interfaccia . È possibile trovarlo nel file di intestazione generato dal compilatore MIDL dal file MIDL per questa applicazione distribuita. Vedere [Sviluppo dell'interfaccia](developing-the-interface.md). **RpcEpRegister richiede** quindi all'applicazione di passare un set di handle di associazione archiviati in un vettore di associazione.

Oltre a registrare i nomi di interfaccia, l'applicazione server può anche registrare gli UUID degli oggetti nella mappa degli endpoint. In questo esempio non sono presenti UUID oggetto da registrare, quindi il terzo parametro di [**RpcEpRegister**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcepregister) è impostato su **NULL.**

L'ultimo parametro è una stringa di commento. Anche se la libreria di runtime RPC non usa questa stringa, è consigliabile impostare la stringa, in quanto migliora la gestibilità del sistema. Un amministratore di sistema può usare la stringa per rilevare le porte usate dalle applicazioni, che possono quindi essere usate per determinare quali porte devono essere gestite dai firewall.

 

 





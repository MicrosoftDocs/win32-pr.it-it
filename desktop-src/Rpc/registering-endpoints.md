---
title: Registrazione degli endpoint
description: La registrazione del programma server nella mappa degli endpoint del computer host del server consente ai programmi client di determinare quale endpoint (in genere una porta TCP/IP o un named pipe) a cui il programma server è in ascolto.
ms.assetid: d09874f8-2b55-4af2-bfe1-8978301d6692
keywords:
- RPC (Remote Procedure Call), attività, registrazione degli endpoint
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f23e02aaae18a9d28b989d16850693a8a8f0678e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103707327"
---
# <a name="registering-endpoints"></a>Registrazione degli endpoint

La registrazione del programma server nella mappa degli endpoint del computer host del server consente ai programmi client di determinare quale endpoint (in genere una porta TCP/IP o un named pipe) a cui il programma server è in ascolto. Per registrarsi nella mappa degli endpoint del sistema host del server, un programma server chiama la funzione [**RpcEpRegister**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcepregister) , come illustrato nel frammento di codice seguente:


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



Il primo parametro di [**RpcEpRegister**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcepregister) è la struttura che rappresenta l'interfaccia. È possibile trovarlo nel file di intestazione generato dal compilatore MIDL dal file MIDL per questa applicazione distribuita. Vedere [sviluppo dell'interfaccia](developing-the-interface.md). Successivamente, **RpcEpRegister** richiede che l'applicazione passi un set di handle di associazione archiviati in un vettore di associazione.

Oltre a registrare i nomi di interfaccia, l'applicazione server può registrare anche UUID di oggetti nella mappa dell'endpoint. In questo esempio non sono presenti UUID di oggetto da registrare, quindi il terzo parametro di [**RpcEpRegister**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcepregister) è impostato su **null**.

L'ultimo parametro è una stringa di commento. Sebbene la libreria di runtime RPC non utilizzi questa stringa, l'impostazione della stringa è consigliata, in quanto migliora la gestibilità del sistema. Un amministratore di sistema può utilizzare la stringa per individuare le porte utilizzate dalle applicazioni, che possono essere utilizzate per determinare le porte da gestire con i firewall.

 

 





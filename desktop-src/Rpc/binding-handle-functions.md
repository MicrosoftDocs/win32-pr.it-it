---
title: Funzioni di handle di associazione
description: La tabella seguente contiene l'elenco delle routine di runtime RPC che operano sugli handle di associazione e specifica il tipo di handle di associazione consentito.
ms.assetid: 16effe59-ebe2-48c3-b97a-90656b6d3b51
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89e00b3cbb2d5fc5637b9414d6f009cfb2e4ade4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106297799"
---
# <a name="binding-handle-functions"></a>Funzioni di handle di associazione

La tabella seguente contiene l'elenco delle routine di runtime RPC che operano sugli handle di associazione e specifica il tipo di handle di associazione consentito.



| Routine                                                            | Argomento di input   | Argomento di output |
|--------------------------------------------------------------------|------------------|-----------------|
| [**RpcBindingCopy**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingcopy)                           | Server           | Server          |
| [**RpcBindingFree**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfree)                           | Server           | nessuno            |
| [**Errore in RpcBindingFromStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding) | nessuno             | Server          |
| [**RpcBindingInqAuthClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclient)         | Client           | nessuno            |
| [**RpcBindingInqAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthinfo)             | Server           | nessuno            |
| [**RpcBindingInqObject**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqobject)                 | Server o client | nessuno            |
| [**RpcBindingReset**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingreset)                         | Server           | nessuno            |
| [**RpcBindingSetAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo)             | Server           | nessuno            |
| [**RpcBindingSetObject**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetobject)                 | Server           | nessuno            |
| [**RpcBindingToStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingtostringbinding)     | Server o client | nessuno            |
| [**RpcBindingVectorFree**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingvectorfree)               | Server           | nessuno            |
| [**RpcNsBindingExport**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingexporta)                   | Server           | nessuno            |
| [**RpcNsBindingImportNext**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportnext)           | nessuno             | Server          |
| [**RpcNsBindingLookupNext**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindinglookupnext)           | nessuno             | Server          |
| [**RpcNsBindingSelect**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingselect)                   | Server           | Server          |
| [**RpcServerInqBindings**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverinqbindings)               | nessuno             | Server          |



 

 

 





---
title: Funzioni di autorizzazione (RPC)
description: Ogni volta che un programma server riceve una richiesta client per l'accesso a una delle procedure remote di gestione, la libreria di runtime RPC richiama una funzione di autorizzazione predefinita.
ms.assetid: e3edbf6f-2876-49ac-a93e-14fd0b5adf53
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47234f83ae76ab6ee29ed434099ba3e4a7dbb3f9c7a01a2448d0cb0dad0267dc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120023413"
---
# <a name="authorization-functions"></a>Funzioni di autorizzazione

Ogni volta che un programma server riceve una richiesta client per l'accesso a una delle procedure remote di gestione, la libreria di runtime RPC richiama una funzione di autorizzazione predefinita. Questa funzione usa il provider di servizi condivisi per controllare le credenziali del client e autorizzare o rifiutare la richiesta.

Il programma server può eseguire l'override della funzione di autorizzazione fornita dal provider di servizi condivisi. Richiamare la [**funzione RpcMgmtSetAuthorizationFn**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtsetauthorizationfn) e passarla all'indirizzo della funzione di autorizzazione. Dopo che il programma server ha impostato la funzione di autorizzazione, la libreria di runtime RPC la chiama ogni volta che il programma server riceve una richiesta client a una delle funzioni di gestione. Per altre informazioni, vedere [**RpcMgmtIsServerListening,**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtisserverlistening) [**RpcMgmtStopServerListening,**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtstopserverlistening) [**RpcMgmtInqIfIds,**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtinqifids) [**RpcMgmtInqServerPrincName**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtinqserverprincname)e [**RpcMgmtInqStats.**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtinqstats)

 

 





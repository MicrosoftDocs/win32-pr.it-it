---
title: Funzioni di autorizzazione (RPC)
description: Ogni volta che un programma server riceve una richiesta client per l'accesso a una delle procedure remote di gestione, la libreria di runtime RPC richiama una funzione di autorizzazione predefinita.
ms.assetid: e3edbf6f-2876-49ac-a93e-14fd0b5adf53
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 490c06ba8e40f132c17986edaef4dc02bbe056d7
ms.sourcegitcommit: 40a1246849dba8ececf54c716b2794b99c96ad50
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/12/2019
ms.locfileid: "104046048"
---
# <a name="authorization-functions"></a>Funzioni di autorizzazione

Ogni volta che un programma server riceve una richiesta client per l'accesso a una delle procedure remote di gestione, la libreria di runtime RPC richiama una funzione di autorizzazione predefinita. Questa funzione utilizza il provider di servizi condivisi per verificare le credenziali del client e autorizzare o rifiutare la richiesta.

Il programma server può eseguire l'override della funzione di autorizzazione fornita dal provider di servizi condivisi. Richiamare la funzione [**RpcMgmtSetAuthorizationFn**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtsetauthorizationfn) e passarla all'indirizzo della funzione di autorizzazione. Quando il programma server imposta la funzione di autorizzazione, la libreria di runtime RPC la chiama ogni volta che il programma server riceve una richiesta client a una delle funzioni di gestione. Per ulteriori informazioni, vedere [**RpcMgmtIsServerListening**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtisserverlistening), [**RpcMgmtStopServerListening**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtstopserverlistening), [**RpcMgmtInqIfIds**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtinqifids), [**RpcMgmtInqServerPrincName**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtinqserverprincname)e [**RpcMgmtInqStats**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtinqstats).

 

 





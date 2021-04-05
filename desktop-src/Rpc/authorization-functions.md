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
# <a name="authorization-functions"></a><span data-ttu-id="c45aa-103">Funzioni di autorizzazione</span><span class="sxs-lookup"><span data-stu-id="c45aa-103">Authorization Functions</span></span>

<span data-ttu-id="c45aa-104">Ogni volta che un programma server riceve una richiesta client per l'accesso a una delle procedure remote di gestione, la libreria di runtime RPC richiama una funzione di autorizzazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="c45aa-104">Each time a server program receives a client request for access to one of the management remote procedures, the RPC run-time library invokes a default authorization function.</span></span> <span data-ttu-id="c45aa-105">Questa funzione utilizza il provider di servizi condivisi per verificare le credenziali del client e autorizzare o rifiutare la richiesta.</span><span class="sxs-lookup"><span data-stu-id="c45aa-105">This function uses the SSP to check the client's credentials and authorize or reject the request.</span></span>

<span data-ttu-id="c45aa-106">Il programma server può eseguire l'override della funzione di autorizzazione fornita dal provider di servizi condivisi.</span><span class="sxs-lookup"><span data-stu-id="c45aa-106">Your server program can override the authorization function that the SSP provides.</span></span> <span data-ttu-id="c45aa-107">Richiamare la funzione [**RpcMgmtSetAuthorizationFn**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtsetauthorizationfn) e passarla all'indirizzo della funzione di autorizzazione.</span><span class="sxs-lookup"><span data-stu-id="c45aa-107">Invoke the function [**RpcMgmtSetAuthorizationFn**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtsetauthorizationfn) and pass it to the address of your authorization function.</span></span> <span data-ttu-id="c45aa-108">Quando il programma server imposta la funzione di autorizzazione, la libreria di runtime RPC la chiama ogni volta che il programma server riceve una richiesta client a una delle funzioni di gestione.</span><span class="sxs-lookup"><span data-stu-id="c45aa-108">Once the server program sets the authorization function, the RPC run-time library calls it every time the server program receives a client request to one of the management functions.</span></span> <span data-ttu-id="c45aa-109">Per ulteriori informazioni, vedere [**RpcMgmtIsServerListening**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtisserverlistening), [**RpcMgmtStopServerListening**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtstopserverlistening), [**RpcMgmtInqIfIds**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtinqifids), [**RpcMgmtInqServerPrincName**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtinqserverprincname)e [**RpcMgmtInqStats**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtinqstats).</span><span class="sxs-lookup"><span data-stu-id="c45aa-109">For more information, see [**RpcMgmtIsServerListening**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtisserverlistening), [**RpcMgmtStopServerListening**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtstopserverlistening), [**RpcMgmtInqIfIds**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtinqifids), [**RpcMgmtInqServerPrincName**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtinqserverprincname), and [**RpcMgmtInqStats**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtinqstats).</span></span>

 

 





---
description: Il server TAPI (TAPISRV) è il repository centrale dei dati di telefonia in un computer utente.
ms.assetid: 794d230c-abe8-429d-bbf5-91ba364b16ab
title: Server TAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 838a6886a5d8e56519f10fc370ed15adc3b1af7d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103883557"
---
# <a name="tapi-server"></a><span data-ttu-id="7db92-103">Server TAPI</span><span class="sxs-lookup"><span data-stu-id="7db92-103">TAPI Server</span></span>

<span data-ttu-id="7db92-104">Il server TAPI (TAPISRV) è il repository centrale dei dati di telefonia in un computer utente.</span><span class="sxs-lookup"><span data-stu-id="7db92-104">The TAPI server (TAPISRV) is the central repository of telephony data on a user computer.</span></span> <span data-ttu-id="7db92-105">Questo processo del servizio tiene traccia delle risorse di telefonia locale e remota, delle applicazioni registrate per gestire le richieste di telefonia assistita e delle funzioni asincrone in sospeso e consente inoltre un'interfaccia coerente con i provider di servizi di telefonia (TSPs).</span><span class="sxs-lookup"><span data-stu-id="7db92-105">This service process tracks local and remote telephony resources, applications registered to handle Assisted Telephony requests, and pending asynchronous functions, and it also enables a consistent interface with telephony service providers (TSPs).</span></span> <span data-ttu-id="7db92-106">Per ulteriori informazioni e un diagramma che illustra la relazione tra il server TAPI e altri componenti e una panoramica dei relativi ruoli, vedere [Microsoft Telephony Programming Model](microsoft-telephony-programming-model.md).</span><span class="sxs-lookup"><span data-stu-id="7db92-106">For more information and a diagram that illustrates the relationship of the TAPI Server to other components and an overview of their roles, see [Microsoft Telephony Programming Model](microsoft-telephony-programming-model.md).</span></span>

<span data-ttu-id="7db92-107">Per i computer che eseguono sistemi operativi Windows Server 2003, Windows XP e Windows 2000, TAPISRV viene eseguito nel contesto di Svchost.exe.</span><span class="sxs-lookup"><span data-stu-id="7db92-107">For computers running on Windows Server 2003 operating systems, Windows XP, and Windows 2000, TAPISRV runs within the context of Svchost.exe.</span></span> <span data-ttu-id="7db92-108">Per i computer che eseguono Windows NT, viene eseguito come processo di servizio separato.</span><span class="sxs-lookup"><span data-stu-id="7db92-108">For computers running on Windows NT, it runs as a separate service process.</span></span> <span data-ttu-id="7db92-109">Quando un'applicazione carica una DLL TAPI nello spazio di processo ed esegue un'operazione di inizializzazione, la DLL stabilisce un collegamento RPC al server TAPI.</span><span class="sxs-lookup"><span data-stu-id="7db92-109">When an application loads a TAPI DLL into its process space and performs an initialization operation, the DLL establishes an RPC link to the TAPI Server.</span></span> <span data-ttu-id="7db92-110">Il server TAPI carica i provider del servizio telefonico (TSPs) nello spazio di elaborazione.</span><span class="sxs-lookup"><span data-stu-id="7db92-110">The TAPI Server loads telephone service providers (TSPs) into its process space.</span></span> <span data-ttu-id="7db92-111">Indipendentemente dal numero di applicazioni che accedono ai dispositivi di un determinato provider, sarà presente una sola istanza di un determinato TSP.</span><span class="sxs-lookup"><span data-stu-id="7db92-111">Regardless of how many applications access a given provider's devices, only one instance of a given TSP will exist.</span></span>

 

 




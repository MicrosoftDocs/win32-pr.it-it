---
title: Informazioni sulle funzioni e le intestazioni delle informazioni di MprInfo
description: Le funzioni seguenti richiedono che il chiamante passi una struttura o un'intestazione di informazioni come uno dei parametri.
ms.assetid: 389002c9-2d24-4b35-ab5b-801fe2091db9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 001c39bf28500d7261b3eb99abf0266470daf3d2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955533"
---
# <a name="understanding-mprinfo-functions-and-information-headers"></a><span data-ttu-id="34843-103">Informazioni sulle funzioni e le intestazioni delle informazioni di MprInfo</span><span class="sxs-lookup"><span data-stu-id="34843-103">Understanding MprInfo Functions and Information Headers</span></span>

<span data-ttu-id="34843-104">Le funzioni seguenti richiedono che il chiamante passi una struttura o un' *intestazione* di informazioni come uno dei parametri.</span><span class="sxs-lookup"><span data-stu-id="34843-104">The following functions require that the caller pass an information structure or *header* as one of the parameters.</span></span>



| <span data-ttu-id="34843-105">Funzione di amministrazione</span><span class="sxs-lookup"><span data-stu-id="34843-105">Administration function</span></span>                                                        | <span data-ttu-id="34843-106">Funzione di configurazione</span><span class="sxs-lookup"><span data-stu-id="34843-106">Configuration function</span></span>                                                           |
|--------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="34843-107">Nessuna funzione di amministrazione</span><span class="sxs-lookup"><span data-stu-id="34843-107">No administration function</span></span>                                                     | [<span data-ttu-id="34843-108">**MprConfigTransportCreate**</span><span class="sxs-lookup"><span data-stu-id="34843-108">**MprConfigTransportCreate**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mprconfigtransportcreate)                     |
| [<span data-ttu-id="34843-109">**MprAdminTransportSetInfo**</span><span class="sxs-lookup"><span data-stu-id="34843-109">**MprAdminTransportSetInfo**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradmintransportsetinfo)                   | [<span data-ttu-id="34843-110">**MprConfigTransportSetInfo**</span><span class="sxs-lookup"><span data-stu-id="34843-110">**MprConfigTransportSetInfo**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mprconfigtransportsetinfo)                   |
| [<span data-ttu-id="34843-111">**MprAdminInterfaceTransportSetInfo**</span><span class="sxs-lookup"><span data-stu-id="34843-111">**MprAdminInterfaceTransportSetInfo**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacetransportsetinfo) | [<span data-ttu-id="34843-112">**MprConfigInterfaceTransportSetInfo**</span><span class="sxs-lookup"><span data-stu-id="34843-112">**MprConfigInterfaceTransportSetInfo**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mprconfiginterfacetransportsetinfo) |
| [<span data-ttu-id="34843-113">**MprAdminInterfaceTransportAdd**</span><span class="sxs-lookup"><span data-stu-id="34843-113">**MprAdminInterfaceTransportAdd**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacetransportadd)         | [<span data-ttu-id="34843-114">**MprConfigInterfaceTransportAdd**</span><span class="sxs-lookup"><span data-stu-id="34843-114">**MprConfigInterfaceTransportAdd**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mprconfiginterfacetransportadd)         |



 

<span data-ttu-id="34843-115">Analogamente, le funzioni seguenti restituiscono le intestazioni delle informazioni.</span><span class="sxs-lookup"><span data-stu-id="34843-115">Similarly, the following functions return information headers.</span></span>



| <span data-ttu-id="34843-116">Funzione di amministrazione</span><span class="sxs-lookup"><span data-stu-id="34843-116">Administration function</span></span>                                                        | <span data-ttu-id="34843-117">Funzione di configurazione</span><span class="sxs-lookup"><span data-stu-id="34843-117">Configuration function</span></span>                                                           |
|--------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| [<span data-ttu-id="34843-118">**MprAdminTransportGetInfo**</span><span class="sxs-lookup"><span data-stu-id="34843-118">**MprAdminTransportGetInfo**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradmintransportgetinfo)                   | [<span data-ttu-id="34843-119">**MprConfigTransportGetInfo**</span><span class="sxs-lookup"><span data-stu-id="34843-119">**MprConfigTransportGetInfo**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mprconfigtransportgetinfo)                   |
| [<span data-ttu-id="34843-120">**MprAdminInterfaceTransportGetInfo**</span><span class="sxs-lookup"><span data-stu-id="34843-120">**MprAdminInterfaceTransportGetInfo**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacetransportgetinfo) | [<span data-ttu-id="34843-121">**MprConfigInterfaceTransportGetInfo**</span><span class="sxs-lookup"><span data-stu-id="34843-121">**MprConfigInterfaceTransportGetInfo**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mprconfiginterfacetransportgetinfo) |



 

<span data-ttu-id="34843-122">Per le funzioni di trasporto, l'intestazione Information contiene informazioni globali per il trasporto.</span><span class="sxs-lookup"><span data-stu-id="34843-122">For the transport functions, the information header contains global information for the transport.</span></span> <span data-ttu-id="34843-123">Per le funzioni client (InterfaceTransport), l'intestazione contiene informazioni specifiche del client, ad esempio OSPF, da amministrare.</span><span class="sxs-lookup"><span data-stu-id="34843-123">For the client (InterfaceTransport) functions, the header contains information specific to the client (for example, OSPF) being administered.</span></span>

<span data-ttu-id="34843-124">Le intestazioni delle informazioni e il relativo contenuto devono essere modificati solo usando le funzioni [MprInfo](router-information-functions.md) .</span><span class="sxs-lookup"><span data-stu-id="34843-124">The information headers and their contents should be manipulated only by using the [MprInfo](router-information-functions.md) functions.</span></span> <span data-ttu-id="34843-125">Gli sviluppatori non devono tentare di modificare direttamente il contenuto delle intestazioni delle informazioni.</span><span class="sxs-lookup"><span data-stu-id="34843-125">Developers should not attempt to manipulate the contents of the information headers directly.</span></span>

<span data-ttu-id="34843-126">Le funzioni di solo interfaccia, ad esempio [**MprAdminInterfaceSetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacesetinfo) , non richiedono l'uso di funzioni MprInfo.</span><span class="sxs-lookup"><span data-stu-id="34843-126">The interface-only functions such as [**MprAdminInterfaceSetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacesetinfo) do not require the use of MprInfo functions.</span></span> <span data-ttu-id="34843-127">Le informazioni passate e restituite con queste funzioni hanno sempre il formato di una struttura di [**\_ interfaccia MPR**](/windows/desktop/api/Mprapi/ns-mprapi-mpr_interface_0) .</span><span class="sxs-lookup"><span data-stu-id="34843-127">The information that is passed and returned with these functions is always in the form of an [**MPR\_INTERFACE**](/windows/desktop/api/Mprapi/ns-mprapi-mpr_interface_0) structure.</span></span>

 

 





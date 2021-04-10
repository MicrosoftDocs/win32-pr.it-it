---
title: Servizio dati remoto rimosso
description: I componenti server di Remote Data Service sono stati rimossi in Windows 8
ms.assetid: 53ECB92C-8868-4A1A-82BD-4ADE75F7BB59
keywords:
- Server RDS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b6588b029fe37f1312c709be168fd695bdc5738
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/01/2020
ms.locfileid: "103963525"
---
# <a name="remote-data-service-server-components-are-removed-in-windows-8"></a><span data-ttu-id="a0786-104">I componenti server di Remote Data Service sono stati rimossi in Windows 8</span><span class="sxs-lookup"><span data-stu-id="a0786-104">Remote data service server components are removed in Windows 8</span></span>

## <a name="platforms"></a><span data-ttu-id="a0786-105">Piattaforme</span><span class="sxs-lookup"><span data-stu-id="a0786-105">Platforms</span></span>

 <span data-ttu-id="a0786-106">**Client** -Windows 8</span><span class="sxs-lookup"><span data-stu-id="a0786-106">**Clients** - Windows 8</span></span>  
<span data-ttu-id="a0786-107">**Server** -Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="a0786-107">**Servers** - Windows Server 2012</span></span>  



## <a name="description"></a><span data-ttu-id="a0786-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a0786-108">Description</span></span>

<span data-ttu-id="a0786-109">Il server servizio dati remoto (RDS) non è disponibile in Windows 8:</span><span class="sxs-lookup"><span data-stu-id="a0786-109">The remote data service (RDS) server is not available in Windows 8:</span></span>

-   <span data-ttu-id="a0786-110">File msadcf.dll, che ospita l'oggetto business "RDSServer. DataFactory" predefinito, viene rimosso e i file associati (msadcfr.dll, msadcfr.dll. mui, handler. reg e handsafe. reg) vengono rimossi</span><span class="sxs-lookup"><span data-stu-id="a0786-110">File msadcf.dll, which hosts the default "business object" RDSServer.DataFactory, is removed, and its associated files (msadcfr.dll, msadcfr.dll.mui, handler.reg and handsafe.reg) are removed</span></span>
-   <span data-ttu-id="a0786-111">File msdfmap.dll, che è il gestore predefinito, viene rimosso e il file msdfmap.ini viene rimosso</span><span class="sxs-lookup"><span data-stu-id="a0786-111">File msdfmap.dll, which is the default Handler, is removed, and the file msdfmap.ini is removed</span></span>
-   <span data-ttu-id="a0786-112">File msadcs.dll, ISAPI, rimosso</span><span class="sxs-lookup"><span data-stu-id="a0786-112">File msadcs.dll, the ISAPI, is removed</span></span>

## <a name="manifestation"></a><span data-ttu-id="a0786-113">Manifestazione</span><span class="sxs-lookup"><span data-stu-id="a0786-113">Manifestation</span></span>

<span data-ttu-id="a0786-114">I clienti non possono ospitare un server RDS in Windows 8.</span><span class="sxs-lookup"><span data-stu-id="a0786-114">Customers cannot host an RDS server on Windows 8.</span></span>

## <a name="mitigation"></a><span data-ttu-id="a0786-115">Strategia di riduzione del rischio</span><span class="sxs-lookup"><span data-stu-id="a0786-115">Mitigation</span></span>

<span data-ttu-id="a0786-116">I clienti possono gestire il server RDS in un computer con Windows 7 o altri sistemi operativi di livello inferiore.</span><span class="sxs-lookup"><span data-stu-id="a0786-116">Customers can keep their RDS server on a machine with Windows 7 or other down-level operating systems.</span></span>

## <a name="solution"></a><span data-ttu-id="a0786-117">Soluzione</span><span class="sxs-lookup"><span data-stu-id="a0786-117">Solution</span></span>

<span data-ttu-id="a0786-118">I clienti possono gestire il server RDS in un computer con Windows 7 o altri sistemi operativi di livello inferiore.</span><span class="sxs-lookup"><span data-stu-id="a0786-118">Customers can keep their RDS server on a machine with Windows 7 or other down-level operating systems.</span></span>

## <a name="resources"></a><span data-ttu-id="a0786-119">Risorse</span><span class="sxs-lookup"><span data-stu-id="a0786-119">Resources</span></span>

[<span data-ttu-id="a0786-120">Guida di orientamento alle tecnologie di accesso ai dati</span><span class="sxs-lookup"><span data-stu-id="a0786-120">Data Access Technologies Roadmap</span></span>](/sql/connect/connect-history?view=sqlallproducts-allversions)

 

 
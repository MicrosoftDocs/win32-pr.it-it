---
description: Il provider WMI raccolta eventi di avvio consente di accedere alle informazioni di connessione e configurazione per la funzionalità di raccolta degli eventi di avvio e di installazione in Windows Server.
ms.assetid: ab9ac8f0-69a5-4a2d-8ee5-1f003aa1bb5b
ms.tgt_platform: multiple
title: Provider WMI raccolta eventi di avvio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a38ef27b2989f856fdcfda82d4ee0e68c3913167
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103877205"
---
# <a name="boot-event-collector-wmi-provider"></a><span data-ttu-id="21e0f-103">Provider WMI raccolta eventi di avvio</span><span class="sxs-lookup"><span data-stu-id="21e0f-103">Boot Event Collector WMI Provider</span></span>

## <a name="purpose"></a><span data-ttu-id="21e0f-104">Scopo</span><span class="sxs-lookup"><span data-stu-id="21e0f-104">Purpose</span></span>

<span data-ttu-id="21e0f-105">Il provider WMI raccolta eventi di avvio consente di accedere alle informazioni di connessione e configurazione per la funzionalità di raccolta degli eventi di avvio e di installazione in Windows Server.</span><span class="sxs-lookup"><span data-stu-id="21e0f-105">The Boot Event Collector WMI provider provides access to connection and configuration information for the Setup and Boot Event Collection feature on Windows Server.</span></span> <span data-ttu-id="21e0f-106">In questo modo è possibile visualizzare un elenco delle connessioni correnti e la cronologia delle connessioni tra un server dell'agente di raccolta e i relativi computer di destinazione.</span><span class="sxs-lookup"><span data-stu-id="21e0f-106">This allows you to view a list of the current connections and the connection history between a collector server and its target computers.</span></span> <span data-ttu-id="21e0f-107">Questo provider consente inoltre di gestire la configurazione di un server di raccolta.</span><span class="sxs-lookup"><span data-stu-id="21e0f-107">In addition, this provider allows you to manage the configuration of a collector server.</span></span>

> [!Note]  
> <span data-ttu-id="21e0f-108">Il provider WMI di raccolta eventi di avvio viene implementato in BEvtCol.exe.</span><span class="sxs-lookup"><span data-stu-id="21e0f-108">The Boot Event Collector WMI provider is implemented in BEvtCol.exe.</span></span>

 

## <a name="in-this-section"></a><span data-ttu-id="21e0f-109">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="21e0f-109">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="21e0f-110">**TargetForwarding**</span><span class="sxs-lookup"><span data-stu-id="21e0f-110">**TargetForwarding**</span></span>](targetforwarding.md)
</dt> <dd>

<span data-ttu-id="21e0f-111">Recupera i dati di invio da un computer di destinazione.</span><span class="sxs-lookup"><span data-stu-id="21e0f-111">Retrieves forwarding data from a target computer.</span></span>

</dd> <dt>

[<span data-ttu-id="21e0f-112">**TargetForwardingDestination**</span><span class="sxs-lookup"><span data-stu-id="21e0f-112">**TargetForwardingDestination**</span></span>](targetforwardingdestination.md)
</dt> <dd>

<span data-ttu-id="21e0f-113">Destinazioni note che contengono i dati raccolti.</span><span class="sxs-lookup"><span data-stu-id="21e0f-113">The known destinations containing the collected data.</span></span> <span data-ttu-id="21e0f-114">Disponibile solo se l'agente di raccolta è in esecuzione con il log di stato abilitato.</span><span class="sxs-lookup"><span data-stu-id="21e0f-114">Available only if the collector is running with the status log enabled.</span></span>

</dd> <dt>

[<span data-ttu-id="21e0f-115">**TargetForwardingHistory**</span><span class="sxs-lookup"><span data-stu-id="21e0f-115">**TargetForwardingHistory**</span></span>](targetforwardinghistory.md)
</dt> <dd>

<span data-ttu-id="21e0f-116">Cronologia recente delle modifiche apportate ai dati di invio per un computer di destinazione.</span><span class="sxs-lookup"><span data-stu-id="21e0f-116">The recent history of changes to the forwarding data for a target computer.</span></span>

</dd> <dt>

[<span data-ttu-id="21e0f-117">**Control**</span><span class="sxs-lookup"><span data-stu-id="21e0f-117">**Control**</span></span>](control.md)
</dt> <dd>

<span data-ttu-id="21e0f-118">Controllo dell'istanza dell'agente di raccolta.</span><span class="sxs-lookup"><span data-stu-id="21e0f-118">Control of the collector instance.</span></span> <span data-ttu-id="21e0f-119">Richiede i privilegi di amministratore (BA).</span><span class="sxs-lookup"><span data-stu-id="21e0f-119">Requires the Administrator (BA) privileges.</span></span>

</dd> </dl>

 

 




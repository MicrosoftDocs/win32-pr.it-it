---
description: La creazione di un filtro di acquisizione che funziona con Network Monitor è un processo in cinque passaggi.
ms.assetid: 04be791c-43c5-44c2-8ab0-799a99974bf6
title: Creazione di un filtro di acquisizione monitoraggio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 097a8276bd6a1f311b343787b3f06175d9b7091f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311627"
---
# <a name="creating-a-monitor-capture-filter"></a><span data-ttu-id="47d40-103">Creazione di un filtro di acquisizione monitoraggio</span><span class="sxs-lookup"><span data-stu-id="47d40-103">Creating a Monitor Capture Filter</span></span>

<span data-ttu-id="47d40-104">La creazione di un filtro di acquisizione che funziona con Network Monitor è un processo in cinque passaggi:</span><span class="sxs-lookup"><span data-stu-id="47d40-104">Creating a capture filter that works with Network Monitor is a five-step process:</span></span>

-   [<span data-ttu-id="47d40-105">Impostazione del filtro ETYPE o SAP</span><span class="sxs-lookup"><span data-stu-id="47d40-105">Setting the Etype or SAP Filter</span></span>](writing-etypesap-filter-portion.md)
-   [<span data-ttu-id="47d40-106">Scrittura del filtro ADDRESSTABLE</span><span class="sxs-lookup"><span data-stu-id="47d40-106">Writing ADDRESSTABLE Filter</span></span>](writing-addresstable-filter-portion.md)
-   [<span data-ttu-id="47d40-107">Scrittura del filtro PATTERNMATCH</span><span class="sxs-lookup"><span data-stu-id="47d40-107">Writing the PATTERNMATCH Filter</span></span>](writing-the-patternmatch-filter.md)
-   [<span data-ttu-id="47d40-108">Ritaglio di un frame</span><span class="sxs-lookup"><span data-stu-id="47d40-108">Clipping a Frame</span></span>](clipping-a-frame.md)
-   [<span data-ttu-id="47d40-109">Implementazione del codice del filtro di acquisizione</span><span class="sxs-lookup"><span data-stu-id="47d40-109">Implementing the Capture Filter Code</span></span>](implementing-the-capture-filter-code.md)

<span data-ttu-id="47d40-110">Un [*filtro di acquisizione*](c.md) è una serie di aggiunte al BLOB di NPP che seleziona i frame che vengono passati di nuovo al monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="47d40-110">A [*capture filter*](c.md) is a series of additions to the NPP BLOB that selects which frames are passed back to the monitor.</span></span> <span data-ttu-id="47d40-111">Se un monitoraggio non modifica il BLOB di NPP, la NPP entra in modalità promiscua e invia tutto il traffico di rete al monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="47d40-111">If a monitor does not alter the NPP BLOB, then the NPP will go into promiscuous mode and send all network traffic to the monitor.</span></span> <span data-ttu-id="47d40-112">L'oggetto NPP è più efficiente se può ridurre i dati passati a un driver, quindi un monitoraggio deve creare un filtro di acquisizione.</span><span class="sxs-lookup"><span data-stu-id="47d40-112">The NPP is most efficient if it can reduce the data handed up to a driver, so a monitor should create a capture filter.</span></span> <span data-ttu-id="47d40-113">Un monitoraggio imposta il relativo filtro di acquisizione scrivendo nel BLOB NPP nella chiamata alla funzione [DoConfigure](imonitor-doconfigure.md) .</span><span class="sxs-lookup"><span data-stu-id="47d40-113">A monitor sets its capture filter by writing to the NPP BLOB in the call to the [DoConfigure](imonitor-doconfigure.md) function.</span></span> <span data-ttu-id="47d40-114">Il MCSVC chiama quindi l'oggetto NPP con il BLOB NPP.</span><span class="sxs-lookup"><span data-stu-id="47d40-114">The MCSVC then calls the NPP with the NPP BLOB.</span></span> <span data-ttu-id="47d40-115">Per altri dettagli sul filtro di acquisizione, sui provider di [pacchetti di rete](network-packet-providers.md) in centrali e sui [BLOB di Network Monitor](network-monitor-blobs.md) nelle funzioni BLOB, vedere i [filtri di acquisizione](capture-filters.md) .</span><span class="sxs-lookup"><span data-stu-id="47d40-115">See [Capture Filters](capture-filters.md) for more details on the capture filter, [Network Packet Providers](network-packet-providers.md) on NPPs, and [Network Monitor Blobs](network-monitor-blobs.md) on BLOB functions.</span></span>

 

 




---
title: Database WinSNMP
description: L'implementazione di Microsoft WinSNMP gestisce un archivio di informazioni amministrative in un database.
ms.assetid: 0a0d9731-d800-4eaa-8230-25469a0b0285
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea83573cad12c05f6dd4b7e2375df5941e05fadb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104471094"
---
# <a name="the-winsnmp-database"></a><span data-ttu-id="43c3a-103">Database WinSNMP</span><span class="sxs-lookup"><span data-stu-id="43c3a-103">The WinSNMP Database</span></span>

<span data-ttu-id="43c3a-104">L'implementazione di Microsoft WinSNMP gestisce un archivio di informazioni amministrative in un database.</span><span class="sxs-lookup"><span data-stu-id="43c3a-104">The Microsoft WinSNMP implementation maintains a store of administrative information in a database.</span></span> <span data-ttu-id="43c3a-105">Il database include le seguenti informazioni:</span><span class="sxs-lookup"><span data-stu-id="43c3a-105">The database includes the following information:</span></span>

-   <span data-ttu-id="43c3a-106">Proprietà della rete e della versione.</span><span class="sxs-lookup"><span data-stu-id="43c3a-106">Network and version properties.</span></span>

    <span data-ttu-id="43c3a-107">L'implementazione utilizza queste proprietà per determinare il protocollo di trasporto di rete e il Framework della versione SNMP da utilizzare per completare le richieste di trasmissione.</span><span class="sxs-lookup"><span data-stu-id="43c3a-107">The implementation uses these properties to determine which network transport protocol and SNMP version framework to use to complete transmission requests.</span></span> <span data-ttu-id="43c3a-108">Per ulteriori informazioni, vedere [informazioni sulle versioni SNMP](about-snmp-versions.md).</span><span class="sxs-lookup"><span data-stu-id="43c3a-108">For more information, see [About SNMP Versions](about-snmp-versions.md).</span></span>

-   <span data-ttu-id="43c3a-109">Modalità di conversione dell'entità e del contesto.</span><span class="sxs-lookup"><span data-stu-id="43c3a-109">Entity and context translation mode.</span></span>

    <span data-ttu-id="43c3a-110">L'implementazione utilizza questa modalità per interpretare i nomi descrittivi per le entità e i contesti SNMP.</span><span class="sxs-lookup"><span data-stu-id="43c3a-110">The implementation uses this mode to interpret user-friendly names for SNMP entities and contexts.</span></span> <span data-ttu-id="43c3a-111">Per ulteriori informazioni, vedere [impostazione della modalità di conversione dell'entità e del contesto](setting-the-entity-and-context-translation-mode.md).</span><span class="sxs-lookup"><span data-stu-id="43c3a-111">For more information, see [Setting the Entity and Context Translation Mode](setting-the-entity-and-context-translation-mode.md).</span></span>

-   <span data-ttu-id="43c3a-112">Impostazione dei criteri di ritrasmissione.</span><span class="sxs-lookup"><span data-stu-id="43c3a-112">Retransmission policy setting.</span></span>

    <span data-ttu-id="43c3a-113">L'implementazione usa questa impostazione per determinare se eseguire o meno i criteri di ritrasmissione dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="43c3a-113">The implementation uses this setting to determine whether or not it should execute the application's retransmission policy.</span></span> <span data-ttu-id="43c3a-114">L'implementazione archivia un valore di timeout e un numero di tentativi per ogni entità di destinazione.</span><span class="sxs-lookup"><span data-stu-id="43c3a-114">The implementation stores a time-out value and a retry count for each destination entity.</span></span> <span data-ttu-id="43c3a-115">Per ulteriori informazioni, vedere [informazioni sulla ritrasmissione](about-retransmission.md) e [la gestione dei criteri di ritrasmissione](managing-the-retransmission-policy.md).</span><span class="sxs-lookup"><span data-stu-id="43c3a-115">For more information, see [About Retransmission](about-retransmission.md) and [Managing the Retransmission Policy](managing-the-retransmission-policy.md).</span></span>

 

 





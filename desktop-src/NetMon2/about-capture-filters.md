---
description: Un filtro di acquisizione è un elemento di un'applicazione NPP che indica al driver Network Monitor (Nmnt.sys) quali frame di dati di rete mantenere e quali frame ignorare.
ms.assetid: 6ab17e18-bd97-42a8-b569-b205ac19ffd1
title: Informazioni sui filtri di acquisizione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7226bb7dc5bc214ab2e09504cc232e1bf591840f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311653"
---
# <a name="about-capture-filters"></a><span data-ttu-id="6991f-103">Informazioni sui filtri di acquisizione</span><span class="sxs-lookup"><span data-stu-id="6991f-103">About Capture Filters</span></span>

<span data-ttu-id="6991f-104">Un filtro di acquisizione è un elemento di un'applicazione NPP che indica al driver Network Monitor (Nmnt.sys) quali frame di dati di rete mantenere e quali frame ignorare.</span><span class="sxs-lookup"><span data-stu-id="6991f-104">A capture filter is an element of an NPP application that instructs the Network Monitor driver (Nmnt.sys) which frames of network data to retain and which frames to ignore.</span></span> <span data-ttu-id="6991f-105">Il vantaggio dell'impostazione di un filtro di acquisizione è una maggiore efficienza.</span><span class="sxs-lookup"><span data-stu-id="6991f-105">The advantage of setting a capture filter is greater efficiency.</span></span> <span data-ttu-id="6991f-106">Non è necessario esaminare i frame acquisiti; il driver Network Monitor li esamina.</span><span class="sxs-lookup"><span data-stu-id="6991f-106">You do not have to examine captured frames; the Network Monitor driver examines them.</span></span> <span data-ttu-id="6991f-107">Questo approccio elimina la copia dei frame, che fornisce un vantaggio per l'utilizzo della memoria.</span><span class="sxs-lookup"><span data-stu-id="6991f-107">This approach eliminates frame copying, which provides a memory use advantage.</span></span>

## <a name="capture-filter-structure"></a><span data-ttu-id="6991f-108">Acquisisci struttura filtro</span><span class="sxs-lookup"><span data-stu-id="6991f-108">Capture Filter Structure</span></span>

<span data-ttu-id="6991f-109">I filtri di acquisizione sono costituiti da tre elementi:</span><span class="sxs-lookup"><span data-stu-id="6991f-109">Capture filters consist of three elements:</span></span>

-   <span data-ttu-id="6991f-110">Impostazioni ETYPE/SAP</span><span class="sxs-lookup"><span data-stu-id="6991f-110">Etype/SAP settings</span></span>
-   <span data-ttu-id="6991f-111">Indirizzo</span><span class="sxs-lookup"><span data-stu-id="6991f-111">Address</span></span>
-   <span data-ttu-id="6991f-112">Corrispondenza criterio</span><span class="sxs-lookup"><span data-stu-id="6991f-112">Pattern match</span></span>

<span data-ttu-id="6991f-113">Insieme, questi elementi valutano logicamente i frame da includere o escludere durante il funzionamento di un'applicazione NPP.</span><span class="sxs-lookup"><span data-stu-id="6991f-113">Together, these elements logically evaluate which frames to include, or exclude, during the operation of an NPP application.</span></span> <span data-ttu-id="6991f-114">Il filtro di acquisizione fornisce corrispondenze complesse ed esclusioni di elementi frame all'applicazione NPP.</span><span class="sxs-lookup"><span data-stu-id="6991f-114">The capture filter supplies complex matches and exclusions of frame elements to the NPP application.</span></span>

<span data-ttu-id="6991f-115">Network Monitor implementa il filtro di acquisizione tramite una struttura di dati, [**capturefilter**](the-capturefilter-structure.md), passata a NPP e quindi passata al driver Network Monitor all'avvio dell'acquisizione.</span><span class="sxs-lookup"><span data-stu-id="6991f-115">Network Monitor implements the capture filter through a data structure, [**CAPTUREFILTER**](the-capturefilter-structure.md), passed to the NPP and then passed on to the Network Monitor driver when the capture starts.</span></span>

<span data-ttu-id="6991f-116">Per ulteriori informazioni sulle operazioni di gestione dei BLOB e sulle funzionalità dei BLOB, vedere [provider di pacchetti di rete](network-packet-providers.md) e [BLOB Network Monitor](network-monitor-blobs.md).</span><span class="sxs-lookup"><span data-stu-id="6991f-116">For more information about NPP operations and BLOB functionality, see [Network Packet Providers](network-packet-providers.md) and [Network Monitor BLOBS](network-monitor-blobs.md).</span></span>

 

 




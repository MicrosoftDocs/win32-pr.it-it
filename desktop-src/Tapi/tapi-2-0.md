---
description: TAPI 2,0 fornisce un piccolo numero di miglioramenti alla funzionalità di base di TAPI 1,4.
ms.assetid: f3a319b4-5e82-4bf9-bd89-a027d58ad126
title: TAPI 2,0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a34a3503916c6ec90c3a90e648ac3622c271d810
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104345426"
---
# <a name="tapi-20"></a><span data-ttu-id="3d9b0-103">TAPI 2,0</span><span class="sxs-lookup"><span data-stu-id="3d9b0-103">TAPI 2.0</span></span>

<span data-ttu-id="3d9b0-104">TAPI 2,0 fornisce un piccolo numero di miglioramenti alla funzionalità di base di TAPI 1,4.</span><span class="sxs-lookup"><span data-stu-id="3d9b0-104">TAPI 2.0 provides a small number of enhancements to the basic TAPI 1.4 functionality.</span></span> <span data-ttu-id="3d9b0-105">Tuttavia, sono state apportate alcune importanti modifiche architettoniche che hanno migliorato notevolmente la stabilità.</span><span class="sxs-lookup"><span data-stu-id="3d9b0-105">However, there were some major architectural changes that greatly improved its stability.</span></span> <span data-ttu-id="3d9b0-106">La maggior parte delle modifiche sono state apportate modifiche fondamentali per l'uso di TAPI per Windows NT 4,0 e per sfruttare i vantaggi delle funzionalità (supporto completo a 32 bit, servizi e Unicode).</span><span class="sxs-lookup"><span data-stu-id="3d9b0-106">Most of the changes were fundamental changes necessary to bring TAPI to Windows NT 4.0 and take advantage of its features (full 32-bit support, services, and Unicode).</span></span> <span data-ttu-id="3d9b0-107">Tuttavia, queste modifiche erano interne a TAPI e avevano un effetto minimo sulle applicazioni TAPI.</span><span class="sxs-lookup"><span data-stu-id="3d9b0-107">However, these changes were internal to TAPI and had little effect on TAPI applications.</span></span>

<span data-ttu-id="3d9b0-108">Le applicazioni che supportano TAPI 1,3 e 1,4 (applicazioni a 16 bit per mezzo di un livello di thunk) funzionano bene nei sistemi operativi Windows Server 2003, Windows XP, Windows 2000 e Windows NT.</span><span class="sxs-lookup"><span data-stu-id="3d9b0-108">Applications that support TAPI 1.3 and 1.4 (16-bit applications by way of a thunking layer) work well on Windows Server 2003 operating systems, Windows XP, Windows 2000, and Windows NT.</span></span> <span data-ttu-id="3d9b0-109">Tuttavia, l'effetto sugli sviluppatori del provider di servizi era significativo.</span><span class="sxs-lookup"><span data-stu-id="3d9b0-109">However, the effect on service-provider developers was significant.</span></span> <span data-ttu-id="3d9b0-110">I provider di servizi per questi sistemi operativi devono essere completamente dll Unicode a 32 bit che possono essere eseguite nel contesto di TAPISRV, non nel contesto dell'applicazione TAPI (come tutti i TSPs precedenti basati su Win16).</span><span class="sxs-lookup"><span data-stu-id="3d9b0-110">Service providers for these operating systems must be fully 32-bit Unicode DLLs that can run in the context of TAPISRV, not in the context of the TAPI application (as did all earlier Win16-based TSPs).</span></span> <span data-ttu-id="3d9b0-111">TSPs progettato per TAPI 1,4 non funziona nei sistemi operativi Windows Server 2003, Windows XP, Windows 2000 o Windows NT.</span><span class="sxs-lookup"><span data-stu-id="3d9b0-111">TSPs designed for TAPI 1.4 do not work on Windows Server 2003 operating systems, Windows XP, Windows 2000, or Windows NT.</span></span>

<span data-ttu-id="3d9b0-112">TAPI 2,0 aggiunge inoltre le funzionalità importanti del supporto del Call Center e del supporto di qualità del servizio (QOS).</span><span class="sxs-lookup"><span data-stu-id="3d9b0-112">TAPI 2.0 also adds the important features of call center support and Quality of Service (QOS) support.</span></span>

<span data-ttu-id="3d9b0-113">I file binari di sistema TAPI disponibili in Windows supportano le versioni di TAPI 1,3 e 1,4 per tutte le applicazioni.</span><span class="sxs-lookup"><span data-stu-id="3d9b0-113">The TAPI system binaries that come with Windows support TAPI versions 1.3 and 1.4 for all applications.</span></span> <span data-ttu-id="3d9b0-114">Tuttavia, le applicazioni a 16 bit non possono usare TAPI 2,0 e non è possibile usare un TSP a 16 bit TAPI 2. x.</span><span class="sxs-lookup"><span data-stu-id="3d9b0-114">However, 16-bit applications cannot use TAPI 2.0, and you cannot use a 16-bit TAPI 2.x TSP.</span></span>

 

 




---
title: Determinazione dello stato dello shim
description: Determinazione dello stato dello shim
ms.assetid: 8D0B633F-9117-4F90-BF8C-AC5F57FCD30B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40b830cbb4579aa2e523dfe2ec1129ed9cd10f37
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104331727"
---
# <a name="determining-shim-status"></a><span data-ttu-id="fba4d-103">Determinazione dello stato dello shim</span><span class="sxs-lookup"><span data-stu-id="fba4d-103">Determining shim status</span></span>

## <a name="platforms"></a><span data-ttu-id="fba4d-104">Piattaforme</span><span class="sxs-lookup"><span data-stu-id="fba4d-104">Platforms</span></span>

<dl> <span data-ttu-id="fba4d-105">Client-Windows 8</span><span class="sxs-lookup"><span data-stu-id="fba4d-105">Clients - Windows 8</span></span>  
<span data-ttu-id="fba4d-106">Server-Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="fba4d-106">Servers - Windows Server 2012</span></span>  
</dl>

## <a name="description"></a><span data-ttu-id="fba4d-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fba4d-107">Description</span></span>

<span data-ttu-id="fba4d-108">Windows 8 registra gli eventi quando le app vengono sottoposto a shim per vari motivi.</span><span class="sxs-lookup"><span data-stu-id="fba4d-108">Windows 8 logs events when apps are being shimmed for various reasons.</span></span> <span data-ttu-id="fba4d-109">Il modo più semplice per determinare se l'app è sottoposto a shim consiste nel controllare il Visualizzatore eventi.</span><span class="sxs-lookup"><span data-stu-id="fba4d-109">The easiest way to determine if your app is being shimmed is to check the event viewer.</span></span> <span data-ttu-id="fba4d-110">Passare a registri applicazioni e servizi \\ Microsoft Windows Application-Experience \\ telemetria del programma.</span><span class="sxs-lookup"><span data-stu-id="fba4d-110">Go to Applications and Services Logs\\Microsoft Windows Application-Experience Program\\Telemetry.</span></span>

## <a name="mitigation"></a><span data-ttu-id="fba4d-111">Strategia di riduzione del rischio</span><span class="sxs-lookup"><span data-stu-id="fba4d-111">Mitigation</span></span>

<span data-ttu-id="fba4d-112">Il modo migliore per uscire da spessoramento consiste nel rinominare il file eseguibile o aumentare la versione principale di 1 (ricompilare il file eseguibile).</span><span class="sxs-lookup"><span data-stu-id="fba4d-112">The best way to get yourself out of shimming is to rename the executable or to increase the major version by 1 (recompile the executable).</span></span>

 

 





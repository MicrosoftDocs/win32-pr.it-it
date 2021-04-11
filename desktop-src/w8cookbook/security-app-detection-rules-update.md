---
title: Aggiornamento delle regole di rilevamento delle app di sicurezza
description: Aggiornamento delle regole di rilevamento delle app di sicurezza
ms.assetid: A272C09B-A777-4119-BAB9-F91ABC03717A
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 242c6f9da8d474c16fab7573e216d3157f93b014
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/01/2020
ms.locfileid: "104047493"
---
# <a name="security-app-detection-rules-update"></a><span data-ttu-id="93982-103">Aggiornamento delle regole di rilevamento delle app di sicurezza</span><span class="sxs-lookup"><span data-stu-id="93982-103">Security app detection rules update</span></span>

## <a name="platforms"></a><span data-ttu-id="93982-104">Piattaforme</span><span class="sxs-lookup"><span data-stu-id="93982-104">Platforms</span></span>

<span data-ttu-id="93982-105">**Client** -Windows 8</span><span class="sxs-lookup"><span data-stu-id="93982-105">**Clients** – Windows 8</span></span>  
<span data-ttu-id="93982-106">**Server** : Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="93982-106">**Servers** – Windows Server 2012</span></span>  


### <a name="description"></a><span data-ttu-id="93982-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="93982-107">Description</span></span>

<span data-ttu-id="93982-108">Le app di Windows Store aggiunte in Windows 8 vengono installate in un percorso comune in "programmi" (% ProgramFiles%) denominato \\ file di programma \\ WindowsApps.</span><span class="sxs-lookup"><span data-stu-id="93982-108">The Windows Store apps being added in Windows 8 are all being installed to a common location under “Program Files” (%programfiles%) called \\program files\\WindowsApps.</span></span>

### <a name="manifestation"></a><span data-ttu-id="93982-109">Manifestazione</span><span class="sxs-lookup"><span data-stu-id="93982-109">Manifestation</span></span>

<span data-ttu-id="93982-110">Questo può causare conflitti con le configurazioni esistenti e alcuni rilevatori antivirus/antimalware vedono questo percorso come una posizione potenziale che rappresenta una fonte di preoccupazione.</span><span class="sxs-lookup"><span data-stu-id="93982-110">This can cause collisions with existing configurations, and some antivirus/anti-malware detectors see this location as a potential location that is a cause for concern.</span></span>

### <a name="mitigation"></a><span data-ttu-id="93982-111">Strategia di riduzione del rischio</span><span class="sxs-lookup"><span data-stu-id="93982-111">Mitigation</span></span>

<span data-ttu-id="93982-112">Le raccomandazioni correnti sono:</span><span class="sxs-lookup"><span data-stu-id="93982-112">The current recommendations are:</span></span>

-   <span data-ttu-id="93982-113">Allontanarsi dai \\ file di programma \\ WindowsApps per archiviare le app personalizzate</span><span class="sxs-lookup"><span data-stu-id="93982-113">Move away from \\program files\\WindowsApps for storing any custom apps</span></span>
-   <span data-ttu-id="93982-114">I fornitori di antivirus/antimalware devono aggiornare le proprie euristiche in modo da non identificare la località come una località di malware</span><span class="sxs-lookup"><span data-stu-id="93982-114">Antivirus/antimalware vendors should update their heuristics so they do not identify that location as a malware location</span></span>

 

 





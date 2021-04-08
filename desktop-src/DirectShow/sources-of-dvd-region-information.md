---
description: Origini delle informazioni sull'area DVD
ms.assetid: f4874aa7-c58a-49a3-9474-c621cc19156b
title: Origini delle informazioni sull'area DVD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ac426f995323bfd30d3430dccb4044c5f71a119
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103967921"
---
# <a name="sources-of-dvd-region-information"></a><span data-ttu-id="04bf6-103">Origini delle informazioni sull'area DVD</span><span class="sxs-lookup"><span data-stu-id="04bf6-103">Sources of DVD Region Information</span></span>

<span data-ttu-id="04bf6-104">Sono disponibili tre fonti di informazioni sull'area DVD che interagiscono per determinare l'area per la riproduzione di DVD in un computer Windows.</span><span class="sxs-lookup"><span data-stu-id="04bf6-104">There are three sources of DVD region information that work together to determine the region for DVD playback on a Windows PC.</span></span>

-   <span data-ttu-id="04bf6-105">Titolo del DVD.</span><span class="sxs-lookup"><span data-stu-id="04bf6-105">DVD Title.</span></span> <span data-ttu-id="04bf6-106">La maggior parte dei titoli DVD è contrassegnata per un'area specifica.</span><span class="sxs-lookup"><span data-stu-id="04bf6-106">Most DVD titles are marked for a specific region.</span></span> <span data-ttu-id="04bf6-107">Alcuni titoli possono essere riprodotti in una sola area, alcuni possono essere riprodotti in più aree e altri possono essere riprodotti in tutte le aree.</span><span class="sxs-lookup"><span data-stu-id="04bf6-107">Some titles can be played in only one region, some can be played in multiple regions, and others can be played all regions.</span></span> <span data-ttu-id="04bf6-108">Le aree da 1 a 6 sono state definite nella specifica DVD-Video originale.</span><span class="sxs-lookup"><span data-stu-id="04bf6-108">Regions 1 through 6 were defined in the original DVD-Video specification.</span></span> <span data-ttu-id="04bf6-109">L'area 7 non è attualmente definita.</span><span class="sxs-lookup"><span data-stu-id="04bf6-109">Region 7 is currently undefined.</span></span> <span data-ttu-id="04bf6-110">L'area 8 è stata aggiunta in 1999 per sedi speciali, ad esempio le aeroplani.</span><span class="sxs-lookup"><span data-stu-id="04bf6-110">Region 8 was added in 1999 for special venues, such as airplanes.</span></span> <span data-ttu-id="04bf6-111">I dischi DVD-ROM (quelli senza area video) non devono contenere codice di area.</span><span class="sxs-lookup"><span data-stu-id="04bf6-111">DVD-ROM discs (those with no video zone) should not contain any region coding.</span></span>
-   <span data-ttu-id="04bf6-112">Unità DVD-ROM.</span><span class="sxs-lookup"><span data-stu-id="04bf6-112">DVD-ROM Drive.</span></span> <span data-ttu-id="04bf6-113">Esistono due tipi di unità DVD-ROM: unità RPC fase 1 (RPC1) e unità RPC fase 2 (RPC2).</span><span class="sxs-lookup"><span data-stu-id="04bf6-113">There are two types of DVD-ROM drives: RPC Phase 1 (RPC1) drives and RPC Phase 2 (RPC2) drives.</span></span> <span data-ttu-id="04bf6-114">Le unità RPC1 non dispongono di supporto hardware integrato per la gestione delle aree.</span><span class="sxs-lookup"><span data-stu-id="04bf6-114">RPC1 drives do not have built-in hardware support for region management.</span></span> <span data-ttu-id="04bf6-115">Per queste unità, Windows mantiene le informazioni sul conteggio delle modifiche dell'area e l'area può essere modificata una sola volta.</span><span class="sxs-lookup"><span data-stu-id="04bf6-115">For these drives, Windows maintains the region change count information and the region can be changed only once.</span></span> <span data-ttu-id="04bf6-116">Le unità RPC2 gestiscono le informazioni sul conteggio delle modifiche nell'hardware e, in generale, l'area di tali unità può essere modificata fino a 5 volte.</span><span class="sxs-lookup"><span data-stu-id="04bf6-116">RPC2 drives maintain the region change count information in hardware and in general the region of such drives can be changed up to 5 times.</span></span>
-   <span data-ttu-id="04bf6-117">Decoder DVD.</span><span class="sxs-lookup"><span data-stu-id="04bf6-117">DVD Decoder.</span></span> <span data-ttu-id="04bf6-118">Alcuni decodificatori DVD, hardware o software, vengono impostati per un'area specifica.</span><span class="sxs-lookup"><span data-stu-id="04bf6-118">Some DVD decoders, hardware or software, are set for a specific region.</span></span> <span data-ttu-id="04bf6-119">In generale, l'utente non può modificare l'area del decodificatore.</span><span class="sxs-lookup"><span data-stu-id="04bf6-119">In general, the user cannot change the decoder's region.</span></span>

## <a name="related-topics"></a><span data-ttu-id="04bf6-120">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="04bf6-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="04bf6-121">Supporto delle modifiche all'area DVD in Windows</span><span class="sxs-lookup"><span data-stu-id="04bf6-121">DVD Region Change Support in Windows</span></span>](dvd-region-change-support-in-windows.md)
</dt> </dl>

 

 




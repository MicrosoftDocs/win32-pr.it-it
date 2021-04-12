---
title: Uso della condivisione della larghezza di banda
description: Uso della condivisione della larghezza di banda
ms.assetid: 1df61a3a-d34a-447e-a7ee-d5d409e7c4fa
keywords:
- Windows Media Format SDK, condivisione della larghezza di banda
- condivisione della larghezza di banda, informazioni
- profili, condivisione della larghezza di banda
- flussi, condivisione della larghezza di banda
- condivisione della larghezza di banda, interfaccia IWMProfile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 298c690b484a8b4b5990aacd5d525867da8923c0
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/25/2020
ms.locfileid: "104398768"
---
# <a name="using-bandwidth-sharing"></a><span data-ttu-id="21e40-108">Uso della condivisione della larghezza di banda</span><span class="sxs-lookup"><span data-stu-id="21e40-108">Using Bandwidth Sharing</span></span>

<span data-ttu-id="21e40-109">È possibile usare gli oggetti di condivisione della larghezza di banda per specificare che determinati flussi, quando combinati, non utilizzeranno più larghezza di banda di quanto specificato.</span><span class="sxs-lookup"><span data-stu-id="21e40-109">You can use bandwidth sharing objects to specify that certain streams, when combined, will not use more bandwidth than specified.</span></span> <span data-ttu-id="21e40-110">Le informazioni in un oggetto di condivisione della larghezza di banda non vengono generate o verificate dal writer né utilizzate dal Reader per alcun elemento.</span><span class="sxs-lookup"><span data-stu-id="21e40-110">The information in a bandwidth sharing object is not generated or verified by the writer nor used by the reader for anything.</span></span>

<span data-ttu-id="21e40-111">Quando viene scritto un file con informazioni sulla condivisione della larghezza di banda nel profilo, i dati vengono archiviati nella relativa sezione di intestazione.</span><span class="sxs-lookup"><span data-stu-id="21e40-111">When a file is written that has bandwidth sharing information in its profile, the data is stored in its header section.</span></span> <span data-ttu-id="21e40-112">È possibile usare l'interfaccia [**IWMProfile**](iwmprofile.md) nel lettore per verificare le informazioni di condivisione della larghezza di banda quando il file viene riprodotto.</span><span class="sxs-lookup"><span data-stu-id="21e40-112">You can use the [**IWMProfile**](iwmprofile.md) interface in the reader to check for bandwidth sharing information when the file is played.</span></span>

<span data-ttu-id="21e40-113">Ogni oggetto di condivisione della larghezza di banda viene definito da due impostazioni.</span><span class="sxs-lookup"><span data-stu-id="21e40-113">Each bandwidth sharing object is defined by two settings.</span></span> <span data-ttu-id="21e40-114">Per prima cosa si intende la larghezza di banda, definita da una larghezza di banda e una finestra del buffer.</span><span class="sxs-lookup"><span data-stu-id="21e40-114">First is the bandwidth, as defined by a bandwidth and a buffer window.</span></span> <span data-ttu-id="21e40-115">La seconda impostazione è un tipo di condivisione della larghezza di banda, che può essere esclusivo o parziale.</span><span class="sxs-lookup"><span data-stu-id="21e40-115">The second setting is a bandwidth sharing type, which can be either exclusive or partial.</span></span> <span data-ttu-id="21e40-116">La condivisione esclusiva della larghezza di banda indica che i flussi costitutivi vengono riprodotti uno alla volta, mentre quello parziale indica che i flussi vengono recapitati contemporaneamente.</span><span class="sxs-lookup"><span data-stu-id="21e40-116">Exclusive bandwidth sharing means that the constituent streams are played back one at a time, while partial means the streams are delivered concurrently.</span></span>

## <a name="related-topics"></a><span data-ttu-id="21e40-117">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="21e40-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="21e40-118">**Interfaccia IWMProfile**</span><span class="sxs-lookup"><span data-stu-id="21e40-118">**IWMProfile Interface**</span></span>](iwmprofile.md)
</dt> <dt>

[<span data-ttu-id="21e40-119">**IWMProfile3::AddBandwidthSharing**</span><span class="sxs-lookup"><span data-stu-id="21e40-119">**IWMProfile3::AddBandwidthSharing**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-addbandwidthsharing)
</dt> <dt>

[<span data-ttu-id="21e40-120">**IWMProfile3::CreateNewBandwidthSharing**</span><span class="sxs-lookup"><span data-stu-id="21e40-120">**IWMProfile3::CreateNewBandwidthSharing**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-createnewbandwidthsharing)
</dt> <dt>

[<span data-ttu-id="21e40-121">**IWMProfile3::GetBandwidthSharing**</span><span class="sxs-lookup"><span data-stu-id="21e40-121">**IWMProfile3::GetBandwidthSharing**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-getbandwidthsharing)
</dt> <dt>

[<span data-ttu-id="21e40-122">**IWMProfile3::GetBandwidthSharingCount**</span><span class="sxs-lookup"><span data-stu-id="21e40-122">**IWMProfile3::GetBandwidthSharingCount**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile3-getbandwidthsharingcount)
</dt> <dt>

[<span data-ttu-id="21e40-123">**Utilizzo dei profili**</span><span class="sxs-lookup"><span data-stu-id="21e40-123">**Working with Profiles**</span></span>](working-with-profiles.md)
</dt> </dl>

 

 





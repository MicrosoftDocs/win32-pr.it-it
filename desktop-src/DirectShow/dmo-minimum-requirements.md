---
description: Requisiti minimi DMO
ms.assetid: cd342f0f-a3dc-4623-a18f-c45071795ef4
title: Requisiti minimi DMO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1c26267f50619062fb8396f93b7578db4d3d8c4
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103965747"
---
# <a name="dmo-minimum-requirements"></a><span data-ttu-id="409a7-103">Requisiti minimi DMO</span><span class="sxs-lookup"><span data-stu-id="409a7-103">DMO Minimum Requirements</span></span>

<span data-ttu-id="409a7-104">Ogni DMO deve soddisfare i requisiti minimi seguenti:</span><span class="sxs-lookup"><span data-stu-id="409a7-104">Every DMO should meet the following minimum requirements:</span></span>

-   <span data-ttu-id="409a7-105">Deve supportare l'aggregazione.</span><span class="sxs-lookup"><span data-stu-id="409a7-105">It must support aggregation.</span></span>
-   <span data-ttu-id="409a7-106">Deve esporre l'interfaccia [**IMediaObject**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-imediaobject) .</span><span class="sxs-lookup"><span data-stu-id="409a7-106">It must expose the [**IMediaObject**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-imediaobject) interface.</span></span>
-   <span data-ttu-id="409a7-107">Il modello di threading deve essere ' both '.</span><span class="sxs-lookup"><span data-stu-id="409a7-107">The threading model must be 'both'.</span></span> <span data-ttu-id="409a7-108">DMOs deve funzionare correttamente in un ambiente a thread libero.</span><span class="sxs-lookup"><span data-stu-id="409a7-108">DMOs must function correctly in a free-threaded environment.</span></span>

<span data-ttu-id="409a7-109">L'effetto audio DMOs deve supportare l'interfaccia [**IMediaObjectInPlace**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobjectinplace) , da usare in DirectMusic e DirectSound.</span><span class="sxs-lookup"><span data-stu-id="409a7-109">Audio effect DMOs should support the [**IMediaObjectInPlace**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobjectinplace) interface, for use in DirectMusic and DirectSound.</span></span>

<span data-ttu-id="409a7-110">Le interfacce seguenti sono documentate altrove, ma sono utili per molti DMOs.</span><span class="sxs-lookup"><span data-stu-id="409a7-110">The following interfaces are documented elsewhere, but are useful for many DMOs.</span></span> <span data-ttu-id="409a7-111">Tuttavia, non sono necessarie.</span><span class="sxs-lookup"><span data-stu-id="409a7-111">They are not required, however.</span></span>

-   <span data-ttu-id="409a7-112">**ISpecifyPropertyPages**, **IPropertyPage**: queste interfacce consentono a DMO di fornire una pagina delle proprietà per consentire all'utente di impostare le proprietà.</span><span class="sxs-lookup"><span data-stu-id="409a7-112">**ISpecifyPropertyPages**, **IPropertyPage**: These interfaces enable a DMO to provide a property page, for the user to set properties.</span></span>
-   <span data-ttu-id="409a7-113">**IPersistStream**: questa interfaccia consente a DMO di salvare lo stato nell'archivio permanente.</span><span class="sxs-lookup"><span data-stu-id="409a7-113">**IPersistStream**: This interface enables the DMO to save its state to persistent storage.</span></span>
-   <span data-ttu-id="409a7-114">[**IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig), [**IAMVideoCompression**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression): queste interfacce consentono a un client di configurare il formato di output del codificatore e le impostazioni di compressione.</span><span class="sxs-lookup"><span data-stu-id="409a7-114">[**IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig), [**IAMVideoCompression**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression): These interfaces enable a client to configure an encoder's output format and compression settings.</span></span> <span data-ttu-id="409a7-115">Queste due interfacce fanno parte dell'API DirectShow, ma sono consigliate anche per DMOs.</span><span class="sxs-lookup"><span data-stu-id="409a7-115">(These two interfaces are part of the DirectShow API, but are also recommended for DMOs.)</span></span>

## <a name="related-topics"></a><span data-ttu-id="409a7-116">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="409a7-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="409a7-117">Scrittura di un DMO</span><span class="sxs-lookup"><span data-stu-id="409a7-117">Writing a DMO</span></span>](writing-a-dmo.md)
</dt> </dl>

 

 




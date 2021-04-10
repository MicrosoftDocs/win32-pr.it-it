---
description: Set di proprietà di trasporto dispositivo esterno
ms.assetid: 9c80cf59-054f-49b6-9456-ed5e091cbfaf
title: Set di proprietà di trasporto dispositivo esterno
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e77942157b7cf5f75b883e6953f3a115d1fa9f6
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104125601"
---
# <a name="external-device-transport-property-set"></a><span data-ttu-id="11602-103">Set di proprietà di trasporto dispositivo esterno</span><span class="sxs-lookup"><span data-stu-id="11602-103">External Device Transport Property Set</span></span>

<span data-ttu-id="11602-104">Questo set di proprietà controlla il trasporto di dati da e verso un dispositivo esterno.</span><span class="sxs-lookup"><span data-stu-id="11602-104">This property set controls the transport of data to and from an external device.</span></span> <span data-ttu-id="11602-105">Nella maggior parte dei casi, le applicazioni non devono utilizzare direttamente questo set di proprietà.</span><span class="sxs-lookup"><span data-stu-id="11602-105">In most cases, applications should not use this property set directly.</span></span> <span data-ttu-id="11602-106">Usare invece l'interfaccia [**IAMExtTransport**](/windows/desktop/api/Strmif/nn-strmif-iamexttransport) .</span><span class="sxs-lookup"><span data-stu-id="11602-106">Use the [**IAMExtTransport**](/windows/desktop/api/Strmif/nn-strmif-iamexttransport) interface instead.</span></span>

<span data-ttu-id="11602-107">Nella tabella seguente sono elencate le proprietà rilevanti per le applicazioni in modalità utente.</span><span class="sxs-lookup"><span data-stu-id="11602-107">The following table lists the properties that are relevant to user-mode applications.</span></span> <span data-ttu-id="11602-108">Per una descrizione completa di questo set di proprietà, vedere Microsoft Windows Driver Development Kit DDK.</span><span class="sxs-lookup"><span data-stu-id="11602-108">For a complete description of this property set, refer to the Microsoft Windows Driver Development Kit DDK.</span></span>



|                   |                           |
|-------------------|---------------------------|
| <span data-ttu-id="11602-109">GUID set di proprietà</span><span class="sxs-lookup"><span data-stu-id="11602-109">Property Set GUID</span></span> | <span data-ttu-id="11602-110">\_trasporto PROPSETID ext \_</span><span class="sxs-lookup"><span data-stu-id="11602-110">PROPSETID\_EXT\_TRANSPORT</span></span> |



 



| <span data-ttu-id="11602-111">ID proprietà</span><span class="sxs-lookup"><span data-stu-id="11602-111">Property ID</span></span>                                                                           | <span data-ttu-id="11602-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="11602-112">Description</span></span>                                  |
|---------------------------------------------------------------------------------------|----------------------------------------------|
| [<span data-ttu-id="11602-113">**\_ricerca KSPROPERTY EXTXPORT \_ ATN \_**</span><span class="sxs-lookup"><span data-stu-id="11602-113">**KSPROPERTY\_EXTXPORT\_ATN\_SEARCH**</span></span>](ksproperty-extxport-atn-search.md)           | <span data-ttu-id="11602-114">Cerca un numero di traccia assoluto (ATN).</span><span class="sxs-lookup"><span data-stu-id="11602-114">Searches for an absolute track number (ATN).</span></span> |
| [<span data-ttu-id="11602-115">**KSPROPERTY \_ EXTXPORT \_ - \_ ricerca timecode**</span><span class="sxs-lookup"><span data-stu-id="11602-115">**KSPROPERTY\_EXTXPORT\_TIMECODE\_SEARCH**</span></span>](ksproperty-extxport-timecode-search.md) | <span data-ttu-id="11602-116">Cerca un codice temporale.</span><span class="sxs-lookup"><span data-stu-id="11602-116">Searches for a time code.</span></span>                    |



 

## <a name="related-topics"></a><span data-ttu-id="11602-117">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="11602-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="11602-118">Set di proprietà</span><span class="sxs-lookup"><span data-stu-id="11602-118">Property Sets</span></span>](property-sets.md)
</dt> </dl>

 

 




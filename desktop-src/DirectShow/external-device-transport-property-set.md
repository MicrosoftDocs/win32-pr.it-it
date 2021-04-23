---
description: Set di proprietà Trasporto dispositivo esterno
ms.assetid: 9c80cf59-054f-49b6-9456-ed5e091cbfaf
title: Set di proprietà Trasporto dispositivo esterno
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85e38217af21ea1839d7c9207a4922bcff00d63a
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909219"
---
# <a name="external-device-transport-property-set"></a><span data-ttu-id="f279a-103">Set di proprietà Trasporto dispositivo esterno</span><span class="sxs-lookup"><span data-stu-id="f279a-103">External Device Transport Property Set</span></span>

<span data-ttu-id="f279a-104">Questo set di proprietà controlla il trasporto dei dati da e verso un dispositivo esterno.</span><span class="sxs-lookup"><span data-stu-id="f279a-104">This property set controls the transport of data to and from an external device.</span></span> <span data-ttu-id="f279a-105">Nella maggior parte dei casi, le applicazioni non devono usare direttamente questa proprietà impostata.</span><span class="sxs-lookup"><span data-stu-id="f279a-105">In most cases, applications should not use this property set directly.</span></span> <span data-ttu-id="f279a-106">Usare invece [**l'interfaccia IAMExtTransport.**](/windows/desktop/api/Strmif/nn-strmif-iamexttransport)</span><span class="sxs-lookup"><span data-stu-id="f279a-106">Use the [**IAMExtTransport**](/windows/desktop/api/Strmif/nn-strmif-iamexttransport) interface instead.</span></span>

<span data-ttu-id="f279a-107">Nella tabella seguente sono elencate le proprietà rilevanti per le applicazioni in modalità utente.</span><span class="sxs-lookup"><span data-stu-id="f279a-107">The following table lists the properties that are relevant to user-mode applications.</span></span> <span data-ttu-id="f279a-108">Per una descrizione completa di questo set di proprietà, vedere microsoft Windows Driver Development Kit DDK.</span><span class="sxs-lookup"><span data-stu-id="f279a-108">For a complete description of this property set, refer to the Microsoft Windows Driver Development Kit DDK.</span></span>



| <span data-ttu-id="f279a-109">Label</span><span class="sxs-lookup"><span data-stu-id="f279a-109">Label</span></span> | <span data-ttu-id="f279a-110">Valore</span><span class="sxs-lookup"><span data-stu-id="f279a-110">Value</span></span> |
|-------------------|---------------------------|
| <span data-ttu-id="f279a-111">GUID set di proprietà</span><span class="sxs-lookup"><span data-stu-id="f279a-111">Property Set GUID</span></span> | <span data-ttu-id="f279a-112">PROPSETID \_ EXT \_ TRANSPORT</span><span class="sxs-lookup"><span data-stu-id="f279a-112">PROPSETID\_EXT\_TRANSPORT</span></span> |



 



| <span data-ttu-id="f279a-113">ID proprietà</span><span class="sxs-lookup"><span data-stu-id="f279a-113">Property ID</span></span>                                                                           | <span data-ttu-id="f279a-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f279a-114">Description</span></span>                                  |
|---------------------------------------------------------------------------------------|----------------------------------------------|
| [<span data-ttu-id="f279a-115">**KSPROPERTY \_ EXTXPORT \_ ATN \_ SEARCH**</span><span class="sxs-lookup"><span data-stu-id="f279a-115">**KSPROPERTY\_EXTXPORT\_ATN\_SEARCH**</span></span>](ksproperty-extxport-atn-search.md)           | <span data-ttu-id="f279a-116">Cerca un numero di traccia assoluto (ATN).</span><span class="sxs-lookup"><span data-stu-id="f279a-116">Searches for an absolute track number (ATN).</span></span> |
| [<span data-ttu-id="f279a-117">**KSPROPERTY \_ EXTXPORT \_ TIMECODE \_ SEARCH**</span><span class="sxs-lookup"><span data-stu-id="f279a-117">**KSPROPERTY\_EXTXPORT\_TIMECODE\_SEARCH**</span></span>](ksproperty-extxport-timecode-search.md) | <span data-ttu-id="f279a-118">Cerca un time code.</span><span class="sxs-lookup"><span data-stu-id="f279a-118">Searches for a time code.</span></span>                    |



 

## <a name="related-topics"></a><span data-ttu-id="f279a-119">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f279a-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f279a-120">Set di proprietà</span><span class="sxs-lookup"><span data-stu-id="f279a-120">Property Sets</span></span>](property-sets.md)
</dt> </dl>

 

 




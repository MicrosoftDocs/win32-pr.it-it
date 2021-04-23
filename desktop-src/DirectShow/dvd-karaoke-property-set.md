---
description: Quando il filtro DVD Navigator passa alla modalità schermo intero, informa il decodificatore audio tramite la proprietà \_ AM PROPERTY \_ DVDKARAOKE \_ ENABLE.
ms.assetid: 78b2998b-d8b3-424d-85bc-872e64eb4a4f
title: Set di proprietà DVD Dvd Dvdmedia.h
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2918513de06a657436ed99e67f672fe74a113b78
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909069"
---
# <a name="dvd-karaoke-property-set"></a><span data-ttu-id="592de-103">DVD Karaoke Property Set</span><span class="sxs-lookup"><span data-stu-id="592de-103">DVD Karaoke Property Set</span></span>

<span data-ttu-id="592de-104">Quando il [filtro DVD Navigator](dvd-navigator-filter.md) passa alla modalità schermo intero, informa il decodificatore audio tramite la proprietà AM PROPERTY **\_ \_ DVDKARAOKE \_ ENABLE.**</span><span class="sxs-lookup"><span data-stu-id="592de-104">When the [DVD Navigator](dvd-navigator-filter.md) filter goes into karaoke mode, it informs the audio decoder through the **AM\_PROPERTY\_DVDKARAOKE\_ENABLE** property.</span></span> <span data-ttu-id="592de-105">Il decodificatore deve quindi disattivare i canali audio da 2 a 5 fino a quando non riceve dallo strumento di navigazione DVD una proprietà **\_ AM PROPERTY \_ DVDKARAOKE \_ DATA** con un puntatore a una struttura di dati [**\_ DVDKaraokeData am**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-am_dvdkaraokedata) che indica come devono essere misti i canali ausiliari.</span><span class="sxs-lookup"><span data-stu-id="592de-105">The decoder should then mute audio channels 2 through 5 until it receives from the DVD Navigator an **AM\_PROPERTY\_DVDKARAOKE\_DATA** property with a pointer to an [**AM\_DvdKaraokeData**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-am_dvdkaraokedata) data structure indicating how the auxiliary channels are to be mixed.</span></span>



| <span data-ttu-id="592de-106">Label</span><span class="sxs-lookup"><span data-stu-id="592de-106">Label</span></span> | <span data-ttu-id="592de-107">Valore</span><span class="sxs-lookup"><span data-stu-id="592de-107">Value</span></span> |
|-------------------|-----------------------------|
| <span data-ttu-id="592de-108">GUID set di proprietà</span><span class="sxs-lookup"><span data-stu-id="592de-108">Property Set GUID</span></span> | <span data-ttu-id="592de-109">AM \_ KSPROPSETID \_ DvdKaraoke</span><span class="sxs-lookup"><span data-stu-id="592de-109">AM\_KSPROPSETID\_DvdKaraoke</span></span> |



 



| <span data-ttu-id="592de-110">ID proprietà</span><span class="sxs-lookup"><span data-stu-id="592de-110">Property ID</span></span>                      | <span data-ttu-id="592de-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="592de-111">Description</span></span>                                                                                                                                                                                                                                                                                                 |
|----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="592de-112">AM \_ PROPERTY \_ DVDKARAOKE \_ ENABLE</span><span class="sxs-lookup"><span data-stu-id="592de-112">AM\_PROPERTY\_DVDKARAOKE\_ENABLE</span></span> | <span data-ttu-id="592de-113">Valore BOOLEAN.</span><span class="sxs-lookup"><span data-stu-id="592de-113">BOOLEAN value.</span></span> <span data-ttu-id="592de-114">Lo strumento di navigazione dvd invia al decodificatore un \_ DVD AM PROPERTYKARAOKE ENABLE con valore TRUE per abilitare il downmixing o FALSE per \_ \_ disabilitarlo.  </span><span class="sxs-lookup"><span data-stu-id="592de-114">The DVD Navigator sends the decoder an AM\_PROPERTY\_DVDKARAOKE\_ENABLE with a value of **TRUE** to enable karaoke downmixing or **FALSE** to disable it.</span></span>                                                                                                                                    |
| <span data-ttu-id="592de-115">PROPRIETÀ \_ AM \_ DVDKARAOKE \_ DATA</span><span class="sxs-lookup"><span data-stu-id="592de-115">AM\_PROPERTY\_DVDKARAOKE\_DATA</span></span>   | <span data-ttu-id="592de-116">Lo strumento di navigazione dvd invia al decodificatore una proprietà AM PROPERTY DVDKARAOKE DATA con un puntatore a una struttura \_ \_ AM \_ [**\_ DvdKaraokeData**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-am_dvdkaraokedata) per modificare la configurazione downmix, ad esempio per attivare o disattivare determinati canali di canali e indirizzarli al canale di output destro o sinistro.</span><span class="sxs-lookup"><span data-stu-id="592de-116">The DVD Navigator sends the decoder an AM\_PROPERTY\_DVDKARAOKE\_DATA property with a pointer to an [**AM\_DvdKaraokeData**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-am_dvdkaraokedata) structure to change the downmix configuration; that is, to turn certain karaoke channels on or off and direct them to the right or left output channel.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="592de-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="592de-117">Requirements</span></span>



| <span data-ttu-id="592de-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="592de-118">Requirement</span></span> | <span data-ttu-id="592de-119">Valore</span><span class="sxs-lookup"><span data-stu-id="592de-119">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="592de-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="592de-120">Header</span></span><br/> | <dl> <span data-ttu-id="592de-121"><dt>Dvdmedia.h</dt></span><span class="sxs-lookup"><span data-stu-id="592de-121"><dt>Dvdmedia.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="592de-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="592de-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="592de-123">Set di proprietà</span><span class="sxs-lookup"><span data-stu-id="592de-123">Property Sets</span></span>](property-sets.md)
</dt> </dl>

 

 





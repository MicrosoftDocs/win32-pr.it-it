---
description: Quando il filtro dello strumento di spostamento DVD passa alla modalità karaoke, informa il decodificatore audio tramite la proprietà AM \_ \_ DVDKARAOKE \_ Enable.
ms.assetid: 78b2998b-d8b3-424d-85bc-872e64eb4a4f
title: Set di proprietà DVD karaoke (dvdmedia. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 396e9fe53ad35dac0c3c0f54a8e04a6fbe698fc1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325726"
---
# <a name="dvd-karaoke-property-set"></a><span data-ttu-id="e2359-103">Set di proprietà di DVD karaoke</span><span class="sxs-lookup"><span data-stu-id="e2359-103">DVD Karaoke Property Set</span></span>

<span data-ttu-id="e2359-104">Quando il filtro dello [strumento di spostamento DVD](dvd-navigator-filter.md) passa alla modalità karaoke, informa il decodificatore audio tramite la proprietà **am \_ \_ DVDKARAOKE \_ Enable** .</span><span class="sxs-lookup"><span data-stu-id="e2359-104">When the [DVD Navigator](dvd-navigator-filter.md) filter goes into karaoke mode, it informs the audio decoder through the **AM\_PROPERTY\_DVDKARAOKE\_ENABLE** property.</span></span> <span data-ttu-id="e2359-105">Il decodificatore deve quindi disattivare i canali audio da 2 a 5 fino a quando non riceve dal navigatore DVD una proprietà **\_ \_ \_ dei dati DVDKARAOKE della proprietà am** con un puntatore a una struttura di dati [**\_ DvdKaraokeData am**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-am_dvdkaraokedata) che indica il modo in cui devono essere combinati i canali ausiliari.</span><span class="sxs-lookup"><span data-stu-id="e2359-105">The decoder should then mute audio channels 2 through 5 until it receives from the DVD Navigator an **AM\_PROPERTY\_DVDKARAOKE\_DATA** property with a pointer to an [**AM\_DvdKaraokeData**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-am_dvdkaraokedata) data structure indicating how the auxiliary channels are to be mixed.</span></span>



|                   |                             |
|-------------------|-----------------------------|
| <span data-ttu-id="e2359-106">GUID set di proprietà</span><span class="sxs-lookup"><span data-stu-id="e2359-106">Property Set GUID</span></span> | <span data-ttu-id="e2359-107">\_DvdKaraoke KSPROPSETID \_</span><span class="sxs-lookup"><span data-stu-id="e2359-107">AM\_KSPROPSETID\_DvdKaraoke</span></span> |



 



| <span data-ttu-id="e2359-108">ID proprietà</span><span class="sxs-lookup"><span data-stu-id="e2359-108">Property ID</span></span>                      | <span data-ttu-id="e2359-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e2359-109">Description</span></span>                                                                                                                                                                                                                                                                                                 |
|----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e2359-110">\_Proprietà am \_ DVDKARAOKE \_ Enable</span><span class="sxs-lookup"><span data-stu-id="e2359-110">AM\_PROPERTY\_DVDKARAOKE\_ENABLE</span></span> | <span data-ttu-id="e2359-111">Valore BOOLEANo.</span><span class="sxs-lookup"><span data-stu-id="e2359-111">BOOLEAN value.</span></span> <span data-ttu-id="e2359-112">Il navigatore DVD invia al decodificatore la \_ Proprietà am \_ DVDKARAOKE \_ Enable con il valore **true** per abilitare il karaoke downmixing o **false** per disabilitarlo.</span><span class="sxs-lookup"><span data-stu-id="e2359-112">The DVD Navigator sends the decoder an AM\_PROPERTY\_DVDKARAOKE\_ENABLE with a value of **TRUE** to enable karaoke downmixing or **FALSE** to disable it.</span></span>                                                                                                                                    |
| <span data-ttu-id="e2359-113">\_ \_ dati DVDKARAOKE proprietà \_ am</span><span class="sxs-lookup"><span data-stu-id="e2359-113">AM\_PROPERTY\_DVDKARAOKE\_DATA</span></span>   | <span data-ttu-id="e2359-114">Il navigatore DVD invia al decodificatore una \_ \_ proprietà dei dati DVDKARAOKE della proprietà am \_ con un puntatore a una struttura [**am \_ DvdKaraokeData**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-am_dvdkaraokedata) per modificare la configurazione downmix, ovvero per attivare o disattivare determinati canali karaoke e indirizzarli al canale di output a destra o a sinistra.</span><span class="sxs-lookup"><span data-stu-id="e2359-114">The DVD Navigator sends the decoder an AM\_PROPERTY\_DVDKARAOKE\_DATA property with a pointer to an [**AM\_DvdKaraokeData**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-am_dvdkaraokedata) structure to change the downmix configuration; that is, to turn certain karaoke channels on or off and direct them to the right or left output channel.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="e2359-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e2359-115">Requirements</span></span>



| <span data-ttu-id="e2359-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="e2359-116">Requirement</span></span> | <span data-ttu-id="e2359-117">Valore</span><span class="sxs-lookup"><span data-stu-id="e2359-117">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e2359-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e2359-118">Header</span></span><br/> | <dl> <span data-ttu-id="e2359-119"><dt>Dvdmedia. h</dt></span><span class="sxs-lookup"><span data-stu-id="e2359-119"><dt>Dvdmedia.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e2359-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e2359-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2359-121">Set di proprietà</span><span class="sxs-lookup"><span data-stu-id="e2359-121">Property Sets</span></span>](property-sets.md)
</dt> </dl>

 

 





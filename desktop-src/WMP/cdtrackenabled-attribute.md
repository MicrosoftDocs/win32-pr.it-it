---
title: Attributo CDTrackEnabled
description: L'attributo CDTrackEnabled indica se la traccia è abilitata per la riproduzione.
ms.assetid: ebbc42bd-2d6c-47ae-9a3f-c6256b120d35
keywords:
- Attributo CDTrackEnabled Windows Media Player
topic_type:
- apiref
api_name:
- CDTrackEnabled
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c81c231dbdfc432ea7aa510a19b1f85e0826c836
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333129"
---
# <a name="cdtrackenabled-attribute"></a><span data-ttu-id="e8184-104">Attributo CDTrackEnabled</span><span class="sxs-lookup"><span data-stu-id="e8184-104">CDTrackEnabled Attribute</span></span>

<span data-ttu-id="e8184-105">L'attributo **CDTrackEnabled** indica se la traccia è abilitata per la riproduzione.</span><span class="sxs-lookup"><span data-stu-id="e8184-105">The **CDTrackEnabled** attribute indicates whether the track is enabled for playback.</span></span>

## <a name="applies-to"></a><span data-ttu-id="e8184-106">Si applica a</span><span class="sxs-lookup"><span data-stu-id="e8184-106">Applies To</span></span>

-   [<span data-ttu-id="e8184-107">Tracce CD</span><span class="sxs-lookup"><span data-stu-id="e8184-107">CD Tracks</span></span>](cd-track-attributes.md)

## <a name="remarks"></a><span data-ttu-id="e8184-108">Commenti</span><span class="sxs-lookup"><span data-stu-id="e8184-108">Remarks</span></span>

<span data-ttu-id="e8184-109">Questo attributo viene archiviato solo nella cache della libreria.</span><span class="sxs-lookup"><span data-stu-id="e8184-109">This attribute is stored only in the library cache.</span></span>

<span data-ttu-id="e8184-110">Quando si riproduce un CD in Windows Media Player, l'utente può selezionare una traccia e specificare che non deve essere riprodotta.</span><span class="sxs-lookup"><span data-stu-id="e8184-110">When playing a CD in Windows Media Player, the user may select a track and specify that it should not be played.</span></span> <span data-ttu-id="e8184-111">Questo valore di questo attributo è true se la traccia può essere riprodotta oppure false se l'utente ha specificato che la traccia non deve essere riprodotta.</span><span class="sxs-lookup"><span data-stu-id="e8184-111">This value of this attribute is True if the track can be played, or False if the user specified that the track should not be played.</span></span>

<span data-ttu-id="e8184-112">Per determinare se è possibile modificare il valore di questo attributo, usare il metodo [Media. isReadOnlyItem](media-isreadonlyitem.md) .</span><span class="sxs-lookup"><span data-stu-id="e8184-112">To determine whether you can change the value of this attribute, use the [Media.isReadOnlyItem](media-isreadonlyitem.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="e8184-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e8184-113">Requirements</span></span>



| <span data-ttu-id="e8184-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="e8184-114">Requirement</span></span> | <span data-ttu-id="e8184-115">Valore</span><span class="sxs-lookup"><span data-stu-id="e8184-115">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="e8184-116">Versione</span><span class="sxs-lookup"><span data-stu-id="e8184-116">Version</span></span><br/> | <span data-ttu-id="e8184-117">Windows Media Player 9 serie o versione successiva</span><span class="sxs-lookup"><span data-stu-id="e8184-117">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e8184-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e8184-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e8184-119">**Riferimento agli attributi**</span><span class="sxs-lookup"><span data-stu-id="e8184-119">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> </dl>

 

 






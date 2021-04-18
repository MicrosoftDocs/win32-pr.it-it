---
description: Le costanti del flag di bit PHONEBUTTONSTATE descrivono le posizioni dei pulsanti.
ms.assetid: f1196e31-65c6-4ade-a0b7-c7758ce97be1
title: Costanti PHONEBUTTONSTATE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2b1cc2f669fb5c1171834f46e11a161e9390eab
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333953"
---
# <a name="phonebuttonstate_-constants"></a><span data-ttu-id="0d131-103">Costanti PHONEBUTTONSTATE_</span><span class="sxs-lookup"><span data-stu-id="0d131-103">PHONEBUTTONSTATE_ Constants</span></span>

<span data-ttu-id="0d131-104">Le costanti del flag di bit **PHONEBUTTONSTATE_** descrivono le posizioni del pulsante.</span><span class="sxs-lookup"><span data-stu-id="0d131-104">The **PHONEBUTTONSTATE_** bit-flag constants describe the button's positions.</span></span>

<dl> <dt>

<span data-ttu-id="0d131-105"><span id="PHONEBUTTONSTATE_DOWN"></span><span id="phonebuttonstate_down"></span>**PHONEBUTTONSTATE_DOWN**</span><span class="sxs-lookup"><span data-stu-id="0d131-105"><span id="PHONEBUTTONSTATE_DOWN"></span><span id="phonebuttonstate_down"></span>**PHONEBUTTONSTATE_DOWN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="0d131-106">Il pulsante si trova nello stato "giù" (premuto).</span><span class="sxs-lookup"><span data-stu-id="0d131-106">The button is in the "down" state (pressed down).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0d131-107"><span id="PHONEBUTTONSTATE_UNAVAIL"></span><span id="phonebuttonstate_unavail"></span>**PHONEBUTTONSTATE_UNAVAIL**</span><span class="sxs-lookup"><span data-stu-id="0d131-107"><span id="PHONEBUTTONSTATE_UNAVAIL"></span><span id="phonebuttonstate_unavail"></span>**PHONEBUTTONSTATE_UNAVAIL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="0d131-108">Indica che lo stato verso l'alto o verso il basso del pulsante non è noto al provider di servizi e non verrà più conosciuto in un momento successivo.</span><span class="sxs-lookup"><span data-stu-id="0d131-108">Indicates that the up or down state of the button is not known to the service provider, and will not become known at a future time.</span></span> <span data-ttu-id="0d131-109">(Versioni TAPI 1,4 e successive)</span><span class="sxs-lookup"><span data-stu-id="0d131-109">(TAPI versions 1.4 and later)</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0d131-110"><span id="PHONEBUTTONSTATE_UNKNOWN"></span><span id="phonebuttonstate_unknown"></span>**PHONEBUTTONSTATE_UNKNOWN**</span><span class="sxs-lookup"><span data-stu-id="0d131-110"><span id="PHONEBUTTONSTATE_UNKNOWN"></span><span id="phonebuttonstate_unknown"></span>**PHONEBUTTONSTATE_UNKNOWN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="0d131-111">Indica che lo stato verso l'alto o verso il basso del pulsante non è noto in questo momento, ma può diventare noto in un momento successivo.</span><span class="sxs-lookup"><span data-stu-id="0d131-111">Indicates that the up or down state of the button is not known at this time, but may become known at a future time.</span></span> <span data-ttu-id="0d131-112">(Versioni TAPI 1,4 e successive)</span><span class="sxs-lookup"><span data-stu-id="0d131-112">(TAPI versions 1.4 and later)</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0d131-113"><span id="PHONEBUTTONSTATE_UP"></span><span id="phonebuttonstate_up"></span>**PHONEBUTTONSTATE_UP**</span><span class="sxs-lookup"><span data-stu-id="0d131-113"><span id="PHONEBUTTONSTATE_UP"></span><span id="phonebuttonstate_up"></span>**PHONEBUTTONSTATE_UP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="0d131-114">Il pulsante si trova nello stato "up".</span><span class="sxs-lookup"><span data-stu-id="0d131-114">The button is in the "up" state.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0d131-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="0d131-115">Remarks</span></span>

<span data-ttu-id="0d131-116">Nessuna estensibilità.</span><span class="sxs-lookup"><span data-stu-id="0d131-116">No extensibility.</span></span> <span data-ttu-id="0d131-117">Tutti i 32 bit sono riservati.</span><span class="sxs-lookup"><span data-stu-id="0d131-117">All 32 bits are reserved.</span></span>

<span data-ttu-id="0d131-118">Per compatibilità con le versioni precedenti, è responsabilità del provider di servizi esaminare la versione dell'API negoziata sul telefono e non usare i valori PHONEBUTTONSTATE_ non supportati dalla versione negoziata.</span><span class="sxs-lookup"><span data-stu-id="0d131-118">For backward compatibility, it is the responsibility of the service provider to examine the negotiated API version on the phone, and to not use those PHONEBUTTONSTATE_ values that the negotiated version does not support.</span></span>

## <a name="requirements"></a><span data-ttu-id="0d131-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0d131-119">Requirements</span></span>



| <span data-ttu-id="0d131-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="0d131-120">Requirement</span></span> | <span data-ttu-id="0d131-121">Valore</span><span class="sxs-lookup"><span data-stu-id="0d131-121">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="0d131-122">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="0d131-122">TAPI version</span></span><br/> | <span data-ttu-id="0d131-123">Richiede TAPI 2,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="0d131-123">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="0d131-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0d131-124">Header</span></span><br/>       | <dl> <span data-ttu-id="0d131-125"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="0d131-125"><dt>Tapi.h</dt></span></span> </dl> |



 

 





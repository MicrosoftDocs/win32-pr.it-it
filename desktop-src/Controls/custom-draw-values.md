---
title: Valori di estrazione personalizzati (CommCtrl. h)
description: In questa sezione vengono elencati i valori utilizzati per identificare le parti di un controllo TrackBar.
ms.assetid: 154321c7-99f8-4ed5-a5ff-fb96126b43c7
topic_type:
- apiref
api_name:
- TBCD_CHANNEL
- TBCD_THUMB
- TBCD_TICS
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ccf05ab951fdc83ec5be414688be56d710ba0d98
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327247"
---
# <a name="custom-draw-values"></a><span data-ttu-id="3497e-103">Valori di estrazione personalizzati</span><span class="sxs-lookup"><span data-stu-id="3497e-103">Custom Draw Values</span></span>

<span data-ttu-id="3497e-104">In questa sezione vengono elencati i valori utilizzati per identificare le parti di un controllo TrackBar.</span><span class="sxs-lookup"><span data-stu-id="3497e-104">This section lists the values used to identify a Trackbar control's parts.</span></span>



| <span data-ttu-id="3497e-105">Costante</span><span class="sxs-lookup"><span data-stu-id="3497e-105">Constant</span></span>                                                                                                                                                   | <span data-ttu-id="3497e-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3497e-106">Description</span></span>                                                                                                     |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------|
| <span id="TBCD_CHANNEL"></span><span id="tbcd_channel"></span><dl> <span data-ttu-id="3497e-107"><dt>**\_canale TBCD**</dt></span><span class="sxs-lookup"><span data-stu-id="3497e-107"><dt>**TBCD\_CHANNEL**</dt></span></span> </dl> | <span data-ttu-id="3497e-108">Identifica il canale con cui scorre il marcatore Thumb del controllo TrackBar.</span><span class="sxs-lookup"><span data-stu-id="3497e-108">Identifies the channel that the trackbar control's thumb marker slides along.</span></span><br/>                        |
| <span id="TBCD_THUMB"></span><span id="tbcd_thumb"></span><dl> <span data-ttu-id="3497e-109"><dt>**TBCD \_ Thumb**</dt></span><span class="sxs-lookup"><span data-stu-id="3497e-109"><dt>**TBCD\_THUMB**</dt></span></span> </dl>       | <span data-ttu-id="3497e-110">Identifica il marcatore Thumb del controllo TrackBar.</span><span class="sxs-lookup"><span data-stu-id="3497e-110">Identifies the trackbar control's thumb marker.</span></span> <span data-ttu-id="3497e-111">Questa è la parte del controllo che l'utente sposta.</span><span class="sxs-lookup"><span data-stu-id="3497e-111">This is the part of the control that the user moves.</span></span><br/> |
| <span id="TBCD_TICS"></span><span id="tbcd_tics"></span><dl> <span data-ttu-id="3497e-112"><dt>**\_TIC TBCD**</dt></span><span class="sxs-lookup"><span data-stu-id="3497e-112"><dt>**TBCD\_TICS**</dt></span></span> </dl>          | <span data-ttu-id="3497e-113">Identifica i segni di graduazione visualizzati lungo il bordo del controllo TrackBar.</span><span class="sxs-lookup"><span data-stu-id="3497e-113">Identifies the tick marks that are displayed along the trackbar control's edge.</span></span><br/>                      |



## <a name="remarks"></a><span data-ttu-id="3497e-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="3497e-114">Remarks</span></span>

<span data-ttu-id="3497e-115">I valori di estrazione personalizzati, ad esempio, vengono specificati nel membro **dwItemSpec** della struttura [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) .</span><span class="sxs-lookup"><span data-stu-id="3497e-115">Custom Draw values, for example, are specified in the **dwItemSpec** member of the [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="3497e-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3497e-116">Requirements</span></span>



| <span data-ttu-id="3497e-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="3497e-117">Requirement</span></span> | <span data-ttu-id="3497e-118">Valore</span><span class="sxs-lookup"><span data-stu-id="3497e-118">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3497e-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3497e-119">Header</span></span><br/> | <dl> <span data-ttu-id="3497e-120"><dt>CommCtrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="3497e-120"><dt>CommCtrl.h</dt></span></span> </dl> |



 

 






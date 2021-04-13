---
title: Costanti del registro eventi di Windows (WinEvt. h)
description: Il registro eventi di Windows definisce le costanti seguenti
ms.assetid: d3a4a136-ca33-4dad-95ad-af1be6687843
topic_type:
- apiref
api_name:
- EVT_VARIANT_TYPE_MASK
- EVT_VARIANT_TYPE_ARRAY
- EVT_READ_ACCESS
- EVT_WRITE_ACCESS
- EVT_CLEAR_ACCESS
- EVT_ALL_ACCESS
api_location:
- WinEvt.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d592cea0eb1738f5ee04ce53faa9a5fa06c0d52a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400601"
---
# <a name="windows-event-log-constants"></a><span data-ttu-id="b2f9a-103">Costanti registro eventi di Windows</span><span class="sxs-lookup"><span data-stu-id="b2f9a-103">Windows Event Log Constants</span></span>

<span data-ttu-id="b2f9a-104">Nel registro eventi di Windows sono definite le costanti seguenti:</span><span class="sxs-lookup"><span data-stu-id="b2f9a-104">Windows Event Log defines the following constants:</span></span>

<dl> <dt>

<span data-ttu-id="b2f9a-105"><span id="EVT_VARIANT_TYPE_MASK"></span><span id="evt_variant_type_mask"></span>**\_ \_ maschera tipo variante \_ evt**</span><span class="sxs-lookup"><span data-stu-id="b2f9a-105"><span id="EVT_VARIANT_TYPE_MASK"></span><span id="evt_variant_type_mask"></span>**EVT\_VARIANT\_TYPE\_MASK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2f9a-106">0x7F</span><span class="sxs-lookup"><span data-stu-id="b2f9a-106">0x7f</span></span>
</dt> <dt>



<span data-ttu-id="b2f9a-107">Maschera di bit utilizzata per mascherare il bit di matrice del tipo Variant, in modo che sia possibile determinare il tipo di dati del valore Variant contenuto nella struttura [**\_ Variant evt**](/windows/desktop/api/WinEvt/ns-winevt-evt_variant) .</span><span class="sxs-lookup"><span data-stu-id="b2f9a-107">A bitmask that you use to mask out the array bit of the variant type, so you can determine the data type of the variant value that the [**EVT\_VARIANT**](/windows/desktop/api/WinEvt/ns-winevt-evt_variant) structure contains.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b2f9a-108"><span id="EVT_VARIANT_TYPE_ARRAY"></span><span id="evt_variant_type_array"></span>**\_matrice di \_ tipi \_ Variant evt**</span><span class="sxs-lookup"><span data-stu-id="b2f9a-108"><span id="EVT_VARIANT_TYPE_ARRAY"></span><span id="evt_variant_type_array"></span>**EVT\_VARIANT\_TYPE\_ARRAY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2f9a-109">128</span><span class="sxs-lookup"><span data-stu-id="b2f9a-109">128</span></span>
</dt> <dt>



<span data-ttu-id="b2f9a-110">Questo bit è impostato per il membro del **tipo** della struttura [**\_ Variant evt**](/windows/desktop/api/WinEvt/ns-winevt-evt_variant) se la variante contiene un puntatore a una matrice di valori, anziché il valore stesso.</span><span class="sxs-lookup"><span data-stu-id="b2f9a-110">The **Type** member of the [**EVT\_VARIANT**](/windows/desktop/api/WinEvt/ns-winevt-evt_variant) structure has this bit set if the variant contains a pointer to an array of values, rather than the value itself.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b2f9a-111"><span id="EVT_READ_ACCESS"></span><span id="evt_read_access"></span>**\_accesso in lettura evt \_**</span><span class="sxs-lookup"><span data-stu-id="b2f9a-111"><span id="EVT_READ_ACCESS"></span><span id="evt_read_access"></span>**EVT\_READ\_ACCESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2f9a-112">0x1</span><span class="sxs-lookup"><span data-stu-id="b2f9a-112">0x1</span></span>
</dt> <dt>



<span data-ttu-id="b2f9a-113">Autorizzazione di controllo di accesso in lettura che consente di leggere le informazioni da un log eventi.</span><span class="sxs-lookup"><span data-stu-id="b2f9a-113">Read access control permission that allows information to be read from an event log.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b2f9a-114"><span id="EVT_WRITE_ACCESS"></span><span id="evt_write_access"></span>**\_accesso in scrittura a evt \_**</span><span class="sxs-lookup"><span data-stu-id="b2f9a-114"><span id="EVT_WRITE_ACCESS"></span><span id="evt_write_access"></span>**EVT\_WRITE\_ACCESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2f9a-115">0x2</span><span class="sxs-lookup"><span data-stu-id="b2f9a-115">0x2</span></span>
</dt> <dt>



<span data-ttu-id="b2f9a-116">Autorizzazione di controllo di accesso in scrittura che consente la scrittura di informazioni in un log eventi.</span><span class="sxs-lookup"><span data-stu-id="b2f9a-116">Write access control permission that allows information to be written to an event log.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b2f9a-117"><span id="EVT_CLEAR_ACCESS"></span><span id="evt_clear_access"></span>**\_accesso evt Clear \_**</span><span class="sxs-lookup"><span data-stu-id="b2f9a-117"><span id="EVT_CLEAR_ACCESS"></span><span id="evt_clear_access"></span>**EVT\_CLEAR\_ACCESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2f9a-118">0x4</span><span class="sxs-lookup"><span data-stu-id="b2f9a-118">0x4</span></span>
</dt> <dt>



<span data-ttu-id="b2f9a-119">Deselezionare l'autorizzazione di controllo di accesso che consente la cancellazione di tutte le informazioni da un log eventi.</span><span class="sxs-lookup"><span data-stu-id="b2f9a-119">Clear access control permission that allows all information to be cleared from an event log.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b2f9a-120"><span id="EVT_ALL_ACCESS"></span><span id="evt_all_access"></span>**EVT \_ tutti gli \_ accessi**</span><span class="sxs-lookup"><span data-stu-id="b2f9a-120"><span id="EVT_ALL_ACCESS"></span><span id="evt_all_access"></span>**EVT\_ALL\_ACCESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2f9a-121">0x7</span><span class="sxs-lookup"><span data-stu-id="b2f9a-121">0x7</span></span>
</dt> <dt>



<span data-ttu-id="b2f9a-122">All (lettura, scrittura, cancellazione ed eliminazione) autorizzazione di controllo di accesso.</span><span class="sxs-lookup"><span data-stu-id="b2f9a-122">All (read, write, clear, and delete) access control permission.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b2f9a-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b2f9a-123">Requirements</span></span>



| <span data-ttu-id="b2f9a-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="b2f9a-124">Requirement</span></span> | <span data-ttu-id="b2f9a-125">Valore</span><span class="sxs-lookup"><span data-stu-id="b2f9a-125">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="b2f9a-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b2f9a-126">Minimum supported client</span></span><br/> | <span data-ttu-id="b2f9a-127">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b2f9a-127">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="b2f9a-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b2f9a-128">Minimum supported server</span></span><br/> | <span data-ttu-id="b2f9a-129">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="b2f9a-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="b2f9a-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b2f9a-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="b2f9a-131"><dt>WinEvt. h</dt></span><span class="sxs-lookup"><span data-stu-id="b2f9a-131"><dt>WinEvt.h</dt></span></span> </dl> |



 

 






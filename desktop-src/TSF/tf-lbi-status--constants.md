---
title: Costanti TF_LBI_STATUS_ (Ctfutb. h)
description: Le \_ costanti TF LBI \_ status \_ \ indicano lo stato di un elemento della barra della lingua. Questi valori vengono usati con il metodo ITfLangBarItem GetStatus.
ms.assetid: 5f2c0e61-f7e5-4dcc-86a3-7bd1c994b8bc
topic_type:
- apiref
api_name:
- TF_LBI_STATUS_HIDDEN
- TF_LBI_STATUS_DISABLED
- TF_LBI_STATUS_BTN_TOGGLED
api_location:
- Ctfutb.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7de9dcf0272eaf79fd001461aa555d78c9d6ae30
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742922"
---
# <a name="tf_lbi_status_-constants"></a><span data-ttu-id="26625-104">\_Costanti di \_ stato TF LBI \_ \*</span><span class="sxs-lookup"><span data-stu-id="26625-104">TF\_LBI\_STATUS\_\* Constants</span></span>

<span data-ttu-id="26625-105">Le costanti \*\* \_ tf \_ LBI \_ \* status\* _ indicano lo stato di un elemento della barra della lingua.</span><span class="sxs-lookup"><span data-stu-id="26625-105">The \**TF\_LBI\_STATUS\_\** _ constants indicate the status of a language bar item.</span></span> <span data-ttu-id="26625-106">Questi valori vengono usati con il metodo [ITfLangBarItem:: GetStatus](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritem-getstatus) .</span><span class="sxs-lookup"><span data-stu-id="26625-106">These values are used with the [ITfLangBarItem::GetStatus](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritem-getstatus) method.</span></span>



| <span data-ttu-id="26625-107">Costante/valore</span><span class="sxs-lookup"><span data-stu-id="26625-107">Constant/value</span></span>                                                                                                                                                                                                                                                       | <span data-ttu-id="26625-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="26625-108">Description</span></span>                                                                                                                                       |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TF_LBI_STATUS_HIDDEN"></span><span id="tf_lbi_status_hidden"></span><dl> <span data-ttu-id="26625-109"><dt>_ \* TF \_ \_Stato LBI \_ nascosto \* \*</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="26625-109"><dt>_\*TF\_LBI\_STATUS\_HIDDEN\*\*</dt> <dt>0x00000001</dt></span></span> </dl>                 | <span data-ttu-id="26625-110">L'elemento è nascosto.</span><span class="sxs-lookup"><span data-stu-id="26625-110">The item is hidden.</span></span> <span data-ttu-id="26625-111">Questo stile viene ignorato se l'elemento non include lo stile HIDDENSTATUSCONTROL di TF \_ LBI \_ Style \_ .</span><span class="sxs-lookup"><span data-stu-id="26625-111">This style is ignored if the item does not include the TF\_LBI\_STYLE\_HIDDENSTATUSCONTROL style.</span></span><br/>                  |
| <span id="TF_LBI_STATUS_DISABLED"></span><span id="tf_lbi_status_disabled"></span><dl> <span data-ttu-id="26625-112"><dt>**Tf \_ \_Stato LBI \_ disabilitato**</dt> <dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="26625-112"><dt>**TF\_LBI\_STATUS\_DISABLED**</dt> <dt>0x00000002</dt></span></span> </dl>           | <span data-ttu-id="26625-113">L'elemento è disabilitato.</span><span class="sxs-lookup"><span data-stu-id="26625-113">The item is disabled.</span></span><br/>                                                                                                                  |
| <span id="TF_LBI_STATUS_BTN_TOGGLED"></span><span id="tf_lbi_status_btn_toggled"></span><dl> <span data-ttu-id="26625-114"><dt>**Tf \_ LBI \_ stato \_ BTN \_ attivato/disattivato**</dt> <dt>0x00010000</dt></span><span class="sxs-lookup"><span data-stu-id="26625-114"><dt>**TF\_LBI\_STATUS\_BTN\_TOGGLED**</dt> <dt>0x00010000</dt></span></span> </dl> | <span data-ttu-id="26625-115">L'elemento è nello stato attivato o disattivato.</span><span class="sxs-lookup"><span data-stu-id="26625-115">The item is in the toggled or pressed state.</span></span> <span data-ttu-id="26625-116">Questo stile viene ignorato se l'elemento non include lo stile di \_ \_ interruttore BTN stile TF LBI \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="26625-116">This style is ignored if the item does not include the TF\_LBI\_STYLE\_BTN\_TOGGLE style.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="26625-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="26625-117">Requirements</span></span>



| <span data-ttu-id="26625-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="26625-118">Requirement</span></span> | <span data-ttu-id="26625-119">Valore</span><span class="sxs-lookup"><span data-stu-id="26625-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="26625-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="26625-120">Minimum supported client</span></span><br/> | <span data-ttu-id="26625-121">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="26625-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="26625-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="26625-122">Minimum supported server</span></span><br/> | <span data-ttu-id="26625-123">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="26625-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="26625-124">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="26625-124">Redistributable</span></span><br/>          | <span data-ttu-id="26625-125">TSF 1,0 su Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="26625-125">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                       |
| <span data-ttu-id="26625-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="26625-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="26625-127"><dt>Ctfutb. h</dt></span><span class="sxs-lookup"><span data-stu-id="26625-127"><dt>Ctfutb.h</dt></span></span> </dl>   |
| <span data-ttu-id="26625-128">IDL</span><span class="sxs-lookup"><span data-stu-id="26625-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="26625-129"><dt>Ctfutb. idl</dt></span><span class="sxs-lookup"><span data-stu-id="26625-129"><dt>Ctfutb.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="26625-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="26625-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="26625-131">ITfLangBarItem:: GetStatus</span><span class="sxs-lookup"><span data-stu-id="26625-131">ITfLangBarItem::GetStatus</span></span>](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritem-getstatus)
</dt> </dl>

 

 






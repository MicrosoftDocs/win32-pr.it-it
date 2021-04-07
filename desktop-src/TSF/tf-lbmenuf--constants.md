---
title: Costanti TF_LBMENUF_ (Ctfutb. h)
description: Le \_ costanti TF LBMENUF \_ \ vengono usate nel metodo AddMenuItem di ITfMenu per specificare le caratteristiche di una voce di menu nella barra della lingua.
ms.assetid: f8f3f397-b84e-4635-b454-31369c679ce2
topic_type:
- apiref
api_name:
- TF_LBMENUF_CHECKED
- TF_LBMENUF_SUBMENU
- TF_LBMENUF_SEPARATOR
- TF_LBMENUF_RADIOCHECKED
- TF_LBMENUF_GRAYED
api_location:
- Ctfutb.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a1a056e9a758419965341b4d508db083fc8f31b4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964174"
---
# <a name="tf_lbmenuf_-constants"></a><span data-ttu-id="ca28e-103">\_Costanti LBMENUF \_ \* TF</span><span class="sxs-lookup"><span data-stu-id="ca28e-103">TF\_LBMENUF\_\* Constants</span></span>

<span data-ttu-id="ca28e-104">Le costanti \*\* \_ tf \_ \* LBMENUF\* _ vengono usate nel metodo [ITfMenu:: AddMenuItem](/windows/desktop/api/Ctfutb/nf-ctfutb-itfmenu-addmenuitem) per specificare le caratteristiche di una voce di menu nella barra della lingua.</span><span class="sxs-lookup"><span data-stu-id="ca28e-104">The \**TF\_LBMENUF\_\** _ constants are used in the [ITfMenu::AddMenuItem](/windows/desktop/api/Ctfutb/nf-ctfutb-itfmenu-addmenuitem) method to specify the characteristics of a menu item in the language bar.</span></span>



| <span data-ttu-id="ca28e-105">Costante/valore</span><span class="sxs-lookup"><span data-stu-id="ca28e-105">Constant/value</span></span>                                                                                                                                                                                                                                         | <span data-ttu-id="ca28e-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ca28e-106">Description</span></span>                                     |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------|
| <span id="TF_LBMENUF_CHECKED"></span><span id="tf_lbmenuf_checked"></span><dl> <span data-ttu-id="ca28e-107"><dt>_ \* TF \_ LBMENUF \_ selezionato \* \*</dt> <dt>0x01</dt></span><span class="sxs-lookup"><span data-stu-id="ca28e-107"><dt>_\*TF\_LBMENUF\_CHECKED\*\*</dt> <dt>0x01</dt></span></span> </dl>                | <span data-ttu-id="ca28e-108">La voce di menu è selezionata.</span><span class="sxs-lookup"><span data-stu-id="ca28e-108">The menu item is checked.</span></span><br/>            |
| <span id="TF_LBMENUF_SUBMENU"></span><span id="tf_lbmenuf_submenu"></span><dl> <span data-ttu-id="ca28e-109"><dt>**Tf \_ \_Sottomenu LBMENUF**</dt> <dt>0x02</dt></span><span class="sxs-lookup"><span data-stu-id="ca28e-109"><dt>**TF\_LBMENUF\_SUBMENU**</dt> <dt>0x02</dt></span></span> </dl>                | <span data-ttu-id="ca28e-110">La voce di menu è un sottomenu.</span><span class="sxs-lookup"><span data-stu-id="ca28e-110">The menu item is a submenu.</span></span><br/>          |
| <span id="TF_LBMENUF_SEPARATOR"></span><span id="tf_lbmenuf_separator"></span><dl> <span data-ttu-id="ca28e-111"><dt>**Tf \_ 0x04 \_ separatore LBMENUF**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="ca28e-111"><dt>**TF\_LBMENUF\_SEPARATOR**</dt> <dt>0x04</dt></span></span> </dl>          | <span data-ttu-id="ca28e-112">La voce di menu è un separatore.</span><span class="sxs-lookup"><span data-stu-id="ca28e-112">The menu item is a separator.</span></span><br/>        |
| <span id="TF_LBMENUF_RADIOCHECKED"></span><span id="tf_lbmenuf_radiochecked"></span><dl> <span data-ttu-id="ca28e-113"><dt>**Tf \_ LBMENUF \_ RADIOchecked**</dt> <dt>0x08</dt></span><span class="sxs-lookup"><span data-stu-id="ca28e-113"><dt>**TF\_LBMENUF\_RADIOCHECKED**</dt> <dt>0x08</dt></span></span> </dl> | <span data-ttu-id="ca28e-114">La voce di menu è un segno di spunta radio.</span><span class="sxs-lookup"><span data-stu-id="ca28e-114">The menu item is a radio check mark.</span></span><br/> |
| <span id="TF_LBMENUF_GRAYED"></span><span id="tf_lbmenuf_grayed"></span><dl> <span data-ttu-id="ca28e-115"><dt>**Tf \_ LBMENUF \_ grigio**</dt> <dt>0x10</dt></span><span class="sxs-lookup"><span data-stu-id="ca28e-115"><dt>**TF\_LBMENUF\_GRAYED**</dt> <dt>0x10</dt></span></span> </dl>                   | <span data-ttu-id="ca28e-116">La voce di menu è disabilitata.</span><span class="sxs-lookup"><span data-stu-id="ca28e-116">The menu item is disabled.</span></span><br/>           |



## <a name="requirements"></a><span data-ttu-id="ca28e-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ca28e-117">Requirements</span></span>



| <span data-ttu-id="ca28e-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="ca28e-118">Requirement</span></span> | <span data-ttu-id="ca28e-119">Valore</span><span class="sxs-lookup"><span data-stu-id="ca28e-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ca28e-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ca28e-120">Minimum supported client</span></span><br/> | <span data-ttu-id="ca28e-121">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="ca28e-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="ca28e-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ca28e-122">Minimum supported server</span></span><br/> | <span data-ttu-id="ca28e-123">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="ca28e-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ca28e-124">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="ca28e-124">Redistributable</span></span><br/>          | <span data-ttu-id="ca28e-125">TSF 1,0 su Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="ca28e-125">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                       |
| <span data-ttu-id="ca28e-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ca28e-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="ca28e-127"><dt>Ctfutb. h</dt></span><span class="sxs-lookup"><span data-stu-id="ca28e-127"><dt>Ctfutb.h</dt></span></span> </dl>   |
| <span data-ttu-id="ca28e-128">IDL</span><span class="sxs-lookup"><span data-stu-id="ca28e-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="ca28e-129"><dt>Ctfutb. idl</dt></span><span class="sxs-lookup"><span data-stu-id="ca28e-129"><dt>Ctfutb.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ca28e-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ca28e-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ca28e-131">ITfMenu::AddMenuItem</span><span class="sxs-lookup"><span data-stu-id="ca28e-131">ITfMenu::AddMenuItem</span></span>](/windows/desktop/api/Ctfutb/nf-ctfutb-itfmenu-addmenuitem)
</dt> </dl>

 

 






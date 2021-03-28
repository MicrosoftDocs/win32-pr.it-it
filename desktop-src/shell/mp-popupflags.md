---
description: Rappresenta le opzioni disponibili quando si visualizza un menu di scelta rapida.
title: Costanti MP_POPUPFLAGS (ShObjIdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: cc1d9ff0-a03b-4bd3-b481-9b78d20eb771
api_name:
- MPPF_SETFOCUS
- MPPF_INITIALSELECT
- MPPF_NOANIMATE
- MPPF_KEYBOARD
- MPPF_REPOSITION
- MPPF_FORCEZORDER
- MPPF_FINALSELECT
- MPPF_ALIGN_LEFT
- MPPF_ALIGN_RIGHT
- MPPF_TOP
- MPPF_LEFT
- MPPF_RIGHT
- MPPF_BOTTOM
- MPPF_POS_MASK
api_type:
- HeaderDef
api_location:
- Shobjidl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 5d49f848df7749a732e9f0b849d44a9be56a5c3e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130083"
---
# <a name="mp_popupflags-constants"></a><span data-ttu-id="fce36-103">\_Costanti POPUPFLAGS MP</span><span class="sxs-lookup"><span data-stu-id="fce36-103">MP\_POPUPFLAGS constants</span></span>

<span data-ttu-id="fce36-104">Rappresenta le opzioni disponibili quando si visualizza un menu di scelta rapida.</span><span class="sxs-lookup"><span data-stu-id="fce36-104">Represent options available when displaying a pop-up menu.</span></span>



| <span data-ttu-id="fce36-105">Costante/valore</span><span class="sxs-lookup"><span data-stu-id="fce36-105">Constant/value</span></span>                                                                                                                                                                                                                               | <span data-ttu-id="fce36-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fce36-106">Description</span></span>                                                                                                                                                                                                                                                              |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MPPF_SETFOCUS"></span><span id="mppf_setfocus"></span><dl> <span data-ttu-id="fce36-107"><dt>**MPPF \_ SetFocus**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="fce36-107"><dt>**MPPF\_SETFOCUS**</dt> <dt>0x00000001</dt></span></span> </dl>                | <span data-ttu-id="fce36-108">Assegnare al menu di scelta rapida lo stato attivo.</span><span class="sxs-lookup"><span data-stu-id="fce36-108">Give the pop-up menu the focus.</span></span><br/>                                                                                                                                                                                                                               |
| <span id="MPPF_INITIALSELECT"></span><span id="mppf_initialselect"></span><dl> <span data-ttu-id="fce36-109"><dt>**MPPF \_**</dt> <dt>0x00000002</dt> INITIALSELECT</span><span class="sxs-lookup"><span data-stu-id="fce36-109"><dt>**MPPF\_INITIALSELECT**</dt> <dt>0x00000002</dt></span></span> </dl> | <span data-ttu-id="fce36-110">Selezionare il primo elemento nel menu a comparsa.</span><span class="sxs-lookup"><span data-stu-id="fce36-110">Select the first item in the pop-up menu.</span></span><br/>                                                                                                                                                                                                                     |
| <span id="MPPF_NOANIMATE"></span><span id="mppf_noanimate"></span><dl> <span data-ttu-id="fce36-111"><dt>**MPPF \_ Noanimate**</dt> <dt>0x00000004</dt></span><span class="sxs-lookup"><span data-stu-id="fce36-111"><dt>**MPPF\_NOANIMATE**</dt> <dt>0x00000004</dt></span></span> </dl>             | <span data-ttu-id="fce36-112">Non usare le animazioni di sistema predefinite, ad esempio la dissolvenza, quando si Visualizza il menu.</span><span class="sxs-lookup"><span data-stu-id="fce36-112">Do not use the default system animations, for example, fade-in, when displaying the menu.</span></span><br/>                                                                                                                                                                     |
| <span id="MPPF_KEYBOARD"></span><span id="mppf_keyboard"></span><dl> <span data-ttu-id="fce36-113"><dt>**MPPF \_**</dt> <dt>0x00000010</dt> tastiera</span><span class="sxs-lookup"><span data-stu-id="fce36-113"><dt>**MPPF\_KEYBOARD**</dt> <dt>0x00000010</dt></span></span> </dl>                | <span data-ttu-id="fce36-114">Attivare il menu tramite un tasto di scelta rapida.</span><span class="sxs-lookup"><span data-stu-id="fce36-114">Activate the menu by a keyboard shortcut.</span></span><br/>                                                                                                                                                                                                                     |
| <span id="MPPF_REPOSITION"></span><span id="mppf_reposition"></span><dl> <span data-ttu-id="fce36-115"><dt>**MPPF \_ Riposizionare**</dt> <dt>0x00000020</dt></span><span class="sxs-lookup"><span data-stu-id="fce36-115"><dt>**MPPF\_REPOSITION**</dt> <dt>0x00000020</dt></span></span> </dl>          | <span data-ttu-id="fce36-116">Consente di visualizzare la barra in una posizione diversa, in base alle modifiche apportate al menu.</span><span class="sxs-lookup"><span data-stu-id="fce36-116">Display the bar in a different position, based on changes to the menu.</span></span><br/>                                                                                                                                                                                        |
| <span id="MPPF_FORCEZORDER"></span><span id="mppf_forcezorder"></span><dl> <span data-ttu-id="fce36-117"><dt>**MPPF \_**</dt> <dt>0x00000040</dt> FORCEZORDER</span><span class="sxs-lookup"><span data-stu-id="fce36-117"><dt>**MPPF\_FORCEZORDER**</dt> <dt>0x00000040</dt></span></span> </dl>       | <span data-ttu-id="fce36-118">Riservato.</span><span class="sxs-lookup"><span data-stu-id="fce36-118">Reserved.</span></span> <span data-ttu-id="fce36-119">Non usare.</span><span class="sxs-lookup"><span data-stu-id="fce36-119">Do not use.</span></span><br/>                                                                                                                                                                                                                                         |
| <span id="MPPF_FINALSELECT"></span><span id="mppf_finalselect"></span><dl> <span data-ttu-id="fce36-120"><dt>**MPPF \_**</dt> <dt>0x00000080</dt> FINALSELECT</span><span class="sxs-lookup"><span data-stu-id="fce36-120"><dt>**MPPF\_FINALSELECT**</dt> <dt>0x00000080</dt></span></span> </dl>       | <span data-ttu-id="fce36-121">Selezionare l'ultimo elemento nel menu.</span><span class="sxs-lookup"><span data-stu-id="fce36-121">Select the last item in the menu.</span></span><br/>                                                                                                                                                                                                                             |
| <span id="MPPF_ALIGN_LEFT"></span><span id="mppf_align_left"></span><dl> <span data-ttu-id="fce36-122"><dt>**MPPF \_ Allinea \_**</dt> <dt>0x02000000</dt> a sinistra</span><span class="sxs-lookup"><span data-stu-id="fce36-122"><dt>**MPPF\_ALIGN\_LEFT**</dt> <dt>0x02000000</dt></span></span> </dl>         | <span data-ttu-id="fce36-123">**Windows Vista o versione successiva**: allineare il menu a comparsa a sinistra dell'area specificata nel parametro *prcExclude* di [**ITrackShellMenu::P opup**](/windows/desktop/api/Shdeprecated/nf-shdeprecated-itrackshellmenu-popup) o [**IMenuPopup::P opup**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-imenupopup-popup).</span><span class="sxs-lookup"><span data-stu-id="fce36-123">**Windows Vista or later**: Align the pop-up menu to the left of the area specified in the *prcExclude* parameter of [**ITrackShellMenu::Popup**](/windows/desktop/api/Shdeprecated/nf-shdeprecated-itrackshellmenu-popup) or [**IMenuPopup::Popup**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-imenupopup-popup).</span></span> <span data-ttu-id="fce36-124">Si tratta dell'allineamento predefinito.</span><span class="sxs-lookup"><span data-stu-id="fce36-124">This is the default alignment.</span></span><br/> |
| <span id="MPPF_ALIGN_RIGHT"></span><span id="mppf_align_right"></span><dl> <span data-ttu-id="fce36-125"><dt>**MPPF \_ Allinea \_**</dt> <dt>0x04000000</dt> a destra</span><span class="sxs-lookup"><span data-stu-id="fce36-125"><dt>**MPPF\_ALIGN\_RIGHT**</dt> <dt>0x04000000</dt></span></span> </dl>      | <span data-ttu-id="fce36-126">**Windows Vista o versione successiva**: allineare il menu a comparsa a destra dell'area specificata nel parametro *prcExclude* di [**ITrackShellMenu::P opup**](/windows/desktop/api/Shdeprecated/nf-shdeprecated-itrackshellmenu-popup) o [**IMenuPopup::P opup**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-imenupopup-popup).</span><span class="sxs-lookup"><span data-stu-id="fce36-126">**Windows Vista or later**: Align the pop-up menu to the right of the area specified in the *prcExclude* parameter of [**ITrackShellMenu::Popup**](/windows/desktop/api/Shdeprecated/nf-shdeprecated-itrackshellmenu-popup) or [**IMenuPopup::Popup**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-imenupopup-popup).</span></span><br/>                               |
| <span id="MPPF_TOP"></span><span id="mppf_top"></span><dl> <span data-ttu-id="fce36-127"><dt>**MPPF \_ PRIMI**</dt> <dt>0x20000000</dt></span><span class="sxs-lookup"><span data-stu-id="fce36-127"><dt>**MPPF\_TOP**</dt> <dt>0x20000000</dt></span></span> </dl>                               | <span data-ttu-id="fce36-128">Posizionare il menu a comparsa sopra il punto iniziale specificato nel parametro *PPT* di [**ITrackShellMenu::P opup**](/windows/desktop/api/Shdeprecated/nf-shdeprecated-itrackshellmenu-popup) o [**IMenuPopup::P opup**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-imenupopup-popup).</span><span class="sxs-lookup"><span data-stu-id="fce36-128">Position the pop-up menu above the initial point specified in the *ppt* parameter of [**ITrackShellMenu::Popup**](/windows/desktop/api/Shdeprecated/nf-shdeprecated-itrackshellmenu-popup) or [**IMenuPopup::Popup**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-imenupopup-popup).</span></span><br/>                                                                |
| <span id="MPPF_LEFT"></span><span id="mppf_left"></span><dl> <span data-ttu-id="fce36-129"><dt>**MPPF \_**</dt> <dt>0X40000000</dt> a sinistra</span><span class="sxs-lookup"><span data-stu-id="fce36-129"><dt>**MPPF\_LEFT**</dt> <dt>0x40000000</dt></span></span> </dl>                            | <span data-ttu-id="fce36-130">Posizionare il menu a comparsa a sinistra del punto iniziale.</span><span class="sxs-lookup"><span data-stu-id="fce36-130">Position the pop-up menu to the left of the initial point.</span></span><br/>                                                                                                                                                                                                    |
| <span id="MPPF_RIGHT"></span><span id="mppf_right"></span><dl> <span data-ttu-id="fce36-131"><dt>**MPPF \_**</dt> <dt>0x60000000</dt> destro</span><span class="sxs-lookup"><span data-stu-id="fce36-131"><dt>**MPPF\_RIGHT**</dt> <dt>0x60000000</dt></span></span> </dl>                         | <span data-ttu-id="fce36-132">Posizionare il menu a comparsa a destra del punto iniziale.</span><span class="sxs-lookup"><span data-stu-id="fce36-132">Position the pop-up menu to the right of the initial point.</span></span><br/>                                                                                                                                                                                                   |
| <span id="MPPF_BOTTOM"></span><span id="mppf_bottom"></span><dl> <span data-ttu-id="fce36-133"><dt>**MPPF \_ In basso**</dt> <dt>(int) 0x80000000</dt></span><span class="sxs-lookup"><span data-stu-id="fce36-133"><dt>**MPPF\_BOTTOM**</dt> <dt>(int)0x80000000</dt></span></span> </dl>                 | <span data-ttu-id="fce36-134">Posizionare il menu a comparsa sotto il punto iniziale.</span><span class="sxs-lookup"><span data-stu-id="fce36-134">Position the pop-up menu below the initial point.</span></span><br/>                                                                                                                                                                                                             |
| <span id="MPPF_POS_MASK"></span><span id="mppf_pos_mask"></span><dl> <span data-ttu-id="fce36-135"><dt>**MPPF \_ POS \_ mask**</dt> <dt>(int) 0xE0000000</dt></span><span class="sxs-lookup"><span data-stu-id="fce36-135"><dt>**MPPF\_POS\_MASK**</dt> <dt>(int)0xE0000000</dt></span></span> </dl>          | <span data-ttu-id="fce36-136">Maschera della posizione dei menu.</span><span class="sxs-lookup"><span data-stu-id="fce36-136">The menu position mask.</span></span><br/>                                                                                                                                                                                                                                       |



## <a name="remarks"></a><span data-ttu-id="fce36-137">Commenti</span><span class="sxs-lookup"><span data-stu-id="fce36-137">Remarks</span></span>

<span data-ttu-id="fce36-138">Queste costanti sono definite nel file ShObjIdl. h a partire da Windows XP Service Pack 1 (SP1) e Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="fce36-138">These constants are defined in the Shobjidl.h file beginning in Windows XP Service Pack 1 (SP1) and Windows Server 2003</span></span>

## <a name="requirements"></a><span data-ttu-id="fce36-139">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fce36-139">Requirements</span></span>



| <span data-ttu-id="fce36-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="fce36-140">Requirement</span></span> | <span data-ttu-id="fce36-141">Valore</span><span class="sxs-lookup"><span data-stu-id="fce36-141">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fce36-142">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fce36-142">Minimum supported client</span></span><br/> | <span data-ttu-id="fce36-143">Solo app desktop Windows XP con SP1 \[\]</span><span class="sxs-lookup"><span data-stu-id="fce36-143">Windows XP with SP1 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="fce36-144">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fce36-144">Minimum supported server</span></span><br/> | <span data-ttu-id="fce36-145">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="fce36-145">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="fce36-146">Intestazione</span><span class="sxs-lookup"><span data-stu-id="fce36-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="fce36-147"><dt>ShObjIdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="fce36-147"><dt>Shobjidl.h</dt></span></span> </dl>   |
| <span data-ttu-id="fce36-148">IDL</span><span class="sxs-lookup"><span data-stu-id="fce36-148">IDL</span></span><br/>                      | <dl> <span data-ttu-id="fce36-149"><dt>ShObjIdl. idl</dt></span><span class="sxs-lookup"><span data-stu-id="fce36-149"><dt>Shobjidl.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fce36-150">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fce36-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fce36-151">**IMenuPopup::P opup**</span><span class="sxs-lookup"><span data-stu-id="fce36-151">**IMenuPopup::Popup**</span></span>](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-imenupopup-popup)
</dt> <dt>

[<span data-ttu-id="fce36-152">**ITrackShellMenu::P opup**</span><span class="sxs-lookup"><span data-stu-id="fce36-152">**ITrackShellMenu::Popup**</span></span>](/windows/desktop/api/Shdeprecated/nf-shdeprecated-itrackshellmenu-popup)
</dt> </dl>

 

 





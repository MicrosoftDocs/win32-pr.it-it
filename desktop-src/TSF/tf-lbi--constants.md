---
title: Costanti TF_LBI_ (Ctfutb. h)
description: Le \_ costanti TF LBI \_ \ vengono usate con il metodo OnUpdate di ITfLangBarItemSink per indicare quali elementi della barra della lingua sono stati modificati.
ms.assetid: ed84012f-19ba-43b3-bbb5-7373ed174c33
topic_type:
- apiref
api_name:
- TF_LBI_ICON
- TF_LBI_TEXT
- TF_LBI_TOOLTIP
- TF_LBI_BITMAP
- TF_LBI_BALLOON
- TF_LBI_STATUS
- TF_LBI_BMPALL
- TF_LBI_BMPBTNALL
- TF_LBI_BTNALL
api_location:
- Ctfutb.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d72b69f1cb5a5b4a24e78a2bdc1ca0e7a9d79cbf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301345"
---
# <a name="tf_lbi_-constants"></a><span data-ttu-id="a6a33-103">\_Costanti LBI \_ \* TF</span><span class="sxs-lookup"><span data-stu-id="a6a33-103">TF\_LBI\_\* Constants</span></span>

<span data-ttu-id="a6a33-104">Le costanti \*\* \_ tf \_ \* LBI\* _ vengono usate con il metodo [ITfLangBarItemSink:: OnUpdate](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritemsink-onupdate) per indicare quali elementi della barra della lingua sono stati modificati.</span><span class="sxs-lookup"><span data-stu-id="a6a33-104">The \**TF\_LBI\_\** _ constants are used with the [ITfLangBarItemSink::OnUpdate](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritemsink-onupdate) method to indicate which language bar items changed.</span></span>



| <span data-ttu-id="a6a33-105">Costante/valore</span><span class="sxs-lookup"><span data-stu-id="a6a33-105">Constant/value</span></span>                                                                                                                                                                                                                                                                  | <span data-ttu-id="a6a33-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a6a33-106">Description</span></span>                                                                                                                                                                                                                                                                                                         |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TF_LBI_ICON"></span><span id="tf_lbi_icon"></span><dl> <span data-ttu-id="a6a33-107"><dt>_ \* TF \_ Icona di LBI \_ \* \*</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="a6a33-107"><dt>_\*TF\_LBI\_ICON\*\*</dt> <dt>0x00000001</dt></span></span> </dl>                                                        | <span data-ttu-id="a6a33-108">L'icona dell'elemento è stata modificata.</span><span class="sxs-lookup"><span data-stu-id="a6a33-108">The icon of the item has changed.</span></span> <span data-ttu-id="a6a33-109">La barra della lingua chiama [ITfLangBarItemButton:: GetIcon](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritembutton-geticon) in risposta a questa notifica.</span><span class="sxs-lookup"><span data-stu-id="a6a33-109">The language bar calls [ITfLangBarItemButton::GetIcon](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritembutton-geticon) in response to this notification.</span></span><br/>                                                                                                                                             |
| <span id="TF_LBI_TEXT"></span><span id="tf_lbi_text"></span><dl> <span data-ttu-id="a6a33-110"><dt>**Tf \_ 0x00000002 \_ testo LBI**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="a6a33-110"><dt>**TF\_LBI\_TEXT**</dt> <dt>0x00000002</dt></span></span> </dl>                                                        | <span data-ttu-id="a6a33-111">Il testo di un pulsante o di un elemento del pulsante bitmap è stato modificato.</span><span class="sxs-lookup"><span data-stu-id="a6a33-111">The text of a button or bitmap button item has changed.</span></span> <span data-ttu-id="a6a33-112">La barra della lingua chiama [ITfLangBarItemButton:: GetText](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritembutton-gettext) o [ITfLangBarItemBitmapButton:: GetText](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritembitmapbutton-gettext), a seconda del caso appropriato, in risposta a questa notifica.</span><span class="sxs-lookup"><span data-stu-id="a6a33-112">The language bar calls [ITfLangBarItemButton::GetText](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritembutton-gettext) or [ITfLangBarItemBitmapButton::GetText](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritembitmapbutton-gettext), whichever is appropriate, in response to this notification.</span></span><br/>           |
| <span id="TF_LBI_TOOLTIP"></span><span id="tf_lbi_tooltip"></span><dl> <span data-ttu-id="a6a33-113"><dt>**Tf \_ \_Descrizione comando LBI**</dt> <dt>0x00000004</dt></span><span class="sxs-lookup"><span data-stu-id="a6a33-113"><dt>**TF\_LBI\_TOOLTIP**</dt> <dt>0x00000004</dt></span></span> </dl>                                               | <span data-ttu-id="a6a33-114">Testo della descrizione comando dell'elemento modificato.</span><span class="sxs-lookup"><span data-stu-id="a6a33-114">The tooltip text of the item changed.</span></span> <span data-ttu-id="a6a33-115">La barra della lingua chiama [ITfLangBarItem:: GetTooltipString](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritem-gettooltipstring) in risposta a questa notifica.</span><span class="sxs-lookup"><span data-stu-id="a6a33-115">The language bar calls [ITfLangBarItem::GetTooltipString](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritem-gettooltipstring) in response to this notification.</span></span><br/>                                                                                                                                   |
| <span id="TF_LBI_BITMAP"></span><span id="tf_lbi_bitmap"></span><dl> <span data-ttu-id="a6a33-116"><dt>**Tf \_ 0x00000008 \_ bitmap LBI**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="a6a33-116"><dt>**TF\_LBI\_BITMAP**</dt> <dt>0x00000008</dt></span></span> </dl>                                                  | <span data-ttu-id="a6a33-117">Bitmap di una bitmap o di un elemento del pulsante bitmap modificato.</span><span class="sxs-lookup"><span data-stu-id="a6a33-117">The bitmap of a bitmap or bitmap button item changed.</span></span> <span data-ttu-id="a6a33-118">La barra della lingua chiama [ITfLangBarItemBitmap::D rawbitmap](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritembitmap-drawbitmap) o [ITfLangBarItemBitmapButton::D rawbitmap](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritembitmapbutton-drawbitmap), a seconda del caso appropriato, in risposta a questa notifica.</span><span class="sxs-lookup"><span data-stu-id="a6a33-118">The language bar calls [ITfLangBarItemBitmap::DrawBitmap](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritembitmap-drawbitmap) or [ITfLangBarItemBitmapButton::DrawBitmap](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritembitmapbutton-drawbitmap), whichever is appropriate, in response to this notification.</span></span><br/> |
| <span id="TF_LBI_BALLOON"></span><span id="tf_lbi_balloon"></span><dl> <span data-ttu-id="a6a33-119"><dt>**Tf \_ 0x00000010 \_ Balloon LBI**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="a6a33-119"><dt>**TF\_LBI\_BALLOON**</dt> <dt>0x00000010</dt></span></span> </dl>                                               | <span data-ttu-id="a6a33-120">Le informazioni relative a un elemento del fumetto sono state modificate.</span><span class="sxs-lookup"><span data-stu-id="a6a33-120">The information for a balloon item changed.</span></span> <span data-ttu-id="a6a33-121">La barra della lingua chiama [ITfLangBarItemBalloon:: GetBalloonInfo](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritemballoon-getballooninfo) in risposta a questa notifica.</span><span class="sxs-lookup"><span data-stu-id="a6a33-121">The language bar calls [ITfLangBarItemBalloon::GetBalloonInfo](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritemballoon-getballooninfo) in response to this notification.</span></span><br/>                                                                                                                   |
| <span id="TF_LBI_STATUS"></span><span id="tf_lbi_status"></span><dl> <span data-ttu-id="a6a33-122"><dt>**Tf \_ \_Stato LBI**</dt> <dt>0x00010000</dt></span><span class="sxs-lookup"><span data-stu-id="a6a33-122"><dt>**TF\_LBI\_STATUS**</dt> <dt>0x00010000</dt></span></span> </dl>                                                  | <span data-ttu-id="a6a33-123">Lo stato dell'elemento è stato modificato.</span><span class="sxs-lookup"><span data-stu-id="a6a33-123">The item status changed.</span></span> <span data-ttu-id="a6a33-124">La barra della lingua chiama [ITfLangBarItem:: GetStatus](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritem-getstatus) in risposta a questa notifica.</span><span class="sxs-lookup"><span data-stu-id="a6a33-124">The language bar calls [ITfLangBarItem::GetStatus](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritem-getstatus) in response to this notification.</span></span><br/>                                                                                                                                                              |
| <span id="TF_LBI_BMPALL"></span><span id="tf_lbi_bmpall"></span><dl> <span data-ttu-id="a6a33-125"><dt>**Tf \_ LBI \_ BMPALL**</dt> <dt>tf \_ LBI \_ bitmap \| tf \_ LBI \_ TOOLTIP</dt></span><span class="sxs-lookup"><span data-stu-id="a6a33-125"><dt>**TF\_LBI\_BMPALL**</dt> <dt>TF\_LBI\_BITMAP\| TF\_LBI\_TOOLTIP</dt></span></span> </dl>                          | <span data-ttu-id="a6a33-126">Combina la \_ bitmap TF LBI \_ e \_ la \_ Descrizione comando tf LBI.</span><span class="sxs-lookup"><span data-stu-id="a6a33-126">Combines TF\_LBI\_BITMAP and TF\_LBI\_TOOLTIP.</span></span><br/>                                                                                                                                                                                                                                                           |
| <span id="TF_LBI_BMPBTNALL"></span><span id="tf_lbi_bmpbtnall"></span><dl> <span data-ttu-id="a6a33-127"><dt>**Tf \_ LBI \_ BMPBTNALL**</dt> <dt>tf \_ LBI \_ bitmap \| tf \_ LBI \_ Text \| tf \_ LBI \_ TOOLTIP</dt></span><span class="sxs-lookup"><span data-stu-id="a6a33-127"><dt>**TF\_LBI\_BMPBTNALL**</dt> <dt>TF\_LBI\_BITMAP\| TF\_LBI\_TEXT\| TF\_LBI\_TOOLTIP</dt></span></span> </dl> | <span data-ttu-id="a6a33-128">Combina la \_ bitmap TF LBI \_ , il \_ testo TF LBI e la \_ \_ \_ Descrizione comando tf LBI.</span><span class="sxs-lookup"><span data-stu-id="a6a33-128">Combines TF\_LBI\_BITMAP, TF\_LBI\_TEXT and TF\_LBI\_TOOLTIP.</span></span><br/>                                                                                                                                                                                                                                            |
| <span id="TF_LBI_BTNALL"></span><span id="tf_lbi_btnall"></span><dl> <span data-ttu-id="a6a33-129"><dt>**Tf \_ LBI \_ BTNALL**</dt> <dt>tf \_ LBI \_ Icon \| tf \_ LBI \_ Text \| tf \_ LBI \_ TOOLTIP</dt></span><span class="sxs-lookup"><span data-stu-id="a6a33-129"><dt>**TF\_LBI\_BTNALL**</dt> <dt>TF\_LBI\_ICON\| TF\_LBI\_TEXT\| TF\_LBI\_TOOLTIP</dt></span></span> </dl>            | <span data-ttu-id="a6a33-130">Combina l' \_ icona TF LBI \_ , il \_ testo TF LBI e la \_ \_ \_ Descrizione comando tf LBI.</span><span class="sxs-lookup"><span data-stu-id="a6a33-130">Combines TF\_LBI\_ICON, TF\_LBI\_TEXT and TF\_LBI\_TOOLTIP.</span></span><br/>                                                                                                                                                                                                                                              |



## <a name="requirements"></a><span data-ttu-id="a6a33-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a6a33-131">Requirements</span></span>



| <span data-ttu-id="a6a33-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="a6a33-132">Requirement</span></span> | <span data-ttu-id="a6a33-133">Valore</span><span class="sxs-lookup"><span data-stu-id="a6a33-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a6a33-134">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a6a33-134">Minimum supported client</span></span><br/> | <span data-ttu-id="a6a33-135">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="a6a33-135">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="a6a33-136">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a6a33-136">Minimum supported server</span></span><br/> | <span data-ttu-id="a6a33-137">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="a6a33-137">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a6a33-138">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="a6a33-138">Redistributable</span></span><br/>          | <span data-ttu-id="a6a33-139">TSF 1,0 su Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="a6a33-139">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                       |
| <span data-ttu-id="a6a33-140">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a6a33-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="a6a33-141"><dt>Ctfutb. h</dt></span><span class="sxs-lookup"><span data-stu-id="a6a33-141"><dt>Ctfutb.h</dt></span></span> </dl>   |
| <span data-ttu-id="a6a33-142">IDL</span><span class="sxs-lookup"><span data-stu-id="a6a33-142">IDL</span></span><br/>                      | <dl> <span data-ttu-id="a6a33-143"><dt>Ctfutb. idl</dt></span><span class="sxs-lookup"><span data-stu-id="a6a33-143"><dt>Ctfutb.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a6a33-144">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a6a33-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a6a33-145">ITfLangBarItemSink:: OnUpdate</span><span class="sxs-lookup"><span data-stu-id="a6a33-145">ITfLangBarItemSink::OnUpdate</span></span>](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritemsink-onupdate)
</dt> </dl>

 

 






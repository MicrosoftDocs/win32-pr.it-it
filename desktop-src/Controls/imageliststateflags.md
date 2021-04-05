---
title: IMAGELISTSTATEFLAGS (COMmctrl. h)
description: I flag seguenti vengono passati al metodo di IImageList di richiamo nel membro fState di IMAGELISTDRAWPARAMS.
ms.assetid: a22b4acf-c290-44b2-9216-b006d0326236
topic_type:
- apiref
api_name:
- ILS_NORMAL
- ILS_GLOW
- ILS_SHADOW
- ILS_SATURATE
- ILS_ALPHA
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fea580294f54b6e2fc5c3e5b6aee1119811c22e8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048199"
---
# <a name="imageliststateflags"></a><span data-ttu-id="30cc1-103">IMAGELISTSTATEFLAGS</span><span class="sxs-lookup"><span data-stu-id="30cc1-103">IMAGELISTSTATEFLAGS</span></span>

<span data-ttu-id="30cc1-104">I flag seguenti vengono passati al metodo [**IImageList::D RAW**](/windows/desktop/api/CommonControls/nf-commoncontrols-iimagelist-draw) nel membro **fState** di [**IMAGELISTDRAWPARAMS**](/windows/win32/api/commctrl/ns-commctrl-imagelistdrawparams).</span><span class="sxs-lookup"><span data-stu-id="30cc1-104">The following flags are passed to the [**IImageList::Draw**](/windows/desktop/api/CommonControls/nf-commoncontrols-iimagelist-draw) method in the **fState** member of [**IMAGELISTDRAWPARAMS**](/windows/win32/api/commctrl/ns-commctrl-imagelistdrawparams).</span></span>



| <span data-ttu-id="30cc1-105">Costante/valore</span><span class="sxs-lookup"><span data-stu-id="30cc1-105">Constant/value</span></span>                                                                                                                                                                                                             | <span data-ttu-id="30cc1-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="30cc1-106">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                   |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="ILS_NORMAL"></span><span id="ils_normal"></span><dl> <span data-ttu-id="30cc1-107"><dt>**ILS \_**</dt> <dt>0x00000000</dt> normale</span><span class="sxs-lookup"><span data-stu-id="30cc1-107"><dt>**ILS\_NORMAL**</dt> <dt>0x00000000</dt></span></span> </dl>       | <span data-ttu-id="30cc1-108">Lo stato dell'immagine non viene modificato.</span><span class="sxs-lookup"><span data-stu-id="30cc1-108">The image state is not modified.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                   |
| <span id="ILS_GLOW"></span><span id="ils_glow"></span><dl> <span data-ttu-id="30cc1-109"><dt>**ILS \_**</dt> <dt>0x00000001</dt> Glow</span><span class="sxs-lookup"><span data-stu-id="30cc1-109"><dt>**ILS\_GLOW**</dt> <dt>0x00000001</dt></span></span> </dl>             | <span data-ttu-id="30cc1-110">Non supportata.</span><span class="sxs-lookup"><span data-stu-id="30cc1-110">Not supported.</span></span> <br/>                                                                                                                                                                                                                                                                                                                                                                    |
| <span id="ILS_SHADOW"></span><span id="ils_shadow"></span><dl> <span data-ttu-id="30cc1-111"><dt>**ILS \_**</dt> <dt>0x00000002</dt> Shadow</span><span class="sxs-lookup"><span data-stu-id="30cc1-111"><dt>**ILS\_SHADOW**</dt> <dt>0x00000002</dt></span></span> </dl>       | <span data-ttu-id="30cc1-112">Non supportata.</span><span class="sxs-lookup"><span data-stu-id="30cc1-112">Not supported.</span></span> <br/>                                                                                                                                                                                                                                                                                                                                                                    |
| <span id="ILS_SATURATE"></span><span id="ils_saturate"></span><dl> <span data-ttu-id="30cc1-113"><dt>**ILS \_ SATURA**</dt> <dt>0x00000004</dt></span><span class="sxs-lookup"><span data-stu-id="30cc1-113"><dt>**ILS\_SATURATE**</dt> <dt>0x00000004</dt></span></span> </dl> | <span data-ttu-id="30cc1-114">Riduce la saturazione del colore dell'icona in scala di grigi.</span><span class="sxs-lookup"><span data-stu-id="30cc1-114">Reduces the color saturation of the icon to grayscale.</span></span> <span data-ttu-id="30cc1-115">Questa operazione influiscono solo sulle immagini 32bpp.</span><span class="sxs-lookup"><span data-stu-id="30cc1-115">This only affects 32bpp images.</span></span> <br/>                                                                                                                                                                                                                                                                                            |
| <span id="ILS_ALPHA"></span><span id="ils_alpha"></span><dl> <span data-ttu-id="30cc1-116"><dt>**ILS \_**</dt> <dt>0x00000008</dt> alfa</span><span class="sxs-lookup"><span data-stu-id="30cc1-116"><dt>**ILS\_ALPHA**</dt> <dt>0x00000008</dt></span></span> </dl>          | <span data-ttu-id="30cc1-117">Alfa fonde l'icona.</span><span class="sxs-lookup"><span data-stu-id="30cc1-117">Alpha blends the icon.</span></span> <span data-ttu-id="30cc1-118">La fusione alfa controlla il livello di trasparenza di un'icona, in base al valore del canale alfa.</span><span class="sxs-lookup"><span data-stu-id="30cc1-118">Alpha blending controls the transparency level of an icon, according to the value of its alpha channel.</span></span> <span data-ttu-id="30cc1-119">Il valore del canale alfa è indicato dal membro **frame** nel metodo [**IMAGELISTDRAWPARAMS**](/windows/win32/api/commctrl/ns-commctrl-imagelistdrawparams) .</span><span class="sxs-lookup"><span data-stu-id="30cc1-119">The value of the alpha channel is indicated by the **frame** member in the [**IMAGELISTDRAWPARAMS**](/windows/win32/api/commctrl/ns-commctrl-imagelistdrawparams) method.</span></span> <span data-ttu-id="30cc1-120">Il canale alfa può essere compreso tra 0 e 255, mentre 0 è completamente trasparente e 255 è completamente opaco.</span><span class="sxs-lookup"><span data-stu-id="30cc1-120">The alpha channel can be from 0 to 255, with 0 being completely transparent, and 255 being completely opaque.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="30cc1-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="30cc1-121">Requirements</span></span>



| <span data-ttu-id="30cc1-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="30cc1-122">Requirement</span></span> | <span data-ttu-id="30cc1-123">Valore</span><span class="sxs-lookup"><span data-stu-id="30cc1-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="30cc1-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="30cc1-124">Minimum supported client</span></span><br/> | <span data-ttu-id="30cc1-125">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="30cc1-125">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="30cc1-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="30cc1-126">Minimum supported server</span></span><br/> | <span data-ttu-id="30cc1-127">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="30cc1-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="30cc1-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="30cc1-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="30cc1-129"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="30cc1-129"><dt>Commctrl.h</dt></span></span> </dl> |



 


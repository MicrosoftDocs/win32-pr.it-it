---
title: Messaggio TB_CHANGEBITMAP (COMmctrl. h)
description: Modifica la bitmap per un pulsante in una barra degli strumenti.
ms.assetid: 112b6f4e-6034-4e13-8b2f-b8411a351fbd
keywords:
- Controlli di Windows Message TB_CHANGEBITMAP
topic_type:
- apiref
api_name:
- TB_CHANGEBITMAP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1367a2a1b4e35d6f52bf1e7a0be42f1e75daa7ac
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874682"
---
# <a name="tb_changebitmap-message"></a><span data-ttu-id="627b9-104">TB \_ CHANGEBITMAP messaggio</span><span class="sxs-lookup"><span data-stu-id="627b9-104">TB\_CHANGEBITMAP message</span></span>

<span data-ttu-id="627b9-105">Modifica la bitmap per un pulsante in una barra degli strumenti.</span><span class="sxs-lookup"><span data-stu-id="627b9-105">Changes the bitmap for a button in a toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="627b9-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="627b9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="627b9-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="627b9-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="627b9-108">Identificatore di comando del pulsante che deve ricevere una nuova bitmap.</span><span class="sxs-lookup"><span data-stu-id="627b9-108">Command identifier of the button that is to receive a new bitmap.</span></span>

</dd> <dt>

<span data-ttu-id="627b9-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="627b9-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="627b9-110">Indice in base zero di un'immagine nell'elenco di immagini della barra degli strumenti.</span><span class="sxs-lookup"><span data-stu-id="627b9-110">Zero-based index of an image in the toolbar's image list.</span></span> <span data-ttu-id="627b9-111">Il sistema Visualizza l'immagine specificata nel pulsante.</span><span class="sxs-lookup"><span data-stu-id="627b9-111">The system displays the specified image in the button.</span></span> <span data-ttu-id="627b9-112">Impostare questo parametro su I \_ IMAGECALLBACK e la barra degli strumenti invierà la notifica [**TBN \_ GETDISPINFO**](tbn-getdispinfo.md) per recuperare l'indice dell'immagine quando necessario.</span><span class="sxs-lookup"><span data-stu-id="627b9-112">Set this parameter to I\_IMAGECALLBACK, and the toolbar will send the [**TBN\_GETDISPINFO**](tbn-getdispinfo.md) notification to retrieve the image index when it is needed.</span></span>

<span data-ttu-id="627b9-113">[Versione 5,81](common-control-versions.md).</span><span class="sxs-lookup"><span data-stu-id="627b9-113">[Version 5.81](common-control-versions.md).</span></span> <span data-ttu-id="627b9-114">Impostare questo parametro su I \_ IMAGENONE per indicare che il pulsante non dispone di un'immagine.</span><span class="sxs-lookup"><span data-stu-id="627b9-114">Set this parameter to I\_IMAGENONE to indicate that the button does not have an image.</span></span> <span data-ttu-id="627b9-115">Il layout del pulsante non includerà alcuno spazio per una bitmap, ma solo per il testo.</span><span class="sxs-lookup"><span data-stu-id="627b9-115">The button layout will not include any space for a bitmap, only text.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="627b9-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="627b9-116">Return value</span></span>

<span data-ttu-id="627b9-117">Restituisce **true** se l'operazione ha esito positivo o **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="627b9-117">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="627b9-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="627b9-118">Requirements</span></span>



| <span data-ttu-id="627b9-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="627b9-119">Requirement</span></span> | <span data-ttu-id="627b9-120">Valore</span><span class="sxs-lookup"><span data-stu-id="627b9-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="627b9-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="627b9-121">Minimum supported client</span></span><br/> | <span data-ttu-id="627b9-122">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="627b9-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="627b9-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="627b9-123">Minimum supported server</span></span><br/> | <span data-ttu-id="627b9-124">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="627b9-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="627b9-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="627b9-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="627b9-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="627b9-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






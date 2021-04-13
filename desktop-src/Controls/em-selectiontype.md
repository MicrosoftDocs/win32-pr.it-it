---
title: Messaggio di EM_SELECTIONTYPE (RichEdit. h)
description: Determina il tipo di selezione per un controllo Rich Edit.
ms.assetid: a4200e32-1056-47bd-be47-5fabaf99c058
keywords:
- Controlli di Windows Message EM_SELECTIONTYPE
topic_type:
- apiref
api_name:
- EM_SELECTIONTYPE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0deb62ac3bf774c72bb076f6fce9aa8c77b423f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518682"
---
# <a name="em_selectiontype-message"></a><span data-ttu-id="57a61-104">\_Messaggio SELECTIONTYPE em</span><span class="sxs-lookup"><span data-stu-id="57a61-104">EM\_SELECTIONTYPE message</span></span>

<span data-ttu-id="57a61-105">Determina il tipo di selezione per un controllo Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="57a61-105">Determines the selection type for a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="57a61-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="57a61-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="57a61-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="57a61-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="57a61-108">Non utilizzato; deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="57a61-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="57a61-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="57a61-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="57a61-110">Non utilizzato; deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="57a61-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="57a61-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="57a61-111">Return value</span></span>

<span data-ttu-id="57a61-112">Se la selezione è vuota, il valore restituito è SEL \_ Empty.</span><span class="sxs-lookup"><span data-stu-id="57a61-112">If the selection is empty, the return value is SEL\_EMPTY.</span></span>

<span data-ttu-id="57a61-113">Se la selezione non è vuota, il valore restituito è un set di flag che contengono uno o più dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="57a61-113">If the selection is not empty, the return value is a set of flags containing one or more of the following values.</span></span>



| <span data-ttu-id="57a61-114">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="57a61-114">Return code</span></span>                                                                                     | <span data-ttu-id="57a61-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="57a61-115">Description</span></span>                                 |
|-------------------------------------------------------------------------------------------------|---------------------------------------------|
| <dl> <span data-ttu-id="57a61-116"><dt>**\_testo SEL**</dt></span><span class="sxs-lookup"><span data-stu-id="57a61-116"><dt>**SEL\_TEXT**</dt></span></span> </dl>        | <span data-ttu-id="57a61-117">Text.</span><span class="sxs-lookup"><span data-stu-id="57a61-117">Text.</span></span><br/>                            |
| <dl> <span data-ttu-id="57a61-118"><dt>**\_oggetto SEL**</dt></span><span class="sxs-lookup"><span data-stu-id="57a61-118"><dt>**SEL\_OBJECT**</dt></span></span> </dl>      | <span data-ttu-id="57a61-119">Almeno un oggetto COM.</span><span class="sxs-lookup"><span data-stu-id="57a61-119">At least one COM object.</span></span><br/>         |
| <dl> <span data-ttu-id="57a61-120"><dt>**SEL \_ MULTIchar**</dt></span><span class="sxs-lookup"><span data-stu-id="57a61-120"><dt>**SEL\_MULTICHAR**</dt></span></span> </dl>   | <span data-ttu-id="57a61-121">Più di un carattere di testo.</span><span class="sxs-lookup"><span data-stu-id="57a61-121">More than one character of text.</span></span><br/> |
| <dl> <span data-ttu-id="57a61-122"><dt>**SEL \_ MULTIoggetto**</dt></span><span class="sxs-lookup"><span data-stu-id="57a61-122"><dt>**SEL\_MULTIOBJECT**</dt></span></span> </dl> | <span data-ttu-id="57a61-123">Più di un oggetto COM.</span><span class="sxs-lookup"><span data-stu-id="57a61-123">More than one COM object.</span></span><br/>        |



 

## <a name="remarks"></a><span data-ttu-id="57a61-124">Commenti</span><span class="sxs-lookup"><span data-stu-id="57a61-124">Remarks</span></span>

<span data-ttu-id="57a61-125">Questo messaggio è utile durante l'elaborazione di [**\_ dimensioni WM**](/windows/desktop/winmsg/wm-size) per l'elemento padre di un controllo Rich Edit senza fondo.</span><span class="sxs-lookup"><span data-stu-id="57a61-125">This message is useful during [**WM\_SIZE**](/windows/desktop/winmsg/wm-size) processing for the parent of a bottomless rich edit control.</span></span>

## <a name="requirements"></a><span data-ttu-id="57a61-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="57a61-126">Requirements</span></span>



| <span data-ttu-id="57a61-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="57a61-127">Requirement</span></span> | <span data-ttu-id="57a61-128">Valore</span><span class="sxs-lookup"><span data-stu-id="57a61-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="57a61-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="57a61-129">Minimum supported client</span></span><br/> | <span data-ttu-id="57a61-130">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="57a61-130">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="57a61-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="57a61-131">Minimum supported server</span></span><br/> | <span data-ttu-id="57a61-132">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="57a61-132">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="57a61-133">Intestazione</span><span class="sxs-lookup"><span data-stu-id="57a61-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="57a61-134"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="57a61-134"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="57a61-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="57a61-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="57a61-136">**\_dimensioni WM**</span><span class="sxs-lookup"><span data-stu-id="57a61-136">**WM\_SIZE**</span></span>](/windows/desktop/winmsg/wm-size)
</dt> </dl>

 


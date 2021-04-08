---
title: Messaggio TB_MAPACCELERATOR (COMmctrl. h)
description: Determina l'ID del pulsante che corrisponde al carattere dell'acceleratore specificato.
ms.assetid: 724b593d-39af-4301-b721-0332844677b1
keywords:
- Controlli di Windows Message TB_MAPACCELERATOR
topic_type:
- apiref
api_name:
- TB_MAPACCELERATOR
- TB_MAPACCELERATORA
- TB_MAPACCELERATORW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 029584d9e1614a3a135da5ebd3f4f446795fd9ca
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742658"
---
# <a name="tb_mapaccelerator-message"></a><span data-ttu-id="e7b77-104">TB \_ MAPACCELERATOR messaggio</span><span class="sxs-lookup"><span data-stu-id="e7b77-104">TB\_MAPACCELERATOR message</span></span>

<span data-ttu-id="e7b77-105">Determina l'ID del pulsante che corrisponde al carattere dell'acceleratore specificato.</span><span class="sxs-lookup"><span data-stu-id="e7b77-105">Determines the ID of the button that corresponds to the specified accelerator character.</span></span>

## <a name="parameters"></a><span data-ttu-id="e7b77-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="e7b77-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e7b77-107">*wParam* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e7b77-107">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e7b77-108">Carattere del tasto di scelta rapida.</span><span class="sxs-lookup"><span data-stu-id="e7b77-108">The accelerator character.</span></span>

</dd> <dt>

<span data-ttu-id="e7b77-109">*lParam* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="e7b77-109">*lParam* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e7b77-110">Puntatore a un **uint**.</span><span class="sxs-lookup"><span data-stu-id="e7b77-110">Pointer to a **UINT**.</span></span> <span data-ttu-id="e7b77-111">In caso di esito positivo, il parametro conterrà l'ID del pulsante con *wParam* come carattere di accelerazione.</span><span class="sxs-lookup"><span data-stu-id="e7b77-111">On return, if successful, this parameter will hold the id of the button that has *wParam* as its accelerator character.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e7b77-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e7b77-112">Return value</span></span>

<span data-ttu-id="e7b77-113">Restituisce un valore diverso da zero se uno dei pulsanti presenta *wParam* come carattere dell'acceleratore oppure zero in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="e7b77-113">Returns a nonzero value if one of the buttons has *wParam* as its accelerator character, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="e7b77-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e7b77-114">Requirements</span></span>



| <span data-ttu-id="e7b77-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="e7b77-115">Requirement</span></span> | <span data-ttu-id="e7b77-116">Valore</span><span class="sxs-lookup"><span data-stu-id="e7b77-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e7b77-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e7b77-117">Minimum supported client</span></span><br/> | <span data-ttu-id="e7b77-118">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e7b77-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e7b77-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e7b77-119">Minimum supported server</span></span><br/> | <span data-ttu-id="e7b77-120">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="e7b77-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e7b77-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e7b77-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="e7b77-122"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="e7b77-122"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="e7b77-123">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="e7b77-123">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="e7b77-124">**TB \_ MAPACCELERATORW** (Unicode) e **TB \_ MAPACCELERATORA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="e7b77-124">**TB\_MAPACCELERATORW** (Unicode) and **TB\_MAPACCELERATORA** (ANSI)</span></span><br/>       |



 

 






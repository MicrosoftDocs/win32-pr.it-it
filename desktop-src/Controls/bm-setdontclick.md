---
title: Messaggio BM_SETDONTCLICK (winuser. h)
description: Imposta un flag su un pulsante di opzione che controlla la generazione di BN che hanno \_ fatto clic su messaggi quando il pulsante riceve lo stato attivo.
ms.assetid: 91d98bce-abea-4afc-a995-0f426ba7a518
keywords:
- Controlli di Windows Message BM_SETDONTCLICK
topic_type:
- apiref
api_name:
- BM_SETDONTCLICK
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c8596ec679ff07b87b3433d5b5a7805698f56f84
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301185"
---
# <a name="bm_setdontclick-message"></a><span data-ttu-id="21b97-104">\_Messaggio SETDONTCLICK BM</span><span class="sxs-lookup"><span data-stu-id="21b97-104">BM\_SETDONTCLICK message</span></span>

<span data-ttu-id="21b97-105">Imposta un flag su un pulsante di opzione che controlla la generazione di BN che hanno [ \_ fatto clic su](bn-clicked.md) messaggi quando il pulsante riceve lo stato attivo.</span><span class="sxs-lookup"><span data-stu-id="21b97-105">Sets a flag on a radio button that controls the generation of [BN\_CLICKED](bn-clicked.md) messages when the button receives focus.</span></span>

## <a name="parameters"></a><span data-ttu-id="21b97-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="21b97-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="21b97-107">*wParam* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="21b97-107">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="21b97-108">Valore **booleano** che specifica lo stato.</span><span class="sxs-lookup"><span data-stu-id="21b97-108">A **BOOL** that specifies the state.</span></span> <span data-ttu-id="21b97-109">**True** per impostare il flag, in caso contrario **false**.</span><span class="sxs-lookup"><span data-stu-id="21b97-109">**TRUE** to set the flag, otherwise **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="21b97-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="21b97-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="21b97-111">Non usato.</span><span class="sxs-lookup"><span data-stu-id="21b97-111">Not used.</span></span> <span data-ttu-id="21b97-112">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="21b97-112">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="21b97-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="21b97-113">Return value</span></span>

<span data-ttu-id="21b97-114">Nessun valore restituito.</span><span class="sxs-lookup"><span data-stu-id="21b97-114">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="21b97-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="21b97-115">Requirements</span></span>



| <span data-ttu-id="21b97-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="21b97-116">Requirement</span></span> | <span data-ttu-id="21b97-117">Valore</span><span class="sxs-lookup"><span data-stu-id="21b97-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="21b97-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="21b97-118">Minimum supported client</span></span><br/> | <span data-ttu-id="21b97-119">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="21b97-119">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="21b97-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="21b97-120">Minimum supported server</span></span><br/> | <span data-ttu-id="21b97-121">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="21b97-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="21b97-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="21b97-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="21b97-123"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="21b97-123"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



 

 






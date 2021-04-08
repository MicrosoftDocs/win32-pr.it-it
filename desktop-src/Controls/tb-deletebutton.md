---
title: Messaggio TB_DELETEBUTTON (COMmctrl. h)
description: Elimina un pulsante dalla barra degli strumenti.
ms.assetid: 6ba569f0-c400-4c0d-bc9f-3a82bcef0360
keywords:
- Controlli di Windows Message TB_DELETEBUTTON
topic_type:
- apiref
api_name:
- TB_DELETEBUTTON
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c1d9bbbca143351f70005990b5ac97fa4fa35cad
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103965003"
---
# <a name="tb_deletebutton-message"></a><span data-ttu-id="d9b3d-104">TB \_ DELETEBUTTON messaggio</span><span class="sxs-lookup"><span data-stu-id="d9b3d-104">TB\_DELETEBUTTON message</span></span>

<span data-ttu-id="d9b3d-105">Elimina un pulsante dalla barra degli strumenti.</span><span class="sxs-lookup"><span data-stu-id="d9b3d-105">Deletes a button from the toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="d9b3d-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="d9b3d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d9b3d-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d9b3d-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d9b3d-108">Indice in base zero del pulsante da eliminare.</span><span class="sxs-lookup"><span data-stu-id="d9b3d-108">Zero-based index of the button to delete.</span></span>

</dd> <dt>

<span data-ttu-id="d9b3d-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d9b3d-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="d9b3d-110">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="d9b3d-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d9b3d-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d9b3d-111">Return value</span></span>

<span data-ttu-id="d9b3d-112">Restituisce **true** se l'operazione ha esito positivo o **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="d9b3d-112">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="d9b3d-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d9b3d-113">Requirements</span></span>



| <span data-ttu-id="d9b3d-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="d9b3d-114">Requirement</span></span> | <span data-ttu-id="d9b3d-115">Valore</span><span class="sxs-lookup"><span data-stu-id="d9b3d-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d9b3d-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d9b3d-116">Minimum supported client</span></span><br/> | <span data-ttu-id="d9b3d-117">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d9b3d-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d9b3d-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d9b3d-118">Minimum supported server</span></span><br/> | <span data-ttu-id="d9b3d-119">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="d9b3d-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d9b3d-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d9b3d-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="d9b3d-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="d9b3d-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






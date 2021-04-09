---
title: Messaggio TB_GETITEMRECT (COMmctrl. h)
description: Recupera il rettangolo di delimitazione di un pulsante in una barra degli strumenti.
ms.assetid: 42c2c86e-0002-4029-be6a-fdfdf405b78c
keywords:
- Controlli di Windows Message TB_GETITEMRECT
topic_type:
- apiref
api_name:
- TB_GETITEMRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e71a4c6540a1a7ff918b97b3a331e692f6d44529
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874218"
---
# <a name="tb_getitemrect-message"></a><span data-ttu-id="b81e1-104">TB \_ GETITEMRECT messaggio</span><span class="sxs-lookup"><span data-stu-id="b81e1-104">TB\_GETITEMRECT message</span></span>

<span data-ttu-id="b81e1-105">Recupera il rettangolo di delimitazione di un pulsante in una barra degli strumenti.</span><span class="sxs-lookup"><span data-stu-id="b81e1-105">Retrieves the bounding rectangle of a button in a toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="b81e1-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="b81e1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b81e1-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b81e1-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b81e1-108">Indice in base zero del pulsante per il quale recuperare le informazioni.</span><span class="sxs-lookup"><span data-stu-id="b81e1-108">Zero-based index of the button for which to retrieve information.</span></span>

</dd> <dt>

<span data-ttu-id="b81e1-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b81e1-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b81e1-110">Puntatore a una struttura [**Rect**](/previous-versions//dd162897(v=vs.85)) che riceve le coordinate client del rettangolo di delimitazione.</span><span class="sxs-lookup"><span data-stu-id="b81e1-110">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that receives the client coordinates of the bounding rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b81e1-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b81e1-111">Return value</span></span>

<span data-ttu-id="b81e1-112">Restituisce **true** se l'operazione ha esito positivo o **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="b81e1-112">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="b81e1-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="b81e1-113">Remarks</span></span>

<span data-ttu-id="b81e1-114">Questo messaggio non recupera il rettangolo di delimitazione per i pulsanti il cui stato è impostato sul valore [**\_ nascosto TBSTATE**](toolbar-button-states.md) .</span><span class="sxs-lookup"><span data-stu-id="b81e1-114">This message does not retrieve the bounding rectangle for buttons whose state is set to the [**TBSTATE\_HIDDEN**](toolbar-button-states.md) value.</span></span>

## <a name="requirements"></a><span data-ttu-id="b81e1-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b81e1-115">Requirements</span></span>



| <span data-ttu-id="b81e1-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="b81e1-116">Requirement</span></span> | <span data-ttu-id="b81e1-117">Valore</span><span class="sxs-lookup"><span data-stu-id="b81e1-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b81e1-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b81e1-118">Minimum supported client</span></span><br/> | <span data-ttu-id="b81e1-119">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b81e1-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b81e1-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b81e1-120">Minimum supported server</span></span><br/> | <span data-ttu-id="b81e1-121">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="b81e1-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b81e1-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b81e1-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="b81e1-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="b81e1-123"><dt>Commctrl.h</dt></span></span> </dl> |



 


---
title: Messaggio PSM_SETNEXTTEXT (Prsht. h)
description: Imposta il testo del pulsante avanti in una procedura guidata. È possibile inviare questo messaggio in modo esplicito o utilizzando la \_ macro PropSheet SetNextText.
ms.assetid: 4608425e-1724-4d0b-b0f6-9fec147a85f6
keywords:
- Controlli di Windows Message PSM_SETNEXTTEXT
topic_type:
- apiref
api_name:
- PSM_SETNEXTTEXT
- PSM_SETNEXTTEXTW
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d781a8d76fca5c1e74bcda452b6ab7e03a32aacc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740095"
---
# <a name="psm_setnexttext-message"></a><span data-ttu-id="2cf2d-105">\_Messaggio SETNEXTTEXT di PSM</span><span class="sxs-lookup"><span data-stu-id="2cf2d-105">PSM\_SETNEXTTEXT message</span></span>

<span data-ttu-id="2cf2d-106">Imposta il testo del pulsante **Avanti** in una procedura guidata.</span><span class="sxs-lookup"><span data-stu-id="2cf2d-106">Sets the text of the **Next** button in a wizard.</span></span> <span data-ttu-id="2cf2d-107">È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**PropSheet \_ SetNextText**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setnexttext) .</span><span class="sxs-lookup"><span data-stu-id="2cf2d-107">You can send this message explicitly or by using the [**PropSheet\_SetNextText**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setnexttext) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="2cf2d-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="2cf2d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2cf2d-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2cf2d-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2cf2d-110">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="2cf2d-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="2cf2d-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2cf2d-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2cf2d-112">Puntatore a un buffer che contiene il testo.</span><span class="sxs-lookup"><span data-stu-id="2cf2d-112">Pointer to a buffer that contains the text.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2cf2d-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2cf2d-113">Return value</span></span>

<span data-ttu-id="2cf2d-114">Nessun valore restituito significativo.</span><span class="sxs-lookup"><span data-stu-id="2cf2d-114">No meaningful return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="2cf2d-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2cf2d-115">Requirements</span></span>



| <span data-ttu-id="2cf2d-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="2cf2d-116">Requirement</span></span> | <span data-ttu-id="2cf2d-117">Valore</span><span class="sxs-lookup"><span data-stu-id="2cf2d-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="2cf2d-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2cf2d-118">Minimum supported client</span></span><br/> | <span data-ttu-id="2cf2d-119">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="2cf2d-119">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="2cf2d-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2cf2d-120">Minimum supported server</span></span><br/> | <span data-ttu-id="2cf2d-121">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="2cf2d-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="2cf2d-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2cf2d-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="2cf2d-123"><dt>Prsht. h</dt></span><span class="sxs-lookup"><span data-stu-id="2cf2d-123"><dt>Prsht.h</dt></span></span> </dl> |
| <span data-ttu-id="2cf2d-124">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="2cf2d-124">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="2cf2d-125">**PSM \_ SETNEXTTEXTW** (Unicode)</span><span class="sxs-lookup"><span data-stu-id="2cf2d-125">**PSM\_SETNEXTTEXTW** (Unicode)</span></span><br/>                                         |



 

 






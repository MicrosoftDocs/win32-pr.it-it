---
title: Messaggio LVM_SETSELECTEDCOLUMN (COMmctrl. h)
description: Imposta l'indice della colonna selezionata.
ms.assetid: 11b0838e-24a7-4c1c-b67d-0912b5a6442a
keywords:
- Controlli di Windows Message LVM_SETSELECTEDCOLUMN
topic_type:
- apiref
api_name:
- LVM_SETSELECTEDCOLUMN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 827c41fabaea722bb2372c6bd3f7c3a54bee92f9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874714"
---
# <a name="lvm_setselectedcolumn-message"></a><span data-ttu-id="0f4aa-104">\_Messaggio SETSELECTEDCOLUMN LVM</span><span class="sxs-lookup"><span data-stu-id="0f4aa-104">LVM\_SETSELECTEDCOLUMN message</span></span>

<span data-ttu-id="0f4aa-105">Imposta l'indice della colonna selezionata.</span><span class="sxs-lookup"><span data-stu-id="0f4aa-105">Sets the index of the selected column.</span></span>

## <a name="parameters"></a><span data-ttu-id="0f4aa-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="0f4aa-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0f4aa-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0f4aa-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="0f4aa-108">Valore di tipo **int** che specifica l'indice di colonna.</span><span class="sxs-lookup"><span data-stu-id="0f4aa-108">Value of type **int** that specifies the column index.</span></span></dd> <dt>

<span data-ttu-id="0f4aa-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0f4aa-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="0f4aa-110">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="0f4aa-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0f4aa-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0f4aa-111">Return value</span></span>

<span data-ttu-id="0f4aa-112">Il valore restituito non viene utilizzato.</span><span class="sxs-lookup"><span data-stu-id="0f4aa-112">The return value is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="0f4aa-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="0f4aa-113">Remarks</span></span>

<span data-ttu-id="0f4aa-114">Gli indici di colonna vengono archiviati in una matrice **int** .</span><span class="sxs-lookup"><span data-stu-id="0f4aa-114">The column indices are stored in an **int** array.</span></span> <span data-ttu-id="0f4aa-115">Vedere il membro **puColumns** di [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema).</span><span class="sxs-lookup"><span data-stu-id="0f4aa-115">See the **puColumns** member of [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema).</span></span>

> [!Note]  
> <span data-ttu-id="0f4aa-116">Per utilizzare questo messaggio, è necessario fornire un manifesto che specifichi Comclt32.dll versione 6,0.</span><span class="sxs-lookup"><span data-stu-id="0f4aa-116">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="0f4aa-117">Per altre informazioni sui manifesti, vedere [Abilitazione degli stili di visualizzazione](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="0f4aa-117">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="0f4aa-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0f4aa-118">Requirements</span></span>



| <span data-ttu-id="0f4aa-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="0f4aa-119">Requirement</span></span> | <span data-ttu-id="0f4aa-120">Valore</span><span class="sxs-lookup"><span data-stu-id="0f4aa-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0f4aa-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0f4aa-121">Minimum supported client</span></span><br/> | <span data-ttu-id="0f4aa-122">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="0f4aa-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="0f4aa-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0f4aa-123">Minimum supported server</span></span><br/> | <span data-ttu-id="0f4aa-124">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="0f4aa-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="0f4aa-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0f4aa-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="0f4aa-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="0f4aa-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






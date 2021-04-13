---
title: Messaggio LVM_GETSELECTEDCOLUMN (COMmctrl. h)
description: Recupera un valore integer che specifica la colonna selezionata.
ms.assetid: 5aba5d96-50fd-439b-9782-fd5d8684b17f
keywords:
- Controlli di Windows Message LVM_GETSELECTEDCOLUMN
topic_type:
- apiref
api_name:
- LVM_GETSELECTEDCOLUMN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24ffae9a9c7812f025241f5b46f3b1ea61bb88bd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104341002"
---
# <a name="lvm_getselectedcolumn-message"></a><span data-ttu-id="d197a-104">\_Messaggio GETSELECTEDCOLUMN LVM</span><span class="sxs-lookup"><span data-stu-id="d197a-104">LVM\_GETSELECTEDCOLUMN message</span></span>

<span data-ttu-id="d197a-105">Recupera un valore integer che specifica la colonna selezionata.</span><span class="sxs-lookup"><span data-stu-id="d197a-105">Retrieves an integer that specifies the selected column.</span></span>

## <a name="parameters"></a><span data-ttu-id="d197a-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="d197a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d197a-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d197a-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="d197a-108">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="d197a-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="d197a-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d197a-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="d197a-110">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="d197a-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d197a-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d197a-111">Return value</span></span>

<span data-ttu-id="d197a-112">Restituisce un **uint** che specifica la colonna selezionata.</span><span class="sxs-lookup"><span data-stu-id="d197a-112">Returns an **UINT** that specifies the selected column.</span></span>

## <a name="remarks"></a><span data-ttu-id="d197a-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="d197a-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="d197a-114">Per utilizzare questo messaggio, è necessario fornire un manifesto che specifichi Comclt32.dll versione 6,0.</span><span class="sxs-lookup"><span data-stu-id="d197a-114">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="d197a-115">Per altre informazioni sui manifesti, vedere [Abilitazione degli stili di visualizzazione](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="d197a-115">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="d197a-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d197a-116">Requirements</span></span>



| <span data-ttu-id="d197a-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="d197a-117">Requirement</span></span> | <span data-ttu-id="d197a-118">Valore</span><span class="sxs-lookup"><span data-stu-id="d197a-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d197a-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d197a-119">Minimum supported client</span></span><br/> | <span data-ttu-id="d197a-120">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d197a-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d197a-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d197a-121">Minimum supported server</span></span><br/> | <span data-ttu-id="d197a-122">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="d197a-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d197a-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d197a-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="d197a-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="d197a-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






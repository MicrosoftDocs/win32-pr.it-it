---
title: Messaggio LVM_HASGROUP (COMmctrl. h)
description: Determina se il controllo di visualizzazione elenco dispone di un gruppo specificato.
ms.assetid: 0b8a9208-5221-4f66-8b26-7de55afe485f
keywords:
- Controlli di Windows Message LVM_HASGROUP
topic_type:
- apiref
api_name:
- LVM_HASGROUP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb05fed8466188aa0025d2128ce64ad7f1512c07
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478502"
---
# <a name="lvm_hasgroup-message"></a><span data-ttu-id="223b1-104">\_Messaggio HASGROUP LVM</span><span class="sxs-lookup"><span data-stu-id="223b1-104">LVM\_HASGROUP message</span></span>

<span data-ttu-id="223b1-105">Determina se il controllo di visualizzazione elenco dispone di un gruppo specificato.</span><span class="sxs-lookup"><span data-stu-id="223b1-105">Determines whether the list-view control has a specified group.</span></span>

## <a name="parameters"></a><span data-ttu-id="223b1-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="223b1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="223b1-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="223b1-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="223b1-108">ID del gruppo.</span><span class="sxs-lookup"><span data-stu-id="223b1-108">ID of the group.</span></span></dd> <dt>

<span data-ttu-id="223b1-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="223b1-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="223b1-110">Deve essere **null**.</span><span class="sxs-lookup"><span data-stu-id="223b1-110">Must be **NULL**.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="223b1-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="223b1-111">Return value</span></span>

<span data-ttu-id="223b1-112">Restituisce **true** se il controllo elenco-visualizzazione dispone del gruppo specificato o **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="223b1-112">Returns **TRUE** if the list-view control has the specified group, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="223b1-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="223b1-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="223b1-114">Per utilizzare questo messaggio, è necessario fornire un manifesto che specifichi Comclt32.dll versione 6,0.</span><span class="sxs-lookup"><span data-stu-id="223b1-114">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="223b1-115">Per altre informazioni sui manifesti, vedere [Abilitazione degli stili di visualizzazione](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="223b1-115">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="223b1-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="223b1-116">Requirements</span></span>



| <span data-ttu-id="223b1-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="223b1-117">Requirement</span></span> | <span data-ttu-id="223b1-118">Valore</span><span class="sxs-lookup"><span data-stu-id="223b1-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="223b1-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="223b1-119">Minimum supported client</span></span><br/> | <span data-ttu-id="223b1-120">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="223b1-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="223b1-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="223b1-121">Minimum supported server</span></span><br/> | <span data-ttu-id="223b1-122">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="223b1-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="223b1-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="223b1-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="223b1-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="223b1-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






---
title: Messaggio LVM_SORTGROUPS (COMmctrl. h)
description: Usa una funzione di confronto definita dall'applicazione per ordinare i gruppi in base all'ID all'interno di un controllo di visualizzazione elenco.
ms.assetid: 553e96d6-a982-4482-8fba-ef11a74fb82e
keywords:
- Controlli di Windows Message LVM_SORTGROUPS
topic_type:
- apiref
api_name:
- LVM_SORTGROUPS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2c70fd0f343c9efe0215c87f430e5ed1c89a3aed
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120958"
---
# <a name="lvm_sortgroups-message"></a><span data-ttu-id="ba0d8-104">\_Messaggio SORTGROUPS LVM</span><span class="sxs-lookup"><span data-stu-id="ba0d8-104">LVM\_SORTGROUPS message</span></span>

<span data-ttu-id="ba0d8-105">Usa una funzione di confronto definita dall'applicazione per ordinare i gruppi in base all'ID all'interno di un controllo di visualizzazione elenco.</span><span class="sxs-lookup"><span data-stu-id="ba0d8-105">Uses an application-defined comparison function to sort groups by ID within a list-view control.</span></span>

## <a name="parameters"></a><span data-ttu-id="ba0d8-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="ba0d8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ba0d8-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ba0d8-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="ba0d8-108">Puntatore a una funzione di confronto definita dall'applicazione, <a href="/windows/desktop/api/commctrl/nc-commctrl-pfnlvgroupcompare">LVGroupCompare</a>.</span><span class="sxs-lookup"><span data-stu-id="ba0d8-108">Pointer to an application-defined comparison function, <a href="/windows/desktop/api/commctrl/nc-commctrl-pfnlvgroupcompare">LVGroupCompare</a>.</span></span></dd> <dt>

<span data-ttu-id="ba0d8-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ba0d8-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="ba0d8-110">Puntatore void alle informazioni definite dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="ba0d8-110">Void pointer to the application-defined information.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ba0d8-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ba0d8-111">Return value</span></span>

<span data-ttu-id="ba0d8-112">Restituisce 1 se ha esito positivo oppure 0 in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="ba0d8-112">Returns 1 if successful, or 0 otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="ba0d8-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="ba0d8-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="ba0d8-114">Per utilizzare questo messaggio, è necessario fornire un manifesto che specifichi Comclt32.dll versione 6,0.</span><span class="sxs-lookup"><span data-stu-id="ba0d8-114">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="ba0d8-115">Per altre informazioni sui manifesti, vedere [Abilitazione degli stili di visualizzazione](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="ba0d8-115">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="ba0d8-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ba0d8-116">Requirements</span></span>



| <span data-ttu-id="ba0d8-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="ba0d8-117">Requirement</span></span> | <span data-ttu-id="ba0d8-118">Valore</span><span class="sxs-lookup"><span data-stu-id="ba0d8-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ba0d8-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ba0d8-119">Minimum supported client</span></span><br/> | <span data-ttu-id="ba0d8-120">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ba0d8-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ba0d8-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ba0d8-121">Minimum supported server</span></span><br/> | <span data-ttu-id="ba0d8-122">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="ba0d8-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ba0d8-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ba0d8-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="ba0d8-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="ba0d8-124"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ba0d8-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ba0d8-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ba0d8-126">**LVGroupCompare**</span><span class="sxs-lookup"><span data-stu-id="ba0d8-126">**LVGroupCompare**</span></span>](/windows/win32/api/commctrl/nc-commctrl-pfnlvgroupcompare)
</dt> </dl>


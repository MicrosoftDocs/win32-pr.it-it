---
title: Messaggio LVM_SETTILEINFO (COMmctrl. h)
description: Imposta le informazioni per un riquadro esistente di un controllo visualizzazione elenco.
ms.assetid: 345e8f16-9a6c-44e3-a262-d5d3be4d33ef
keywords:
- Controlli di Windows Message LVM_SETTILEINFO
topic_type:
- apiref
api_name:
- LVM_SETTILEINFO
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 489e163955b8f9cbf99ad25357b5be5a5d5981fd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119459"
---
# <a name="lvm_settileinfo-message"></a><span data-ttu-id="83780-104">\_Messaggio SETTILEINFO LVM</span><span class="sxs-lookup"><span data-stu-id="83780-104">LVM\_SETTILEINFO message</span></span>

<span data-ttu-id="83780-105">Imposta le informazioni per un riquadro esistente di un controllo visualizzazione elenco.</span><span class="sxs-lookup"><span data-stu-id="83780-105">Sets information for an existing tile of a list-view control.</span></span>

## <a name="parameters"></a><span data-ttu-id="83780-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="83780-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="83780-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="83780-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="83780-108">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="83780-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="83780-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="83780-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="83780-110">Puntatore a una struttura <a href="/windows/win32/api/commctrl/ns-commctrl-lvtileinfo">**LVTILEINFO**</a> che contiene le informazioni da impostare.</span><span class="sxs-lookup"><span data-stu-id="83780-110">Pointer to an <a href="/windows/win32/api/commctrl/ns-commctrl-lvtileinfo">**LVTILEINFO**</a> structure that contains the information to set.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="83780-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="83780-111">Return value</span></span>

<span data-ttu-id="83780-112">Restituisce **true** se l'operazione ha esito positivo o **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="83780-112">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="83780-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="83780-113">Remarks</span></span>

<span data-ttu-id="83780-114">**LVM \_ SETTILEINFO** non è supportato nello stile [**\_ OWNERDATA di LVS**](list-view-window-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="83780-114">**LVM\_SETTILEINFO** is not supported under the [**LVS\_OWNERDATA**](list-view-window-styles.md) style.</span></span>

> [!Note]  
> <span data-ttu-id="83780-115">Per utilizzare questo messaggio, è necessario fornire un manifesto che specifichi Comclt32.dll versione 6,0.</span><span class="sxs-lookup"><span data-stu-id="83780-115">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="83780-116">Per altre informazioni sui manifesti, vedere [Abilitazione degli stili di visualizzazione](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="83780-116">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="83780-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="83780-117">Requirements</span></span>



| <span data-ttu-id="83780-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="83780-118">Requirement</span></span> | <span data-ttu-id="83780-119">Valore</span><span class="sxs-lookup"><span data-stu-id="83780-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="83780-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="83780-120">Minimum supported client</span></span><br/> | <span data-ttu-id="83780-121">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="83780-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="83780-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="83780-122">Minimum supported server</span></span><br/> | <span data-ttu-id="83780-123">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="83780-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="83780-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="83780-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="83780-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="83780-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






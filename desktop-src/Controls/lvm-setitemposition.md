---
title: Messaggio LVM_SETITEMPOSITION (COMmctrl. h)
description: Sposta un elemento in una posizione specificata in un controllo visualizzazione elenco (deve essere in una visualizzazione icona o piccola). È possibile inviare questo messaggio in modo esplicito o usando la \_ macro SetItemPosition di ListView.
ms.assetid: dfb35af4-e6c3-40fc-9d7c-cf0d68a3ea01
keywords:
- Controlli di Windows Message LVM_SETITEMPOSITION
topic_type:
- apiref
api_name:
- LVM_SETITEMPOSITION
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b95fcf2949f1e19677bd445c0f6c5f762db078d1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873894"
---
# <a name="lvm_setitemposition-message"></a><span data-ttu-id="1b06e-105">\_Messaggio SETITEMPOSITION LVM</span><span class="sxs-lookup"><span data-stu-id="1b06e-105">LVM\_SETITEMPOSITION message</span></span>

<span data-ttu-id="1b06e-106">Sposta un elemento in una posizione specificata in un controllo visualizzazione elenco (deve essere in una visualizzazione icona o piccola).</span><span class="sxs-lookup"><span data-stu-id="1b06e-106">Moves an item to a specified position in a list-view control (must be in icon or small icon view).</span></span> <span data-ttu-id="1b06e-107">È possibile inviare questo messaggio in modo esplicito o usando la macro [**\_ SetItemPosition di ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitemposition) .</span><span class="sxs-lookup"><span data-stu-id="1b06e-107">You can send this message explicitly or by using the [**ListView\_SetItemPosition**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitemposition) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="1b06e-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="1b06e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1b06e-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1b06e-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1b06e-110">Indice dell'elemento della visualizzazione elenco.</span><span class="sxs-lookup"><span data-stu-id="1b06e-110">Index of the list-view item.</span></span>

</dd> <dt>

<span data-ttu-id="1b06e-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1b06e-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1b06e-112">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) specifica la nuova posizione x dell'angolo superiore sinistro dell'elemento, in coordinate della visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="1b06e-112">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) specifies the new x-position of the item's upper-left corner, in view coordinates.</span></span> <span data-ttu-id="1b06e-113">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifica la nuova posizione y dell'angolo superiore sinistro dell'elemento, in coordinate della visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="1b06e-113">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the new y-position of the item's upper-left corner, in view coordinates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1b06e-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1b06e-114">Return value</span></span>

<span data-ttu-id="1b06e-115">Restituisce **true** se l'operazione ha esito positivo o **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="1b06e-115">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="1b06e-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="1b06e-116">Remarks</span></span>

<span data-ttu-id="1b06e-117">Se il controllo elenco-visualizzazione dispone dello stile [**LVS \_ AutoArrange**](list-view-window-styles.md) , gli elementi nel controllo elenco-visualizzazione vengono disposti dopo l'impostazione della posizione dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="1b06e-117">If the list-view control has the [**LVS\_AUTOARRANGE**](list-view-window-styles.md) style, the items in the list-view control are arranged after the position of the item is set.</span></span>

<span data-ttu-id="1b06e-118">In Windows Vista, l'invio di questo messaggio a un controllo di visualizzazione elenco con lo stile [**LVS \_ AutoArrange**](list-view-window-styles.md) non esegue alcuna operazione e il valore restituito è **false**.</span><span class="sxs-lookup"><span data-stu-id="1b06e-118">On Windows Vista, sending this message to a list-view control with the [**LVS\_AUTOARRANGE**](list-view-window-styles.md) style does nothing, and the return value is **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="1b06e-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1b06e-119">Requirements</span></span>



| <span data-ttu-id="1b06e-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="1b06e-120">Requirement</span></span> | <span data-ttu-id="1b06e-121">Valore</span><span class="sxs-lookup"><span data-stu-id="1b06e-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1b06e-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1b06e-122">Minimum supported client</span></span><br/> | <span data-ttu-id="1b06e-123">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="1b06e-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="1b06e-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1b06e-124">Minimum supported server</span></span><br/> | <span data-ttu-id="1b06e-125">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="1b06e-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="1b06e-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1b06e-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="1b06e-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="1b06e-127"><dt>Commctrl.h</dt></span></span> </dl> |



 


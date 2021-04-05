---
title: Messaggio LVM_SETITEMPOSITION32 (COMmctrl. h)
description: Sposta un elemento in una posizione specificata in un controllo visualizzazione elenco (deve essere in una visualizzazione icona o piccola).
ms.assetid: 77db5fd0-bbc3-47ad-95ef-61ef4ac022bc
keywords:
- Controlli di Windows Message LVM_SETITEMPOSITION32
topic_type:
- apiref
api_name:
- LVM_SETITEMPOSITION32
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 450963e4adf5ea2b0644f8d155145ba577efab83
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048422"
---
# <a name="lvm_setitemposition32-message"></a><span data-ttu-id="bf359-104">\_Messaggio SETITEMPOSITION32 LVM</span><span class="sxs-lookup"><span data-stu-id="bf359-104">LVM\_SETITEMPOSITION32 message</span></span>

<span data-ttu-id="bf359-105">Sposta un elemento in una posizione specificata in un controllo visualizzazione elenco (deve essere in una visualizzazione icona o piccola).</span><span class="sxs-lookup"><span data-stu-id="bf359-105">Moves an item to a specified position in a list-view control (must be in icon or small icon view).</span></span> <span data-ttu-id="bf359-106">Questo messaggio è diverso dal messaggio [**LVM \_ SETITEMPOSITION**](lvm-setitemposition.md) in quanto usa coordinate a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="bf359-106">This message differs from the [**LVM\_SETITEMPOSITION**](lvm-setitemposition.md) message in that it uses 32-bit coordinates.</span></span> <span data-ttu-id="bf359-107">È possibile inviare questo messaggio in modo esplicito o usando la macro [**\_ SetItemPosition32 di ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitemposition32) .</span><span class="sxs-lookup"><span data-stu-id="bf359-107">You can send this message explicitly or by using the [**ListView\_SetItemPosition32**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitemposition32) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="bf359-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="bf359-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bf359-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="bf359-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bf359-110">Indice dell'elemento della visualizzazione elenco per il quale impostare la posizione.</span><span class="sxs-lookup"><span data-stu-id="bf359-110">Index of the list-view item for which to set the position.</span></span>

</dd> <dt>

<span data-ttu-id="bf359-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="bf359-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bf359-112">Puntatore a una struttura di [**punti**](/previous-versions//dd162805(v=vs.85)) che contiene la nuova posizione dell'elemento, in coordinate di visualizzazione elenco.</span><span class="sxs-lookup"><span data-stu-id="bf359-112">Pointer to a [**POINT**](/previous-versions//dd162805(v=vs.85)) structure that contains the new position of the item, in list-view coordinates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bf359-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="bf359-113">Return value</span></span>

<span data-ttu-id="bf359-114">Nessun valore restituito.</span><span class="sxs-lookup"><span data-stu-id="bf359-114">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="bf359-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bf359-115">Requirements</span></span>



| <span data-ttu-id="bf359-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="bf359-116">Requirement</span></span> | <span data-ttu-id="bf359-117">Valore</span><span class="sxs-lookup"><span data-stu-id="bf359-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="bf359-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bf359-118">Minimum supported client</span></span><br/> | <span data-ttu-id="bf359-119">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="bf359-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="bf359-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bf359-120">Minimum supported server</span></span><br/> | <span data-ttu-id="bf359-121">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="bf359-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="bf359-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="bf359-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="bf359-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="bf359-123"><dt>Commctrl.h</dt></span></span> </dl> |



 


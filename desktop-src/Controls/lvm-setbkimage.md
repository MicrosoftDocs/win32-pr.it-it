---
title: Messaggio LVM_SETBKIMAGE (COMmctrl. h)
description: Imposta l'immagine di sfondo in un controllo visualizzazione elenco. È possibile inviare questo messaggio in modo esplicito o usando la \_ macro SetBkImage di ListView.
ms.assetid: 8fdd363c-ac12-498b-80b7-aaa5741cfd76
keywords:
- Controlli di Windows Message LVM_SETBKIMAGE
topic_type:
- apiref
api_name:
- LVM_SETBKIMAGE
- LVM_SETBKIMAGEA
- LVM_SETBKIMAGEW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e22bebdcb36faff56dfabab721731acb55fdec14
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477566"
---
# <a name="lvm_setbkimage-message"></a><span data-ttu-id="6cae9-105">\_Messaggio SETBKIMAGE LVM</span><span class="sxs-lookup"><span data-stu-id="6cae9-105">LVM\_SETBKIMAGE message</span></span>

<span data-ttu-id="6cae9-106">Imposta l'immagine di sfondo in un controllo visualizzazione elenco.</span><span class="sxs-lookup"><span data-stu-id="6cae9-106">Sets the background image in a list-view control.</span></span> <span data-ttu-id="6cae9-107">È possibile inviare questo messaggio in modo esplicito o usando la macro [**\_ SetBkImage di ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setbkimage) .</span><span class="sxs-lookup"><span data-stu-id="6cae9-107">You can send this message explicitly or by using the [**ListView\_SetBkImage**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setbkimage) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="6cae9-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="6cae9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6cae9-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6cae9-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6cae9-110">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="6cae9-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="6cae9-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6cae9-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6cae9-112">Puntatore a una struttura [**LVBKIMAGE**](/windows/win32/api/commctrl/ns-commctrl-lvbkimagea) che contiene le nuove informazioni sull'immagine di sfondo.</span><span class="sxs-lookup"><span data-stu-id="6cae9-112">Pointer to a [**LVBKIMAGE**](/windows/win32/api/commctrl/ns-commctrl-lvbkimagea) structure that contains the new background image information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6cae9-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6cae9-113">Return value</span></span>

<span data-ttu-id="6cae9-114">Restituisce un valore diverso da zero se ha esito positivo oppure zero in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="6cae9-114">Returns nonzero if successful, or zero otherwise.</span></span> <span data-ttu-id="6cae9-115">Restituisce zero se il membro **ulFlags** della struttura [**LVBKIMAGE**](/windows/win32/api/commctrl/ns-commctrl-lvbkimagea) è **LVBKIF \_ source \_ None**.</span><span class="sxs-lookup"><span data-stu-id="6cae9-115">Returns zero if the **ulFlags** member of the [**LVBKIMAGE**](/windows/win32/api/commctrl/ns-commctrl-lvbkimagea) structure is **LVBKIF\_SOURCE\_NONE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="6cae9-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="6cae9-116">Remarks</span></span>

<span data-ttu-id="6cae9-117">Poiché il controllo elenco-visualizzazione USA OLE COM per manipolare le immagini di sfondo, l'applicazione chiamante deve chiamare [**CoInitialize**](/windows/desktop/api/objbase/nf-objbase-coinitialize) o [**OleInitialize**](/windows/desktop/api/ole2/nf-ole2-oleinitialize) prima di inviare questo messaggio.</span><span class="sxs-lookup"><span data-stu-id="6cae9-117">Because the list-view control uses OLE COM to manipulate the background images, the calling application must call [**CoInitialize**](/windows/desktop/api/objbase/nf-objbase-coinitialize) or [**OleInitialize**](/windows/desktop/api/ole2/nf-ole2-oleinitialize) before sending this message.</span></span> <span data-ttu-id="6cae9-118">È consigliabile chiamare una di queste funzioni quando l'applicazione viene inizializzata e chiamare [**CoUninitialize**](/windows/desktop/api/combaseapi/nf-combaseapi-couninitialize) o [**OleUninitialize**](/windows/desktop/api/ole2/nf-ole2-oleuninitialize) quando l'applicazione viene terminata.</span><span class="sxs-lookup"><span data-stu-id="6cae9-118">It is best to call one of these functions when the application is initialized and call either [**CoUninitialize**](/windows/desktop/api/combaseapi/nf-combaseapi-couninitialize) or [**OleUninitialize**](/windows/desktop/api/ole2/nf-ole2-oleuninitialize) when the application is terminating.</span></span>

## <a name="requirements"></a><span data-ttu-id="6cae9-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6cae9-119">Requirements</span></span>



| <span data-ttu-id="6cae9-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="6cae9-120">Requirement</span></span> | <span data-ttu-id="6cae9-121">Valore</span><span class="sxs-lookup"><span data-stu-id="6cae9-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6cae9-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6cae9-122">Minimum supported client</span></span><br/> | <span data-ttu-id="6cae9-123">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="6cae9-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="6cae9-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6cae9-124">Minimum supported server</span></span><br/> | <span data-ttu-id="6cae9-125">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="6cae9-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6cae9-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6cae9-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="6cae9-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="6cae9-127"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="6cae9-128">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="6cae9-128">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="6cae9-129">**LVM \_ SETBKIMAGEW** (Unicode) e **LVM \_ SETBKIMAGEA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="6cae9-129">**LVM\_SETBKIMAGEW** (Unicode) and **LVM\_SETBKIMAGEA** (ANSI)</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="6cae9-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6cae9-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6cae9-131">**\_GETBKIMAGE LVM**</span><span class="sxs-lookup"><span data-stu-id="6cae9-131">**LVM\_GETBKIMAGE**</span></span>](lvm-getbkimage.md)
</dt> </dl>

 


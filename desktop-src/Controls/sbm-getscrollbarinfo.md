---
title: Messaggio SBM_GETSCROLLBARINFO (winuser. h)
description: Inviato da un'applicazione per recuperare informazioni sulla barra di scorrimento specificata.
ms.assetid: db6f704f-99ee-448c-ae7a-dd5a23399fb6
keywords:
- Controlli di Windows Message SBM_GETSCROLLBARINFO
topic_type:
- apiref
api_name:
- SBM_GETSCROLLBARINFO
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8bdd78eb665bd069d854538bb2bdfae1a946765
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741375"
---
# <a name="sbm_getscrollbarinfo-message"></a><span data-ttu-id="cd57a-104">\_Messaggio GETSCROLLBARINFO SBM</span><span class="sxs-lookup"><span data-stu-id="cd57a-104">SBM\_GETSCROLLBARINFO message</span></span>

<span data-ttu-id="cd57a-105">Inviato da un'applicazione per recuperare informazioni sulla barra di scorrimento specificata.</span><span class="sxs-lookup"><span data-stu-id="cd57a-105">Sent by an application to retrieve information about the specified scroll bar.</span></span>

## <a name="parameters"></a><span data-ttu-id="cd57a-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="cd57a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cd57a-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="cd57a-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cd57a-108">Non utilizzato; deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="cd57a-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="cd57a-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="cd57a-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cd57a-110">Puntatore a una struttura [**SCROLLBARINFO**](/windows/win32/api/winuser/ns-winuser-scrollbarinfo) che riceve le informazioni.</span><span class="sxs-lookup"><span data-stu-id="cd57a-110">Pointer to a [**SCROLLBARINFO**](/windows/win32/api/winuser/ns-winuser-scrollbarinfo) structure that receives the information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cd57a-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="cd57a-111">Return value</span></span>

<span data-ttu-id="cd57a-112">Restituisce un valore diverso da zero in caso di esito positivo o zero.</span><span class="sxs-lookup"><span data-stu-id="cd57a-112">Returns nonzero if successful or zero otherwise.</span></span>

<span data-ttu-id="cd57a-113">Per informazioni dettagliate sull'errore, chiamare [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="cd57a-113">To get extended error information, call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="requirements"></a><span data-ttu-id="cd57a-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cd57a-114">Requirements</span></span>



| <span data-ttu-id="cd57a-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="cd57a-115">Requirement</span></span> | <span data-ttu-id="cd57a-116">Valore</span><span class="sxs-lookup"><span data-stu-id="cd57a-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cd57a-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cd57a-117">Minimum supported client</span></span><br/> | <span data-ttu-id="cd57a-118">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="cd57a-118">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="cd57a-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cd57a-119">Minimum supported server</span></span><br/> | <span data-ttu-id="cd57a-120">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="cd57a-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="cd57a-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="cd57a-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="cd57a-122"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="cd57a-122"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cd57a-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cd57a-123">See also</span></span>

<dl> <dt>

<span data-ttu-id="cd57a-124">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="cd57a-124">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="cd57a-125">**GetScrollBarInfo**</span><span class="sxs-lookup"><span data-stu-id="cd57a-125">**GetScrollBarInfo**</span></span>](/windows/desktop/api/Winuser/nf-winuser-getscrollbarinfo)
</dt> <dt>

[<span data-ttu-id="cd57a-126">**SCROLLBARINFO**</span><span class="sxs-lookup"><span data-stu-id="cd57a-126">**SCROLLBARINFO**</span></span>](/windows/win32/api/winuser/ns-winuser-scrollbarinfo)
</dt> </dl>

 


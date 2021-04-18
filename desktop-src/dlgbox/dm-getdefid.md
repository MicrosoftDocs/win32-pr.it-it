---
title: Messaggio DM_GETDEFID (winuser. h)
description: Recupera l'identificatore del controllo pulsante di comando predefinito per una finestra di dialogo.
ms.assetid: 9f00a494-f5a2-4c4e-a9fc-2220d9326eb9
keywords:
- Finestre di dialogo DM_GETDEFID messaggio
topic_type:
- apiref
api_name:
- DM_GETDEFID
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7fdcdfc2cd278ab452d48ecb1c254bdb00ffbb7c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518880"
---
# <a name="dm_getdefid-message"></a><span data-ttu-id="c79b5-104">\_Messaggio DM GETDEFID</span><span class="sxs-lookup"><span data-stu-id="c79b5-104">DM\_GETDEFID message</span></span>

<span data-ttu-id="c79b5-105">Recupera l'identificatore del controllo pulsante di comando predefinito per una finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="c79b5-105">Retrieves the identifier of the default push button control for a dialog box.</span></span>


```C++
#define WM_USER              0x0400
#define DM_GETDEFID         (WM_USER+0)
```



## <a name="parameters"></a><span data-ttu-id="c79b5-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="c79b5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c79b5-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c79b5-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c79b5-108">Questo parametro non viene utilizzato e deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="c79b5-108">This parameter is not used and must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="c79b5-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c79b5-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c79b5-110">Questo parametro non viene utilizzato e deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="c79b5-110">This parameter is not used and must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c79b5-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c79b5-111">Return value</span></span>

<span data-ttu-id="c79b5-112">Se esiste un pulsante di push predefinito, la parola più significativa del valore restituito contiene il valore **DC \_ HASDEFID** e la parola di basso livello contiene l'identificatore del controllo.</span><span class="sxs-lookup"><span data-stu-id="c79b5-112">If a default push button exists, the high-order word of the return value contains the value **DC\_HASDEFID** and the low-order word contains the control identifier.</span></span> <span data-ttu-id="c79b5-113">In caso contrario, il valore restituito è zero.</span><span class="sxs-lookup"><span data-stu-id="c79b5-113">Otherwise, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="c79b5-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="c79b5-114">Remarks</span></span>

<span data-ttu-id="c79b5-115">La funzione [**DefDlgProc**](/windows/desktop/api/Winuser/nf-winuser-defdlgprocw) elabora questo messaggio.</span><span class="sxs-lookup"><span data-stu-id="c79b5-115">The [**DefDlgProc**](/windows/desktop/api/Winuser/nf-winuser-defdlgprocw) function processes this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="c79b5-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c79b5-116">Requirements</span></span>



| <span data-ttu-id="c79b5-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="c79b5-117">Requirement</span></span> | <span data-ttu-id="c79b5-118">Valore</span><span class="sxs-lookup"><span data-stu-id="c79b5-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c79b5-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c79b5-119">Minimum supported client</span></span><br/> | <span data-ttu-id="c79b5-120">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="c79b5-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="c79b5-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c79b5-121">Minimum supported server</span></span><br/> | <span data-ttu-id="c79b5-122">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="c79b5-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="c79b5-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c79b5-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="c79b5-124"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c79b5-124"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c79b5-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c79b5-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="c79b5-126">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="c79b5-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="c79b5-127">**DefDlgProc**</span><span class="sxs-lookup"><span data-stu-id="c79b5-127">**DefDlgProc**</span></span>](/windows/desktop/api/Winuser/nf-winuser-defdlgprocw)
</dt> <dt>

[<span data-ttu-id="c79b5-128">**\_SETDEFID DM**</span><span class="sxs-lookup"><span data-stu-id="c79b5-128">**DM\_SETDEFID**</span></span>](dm-setdefid.md)
</dt> <dt>

<span data-ttu-id="c79b5-129">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="c79b5-129">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="c79b5-130">Finestre di dialogo</span><span class="sxs-lookup"><span data-stu-id="c79b5-130">Dialog Boxes</span></span>](dialog-boxes.md)
</dt> </dl>

 

 






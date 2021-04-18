---
description: Un'applicazione invia il \_ messaggio WM MDIRESTORE a una finestra del client di interfaccia a documenti multipli (MDI) per ripristinare una finestra figlio MDI dalla dimensione ingrandita o ridotta a icona.
ms.assetid: bb99fda1-9eb5-4307-9326-9a417a046c22
title: Messaggio WM_MDIRESTORE (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cc2cf36a0b428e1e9003682a5e766f613fd7ba81
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306659"
---
# <a name="wm_mdirestore-message"></a><span data-ttu-id="a21c6-103">\_Messaggio MDIRESTORE WM</span><span class="sxs-lookup"><span data-stu-id="a21c6-103">WM\_MDIRESTORE message</span></span>

<span data-ttu-id="a21c6-104">Un'applicazione invia il messaggio **WM \_ MDIRESTORE** a una finestra del client di interfaccia a documenti multipli (MDI) per ripristinare una finestra figlio MDI dalla dimensione ingrandita o ridotta a icona.</span><span class="sxs-lookup"><span data-stu-id="a21c6-104">An application sends the **WM\_MDIRESTORE** message to a multiple-document interface (MDI) client window to restore an MDI child window from maximized or minimized size.</span></span>


```C++
#define WM_MDIRESTORE                   0x0223
```



## <a name="parameters"></a><span data-ttu-id="a21c6-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="a21c6-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a21c6-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a21c6-106">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a21c6-107">Handle per la finestra figlio MDI da ripristinare.</span><span class="sxs-lookup"><span data-stu-id="a21c6-107">A handle to the MDI child window to be restored.</span></span>

</dd> <dt>

<span data-ttu-id="a21c6-108">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a21c6-108">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a21c6-109">Questo parametro non viene usato.</span><span class="sxs-lookup"><span data-stu-id="a21c6-109">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a21c6-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a21c6-110">Return value</span></span>

<span data-ttu-id="a21c6-111">Tipo: **zero**</span><span class="sxs-lookup"><span data-stu-id="a21c6-111">Type: **zero**</span></span>

<span data-ttu-id="a21c6-112">Il valore restituito è sempre zero.</span><span class="sxs-lookup"><span data-stu-id="a21c6-112">The return value is always zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="a21c6-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a21c6-113">Requirements</span></span>



| <span data-ttu-id="a21c6-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="a21c6-114">Requirement</span></span> | <span data-ttu-id="a21c6-115">Valore</span><span class="sxs-lookup"><span data-stu-id="a21c6-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a21c6-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a21c6-116">Minimum supported client</span></span><br/> | <span data-ttu-id="a21c6-117">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="a21c6-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="a21c6-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a21c6-118">Minimum supported server</span></span><br/> | <span data-ttu-id="a21c6-119">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="a21c6-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="a21c6-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a21c6-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="a21c6-121"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a21c6-121"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a21c6-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a21c6-122">See also</span></span>

<dl> <dt>

<span data-ttu-id="a21c6-123">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="a21c6-123">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="a21c6-124">**\_MDIMAXIMIZE WM**</span><span class="sxs-lookup"><span data-stu-id="a21c6-124">**WM\_MDIMAXIMIZE**</span></span>](wm-mdimaximize.md)
</dt> <dt>

<span data-ttu-id="a21c6-125">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="a21c6-125">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="a21c6-126">Interfaccia a documenti multipli</span><span class="sxs-lookup"><span data-stu-id="a21c6-126">Multiple Document Interface</span></span>](multiple-document-interface.md)
</dt> </dl>

 

 





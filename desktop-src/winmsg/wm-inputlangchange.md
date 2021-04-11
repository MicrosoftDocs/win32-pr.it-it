---
description: Inviato alla finestra in primo piano interessata dopo la modifica della lingua di input di un'applicazione. È necessario apportare le impostazioni specifiche dell'applicazione e passare il messaggio alla funzione DefWindowProc, che passa il messaggio a tutte le finestre figlio di primo livello.
ms.assetid: 4d403b1d-f6f7-40d5-9bf5-6a9c4da0803c
title: Messaggio WM_INPUTLANGCHANGE (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0cdf04a775873e4cefe2c79269c14bd3d4da8d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128962"
---
# <a name="wm_inputlangchange-message"></a><span data-ttu-id="41e7e-104">\_Messaggio INPUTLANGCHANGE WM</span><span class="sxs-lookup"><span data-stu-id="41e7e-104">WM\_INPUTLANGCHANGE message</span></span>

<span data-ttu-id="41e7e-105">Inviato alla finestra in primo piano interessata dopo la modifica della lingua di input di un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="41e7e-105">Sent to the topmost affected window after an application's input language has been changed.</span></span> <span data-ttu-id="41e7e-106">È necessario apportare le impostazioni specifiche dell'applicazione e passare il messaggio alla funzione [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) , che passa il messaggio a tutte le finestre figlio di primo livello.</span><span class="sxs-lookup"><span data-stu-id="41e7e-106">You should make any application-specific settings and pass the message to the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function, which passes the message to all first-level child windows.</span></span> <span data-ttu-id="41e7e-107">Queste finestre figlio possono passare il messaggio a [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) per passare il messaggio alle finestre figlio e così via.</span><span class="sxs-lookup"><span data-stu-id="41e7e-107">These child windows can pass the message to [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) to have it pass the message to their child windows, and so on.</span></span>

<span data-ttu-id="41e7e-108">Una finestra riceve questo messaggio tramite la funzione [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="41e7e-108">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_INPUTLANGCHANGE              0x0051
```



## <a name="parameters"></a><span data-ttu-id="41e7e-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="41e7e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="41e7e-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="41e7e-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="41e7e-111">Set di caratteri delle nuove impostazioni locali.</span><span class="sxs-lookup"><span data-stu-id="41e7e-111">The character set of the new locale.</span></span>

</dd> <dt>

<span data-ttu-id="41e7e-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="41e7e-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="41e7e-113">Identificatore delle impostazioni locali di input.</span><span class="sxs-lookup"><span data-stu-id="41e7e-113">The input locale identifier.</span></span> <span data-ttu-id="41e7e-114">Per altre informazioni, vedere [lingue, impostazioni locali e layout di tastiera](../inputdev/about-keyboard-input.md).</span><span class="sxs-lookup"><span data-stu-id="41e7e-114">For more information, see [Languages, Locales, and Keyboard Layouts](../inputdev/about-keyboard-input.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="41e7e-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="41e7e-115">Return value</span></span>

<span data-ttu-id="41e7e-116">Tipo: **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="41e7e-116">Type: **LRESULT**</span></span>

<span data-ttu-id="41e7e-117">Un'applicazione deve restituire un valore diverso da zero se elabora questo messaggio.</span><span class="sxs-lookup"><span data-stu-id="41e7e-117">An application should return nonzero if it processes this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="41e7e-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="41e7e-118">Requirements</span></span>



| <span data-ttu-id="41e7e-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="41e7e-119">Requirement</span></span> | <span data-ttu-id="41e7e-120">Valore</span><span class="sxs-lookup"><span data-stu-id="41e7e-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="41e7e-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="41e7e-121">Minimum supported client</span></span><br/> | <span data-ttu-id="41e7e-122">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="41e7e-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="41e7e-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="41e7e-123">Minimum supported server</span></span><br/> | <span data-ttu-id="41e7e-124">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="41e7e-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="41e7e-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="41e7e-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="41e7e-126"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="41e7e-126"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="41e7e-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="41e7e-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="41e7e-128">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="41e7e-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="41e7e-129">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="41e7e-129">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="41e7e-130">**\_INPUTLANGCHANGEREQUEST WM**</span><span class="sxs-lookup"><span data-stu-id="41e7e-130">**WM\_INPUTLANGCHANGEREQUEST**</span></span>](wm-inputlangchangerequest.md)
</dt> <dt>

<span data-ttu-id="41e7e-131">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="41e7e-131">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="41e7e-132">Windows</span><span class="sxs-lookup"><span data-stu-id="41e7e-132">Windows</span></span>](windows.md)
</dt> </dl>

 

 

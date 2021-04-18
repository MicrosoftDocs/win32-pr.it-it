---
description: Un'applicazione invia il \_ messaggio WM MDIMAXIMIZE a una finestra del client di interfaccia a documenti multipli (MDI) per ingrandire una finestra figlio MDI.
ms.assetid: 7c5e4157-13f6-40d7-a64a-076bd14aca0d
title: Messaggio WM_MDIMAXIMIZE (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8372bcb25f35a52793292de4fd94a4a9dadafe6a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306663"
---
# <a name="wm_mdimaximize-message"></a><span data-ttu-id="be989-103">\_Messaggio MDIMAXIMIZE WM</span><span class="sxs-lookup"><span data-stu-id="be989-103">WM\_MDIMAXIMIZE message</span></span>

<span data-ttu-id="be989-104">Un'applicazione invia il messaggio **WM \_ MDIMAXIMIZE** a una finestra del client di interfaccia a documenti multipli (MDI) per ingrandire una finestra figlio MDI.</span><span class="sxs-lookup"><span data-stu-id="be989-104">An application sends the **WM\_MDIMAXIMIZE** message to a multiple-document interface (MDI) client window to maximize an MDI child window.</span></span> <span data-ttu-id="be989-105">Il sistema ridimensiona la finestra figlio per fare in modo che l'area client riempia la finestra del client.</span><span class="sxs-lookup"><span data-stu-id="be989-105">The system resizes the child window to make its client area fill the client window.</span></span> <span data-ttu-id="be989-106">Il sistema posiziona l'icona del menu finestra della finestra figlio nella posizione più a destra della barra dei menu della finestra cornice e posiziona l'icona di ripristino della finestra figlio nella posizione più a sinistra.</span><span class="sxs-lookup"><span data-stu-id="be989-106">The system places the child window's window menu icon in the rightmost position of the frame window's menu bar, and places the child window's restore icon in the leftmost position.</span></span> <span data-ttu-id="be989-107">Il sistema aggiunge anche il testo della barra del titolo della finestra figlio a quello della finestra cornice.</span><span class="sxs-lookup"><span data-stu-id="be989-107">The system also appends the title bar text of the child window to that of the frame window.</span></span>


```C++
#define WM_MDIMAXIMIZE                  0x0225
```



## <a name="parameters"></a><span data-ttu-id="be989-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="be989-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="be989-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="be989-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="be989-110">Handle per la finestra figlio MDI da ingrandire.</span><span class="sxs-lookup"><span data-stu-id="be989-110">A handle to the MDI child window to be maximized.</span></span>

</dd> <dt>

<span data-ttu-id="be989-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="be989-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="be989-112">Questo parametro non viene usato.</span><span class="sxs-lookup"><span data-stu-id="be989-112">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="be989-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="be989-113">Return value</span></span>

<span data-ttu-id="be989-114">Tipo: **zero**</span><span class="sxs-lookup"><span data-stu-id="be989-114">Type: **zero**</span></span>

<span data-ttu-id="be989-115">Il valore restituito è sempre zero.</span><span class="sxs-lookup"><span data-stu-id="be989-115">The return value is always zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="be989-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="be989-116">Remarks</span></span>

<span data-ttu-id="be989-117">Se una finestra client MDI riceve un messaggio che modifica l'attivazione delle finestre figlio mentre la finestra figlio MDI attualmente attiva è ingrandita, il sistema ripristina la finestra figlio attiva e ingrandisce la finestra figlio appena attivata.</span><span class="sxs-lookup"><span data-stu-id="be989-117">If an MDI client window receives any message that changes the activation of its child windows while the currently active MDI child window is maximized, the system restores the active child window and maximizes the newly activated child window.</span></span>

## <a name="requirements"></a><span data-ttu-id="be989-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="be989-118">Requirements</span></span>



| <span data-ttu-id="be989-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="be989-119">Requirement</span></span> | <span data-ttu-id="be989-120">Valore</span><span class="sxs-lookup"><span data-stu-id="be989-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="be989-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="be989-121">Minimum supported client</span></span><br/> | <span data-ttu-id="be989-122">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="be989-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="be989-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="be989-123">Minimum supported server</span></span><br/> | <span data-ttu-id="be989-124">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="be989-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="be989-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="be989-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="be989-126"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="be989-126"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="be989-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="be989-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="be989-128">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="be989-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="be989-129">**\_MDIRESTORE WM**</span><span class="sxs-lookup"><span data-stu-id="be989-129">**WM\_MDIRESTORE**</span></span>](wm-mdirestore.md)
</dt> <dt>

<span data-ttu-id="be989-130">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="be989-130">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="be989-131">Interfaccia a documenti multipli</span><span class="sxs-lookup"><span data-stu-id="be989-131">Multiple Document Interface</span></span>](multiple-document-interface.md)
</dt> </dl>

 

 





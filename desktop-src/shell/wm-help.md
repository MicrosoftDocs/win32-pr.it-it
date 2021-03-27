---
description: Indica che l'utente ha premuto il tasto F1.
ms.assetid: 6a090125-67dd-4267-9973-10e32c6e4f1f
title: Messaggio WM_HELP (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7dd1b042a2e57fb64eb3aa81f38cec336e33efab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104979463"
---
# <a name="wm_help-message"></a><span data-ttu-id="2b405-103">\_Messaggio della Guida WM</span><span class="sxs-lookup"><span data-stu-id="2b405-103">WM\_HELP message</span></span>

<span data-ttu-id="2b405-104">Indica che l'utente ha premuto il tasto F1.</span><span class="sxs-lookup"><span data-stu-id="2b405-104">Indicates that the user pressed the F1 key.</span></span> <span data-ttu-id="2b405-105">Se un menu è attivo quando si preme F1, **la \_ Guida di WM** viene inviata alla finestra associata al menu. in caso contrario, la **\_ Guida di WM** viene inviata alla finestra con lo stato attivo della tastiera.</span><span class="sxs-lookup"><span data-stu-id="2b405-105">If a menu is active when F1 is pressed, **WM\_HELP** is sent to the window associated with the menu; otherwise, **WM\_HELP** is sent to the window that has the keyboard focus.</span></span> <span data-ttu-id="2b405-106">Se nessuna finestra dispone dello stato attivo della tastiera, la **\_ Guida WM** viene inviata alla finestra attualmente attiva.</span><span class="sxs-lookup"><span data-stu-id="2b405-106">If no window has the keyboard focus, **WM\_HELP** is sent to the currently active window.</span></span>

## <a name="parameters"></a><span data-ttu-id="2b405-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="2b405-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2b405-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2b405-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2b405-109">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="2b405-109">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="2b405-110">*lphi*</span><span class="sxs-lookup"><span data-stu-id="2b405-110">*lphi*</span></span> 
</dt> <dd>

<span data-ttu-id="2b405-111">Indirizzo di una struttura [**HELPINFO**](/windows/win32/api/winuser/ns-winuser-helpinfo) che contiene informazioni sulla voce di menu, il controllo, la finestra di dialogo o la finestra per la quale è richiesta la guida.</span><span class="sxs-lookup"><span data-stu-id="2b405-111">The address of a [**HELPINFO**](/windows/win32/api/winuser/ns-winuser-helpinfo) structure that contains information about the menu item, control, dialog box, or window for which Help is requested.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2b405-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2b405-112">Return value</span></span>

<span data-ttu-id="2b405-113">Restituisce **true**.</span><span class="sxs-lookup"><span data-stu-id="2b405-113">Returns **TRUE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="2b405-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="2b405-114">Remarks</span></span>

<span data-ttu-id="2b405-115">La funzione [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) passa **la \_ Guida WM** alla finestra padre di una finestra figlio o al proprietario di una finestra di primo livello.</span><span class="sxs-lookup"><span data-stu-id="2b405-115">The [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function passes **WM\_HELP** to the parent window of a child window or to the owner of a top-level window.</span></span>

## <a name="requirements"></a><span data-ttu-id="2b405-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2b405-116">Requirements</span></span>



| <span data-ttu-id="2b405-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="2b405-117">Requirement</span></span> | <span data-ttu-id="2b405-118">Valore</span><span class="sxs-lookup"><span data-stu-id="2b405-118">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="2b405-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2b405-119">Minimum supported client</span></span><br/> | <span data-ttu-id="2b405-120">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="2b405-120">Windows XP \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="2b405-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2b405-121">Minimum supported server</span></span><br/> | <span data-ttu-id="2b405-122">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="2b405-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="2b405-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2b405-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="2b405-124"><dt>Winuser. h</dt></span><span class="sxs-lookup"><span data-stu-id="2b405-124"><dt>Winuser.h</dt></span></span> </dl> |



 

 

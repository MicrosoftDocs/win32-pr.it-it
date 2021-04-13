---
title: Messaggio ACM_OPEN (COMmctrl. h)
description: Apre un clip AVI e ne Visualizza il primo fotogramma in un controllo dell'animazione. È possibile inviare questo messaggio in modo esplicito o usare la \_ macro OpenEx, animate Open o animate \_ . Si consiglia di usare la versione Unicode di questo messaggio, ACM \_ OPENW.
ms.assetid: 87f476ce-bb27-4b5f-bfdf-dff84bd7e4f4
keywords:
- Controlli di Windows Message ACM_OPEN
topic_type:
- apiref
api_name:
- ACM_OPEN
- ACM_OPENA
- ACM_OPENW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0588c0e321efe5cace63baf4016dbaa97f735252
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400360"
---
# <a name="acm_open-message"></a><span data-ttu-id="49a95-106">\_Messaggio aperto ACM</span><span class="sxs-lookup"><span data-stu-id="49a95-106">ACM\_OPEN message</span></span>

<span data-ttu-id="49a95-107">Apre un clip AVI e ne Visualizza il primo fotogramma in un controllo dell'animazione.</span><span class="sxs-lookup"><span data-stu-id="49a95-107">Opens an AVI clip and displays its first frame in an animation control.</span></span> <span data-ttu-id="49a95-108">È possibile inviare questo messaggio in modo esplicito o usare la macro OpenEx, [**animate \_ Open**](/windows/desktop/api/Commctrl/nf-commctrl-animate_open) o [**\_ animate**](/windows/desktop/api/Commctrl/nf-commctrl-animate_openex) .</span><span class="sxs-lookup"><span data-stu-id="49a95-108">You can send this message explicitly or use the [**Animate\_Open**](/windows/desktop/api/Commctrl/nf-commctrl-animate_open) or [**Animate\_OpenEx**](/windows/desktop/api/Commctrl/nf-commctrl-animate_openex) macro.</span></span> <span data-ttu-id="49a95-109">Si consiglia di usare la versione Unicode di questo messaggio, ACM \_ OPENW.</span><span class="sxs-lookup"><span data-stu-id="49a95-109">We recommend using the Unicode version of this message, ACM\_OPENW.</span></span>

## <a name="parameters"></a><span data-ttu-id="49a95-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="49a95-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="49a95-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="49a95-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="49a95-112">[Versione 4,71](common-control-versions.md) e successive.</span><span class="sxs-lookup"><span data-stu-id="49a95-112">[Version 4.71](common-control-versions.md) and later.</span></span> <span data-ttu-id="49a95-113">Handle di istanza per il modulo da cui deve essere caricata la risorsa.</span><span class="sxs-lookup"><span data-stu-id="49a95-113">An instance handle to the module from which the resource should be loaded.</span></span> <span data-ttu-id="49a95-114">Impostare questo valore su **null** per fare in modo che il controllo usi il valore HINSTANCE usato per creare la finestra.</span><span class="sxs-lookup"><span data-stu-id="49a95-114">Set this value to **NULL** to have the control use the HINSTANCE value used to create the window.</span></span> <span data-ttu-id="49a95-115">Si noti che se la finestra viene creata da una DLL, il valore predefinito per *wParam* è il valore HINSTANCE della dll, non dell'applicazione che chiama la dll.</span><span class="sxs-lookup"><span data-stu-id="49a95-115">Note that if the window is created by a DLL, the default value for *wParam* is the HINSTANCE value of the DLL, not of the application that calls the DLL.</span></span>

</dd> <dt>

<span data-ttu-id="49a95-116">*lParam*</span><span class="sxs-lookup"><span data-stu-id="49a95-116">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="49a95-117">Puntatore a un buffer che contiene il percorso del file AVI o il nome di una risorsa AVI.</span><span class="sxs-lookup"><span data-stu-id="49a95-117">A pointer to a buffer that contains the path of the AVI file or the name of an AVI resource.</span></span> <span data-ttu-id="49a95-118">In alternativa, questo parametro può essere costituito dall'identificatore di risorsa AVI in [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) e da zero in [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="49a95-118">Alternatively, this parameter can consist of the AVI resource identifier in the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) and zero in the [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)).</span></span> <span data-ttu-id="49a95-119">Per creare questo valore, usare la macro [**MAKEINTRESOURCE**](/windows/desktop/api/winuser/nf-winuser-makeintresourcea) .</span><span class="sxs-lookup"><span data-stu-id="49a95-119">To create this value, use the [**MAKEINTRESOURCE**](/windows/desktop/api/winuser/nf-winuser-makeintresourcea) macro.</span></span> <span data-ttu-id="49a95-120">Il controllo carica la risorsa AVI dal modulo specificato dall'handle di istanza passato alla funzione [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) , alla macro [**\_ create animate**](/windows/desktop/api/Commctrl/nf-commctrl-animate_create) o alla funzione di creazione della finestra di dialogo che ha creato il controllo.</span><span class="sxs-lookup"><span data-stu-id="49a95-120">The control loads the AVI resource from the module specified by the instance handle passed to the [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) function, the [**Animate\_Create**](/windows/desktop/api/Commctrl/nf-commctrl-animate_create) macro, or the dialog box creation function that created the control.</span></span> <span data-ttu-id="49a95-121">Nella [versione 4,71](common-control-versions.md) e successive la risorsa viene caricata dal modulo specificato da *wParam*.</span><span class="sxs-lookup"><span data-stu-id="49a95-121">In [Version 4.71](common-control-versions.md) and later, the resource is loaded from the module specified by *wParam*.</span></span> <span data-ttu-id="49a95-122">Una risorsa AVI deve avere il tipo "AVI".</span><span class="sxs-lookup"><span data-stu-id="49a95-122">An AVI resource must have the "AVI" type.</span></span> <span data-ttu-id="49a95-123">Se questo parametro è **null**, il sistema chiude il file AVI che è stato precedentemente aperto per il controllo di animazione specificato, se presente.</span><span class="sxs-lookup"><span data-stu-id="49a95-123">If this parameter is **NULL**, the system closes the AVI file that was previously opened for the specified animation control, if any.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="49a95-124">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="49a95-124">Return value</span></span>

<span data-ttu-id="49a95-125">Restituisce un valore diverso da zero se ha esito positivo oppure zero in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="49a95-125">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="49a95-126">Commenti</span><span class="sxs-lookup"><span data-stu-id="49a95-126">Remarks</span></span>

<span data-ttu-id="49a95-127">Il file o la risorsa AVI specificata da *lpszName* non deve contenere audio.</span><span class="sxs-lookup"><span data-stu-id="49a95-127">The AVI file or resource specified by *lpszName* must not contain audio.</span></span>

<span data-ttu-id="49a95-128">Si consiglia di usare la versione Unicode di questo messaggio, ACM \_ OPENW.</span><span class="sxs-lookup"><span data-stu-id="49a95-128">We recommend using the Unicode version of this message, ACM\_OPENW.</span></span>

<span data-ttu-id="49a95-129">È possibile aprire solo clip AVI invisibile all'utente.</span><span class="sxs-lookup"><span data-stu-id="49a95-129">You can only open silent AVI clips.</span></span> <span data-ttu-id="49a95-130">\_L'apertura e l' [**animazione \_**](/windows/desktop/api/Commctrl/nf-commctrl-animate_open) di ACM Open hanno esito negativo se *lParam* specifica una clip AVI contenente un suono.</span><span class="sxs-lookup"><span data-stu-id="49a95-130">ACM\_OPEN and [**Animate\_Open**](/windows/desktop/api/Commctrl/nf-commctrl-animate_open) fail if *lParam* specifies an AVI clip that contains sound.</span></span>

<span data-ttu-id="49a95-131">È possibile usare l' [**animazione \_ Close**](/windows/desktop/api/Commctrl/nf-commctrl-animate_close) per chiudere un file AVI o una risorsa AVI precedentemente aperta per il controllo di animazione specificato.</span><span class="sxs-lookup"><span data-stu-id="49a95-131">You can use [**Animate\_Close**](/windows/desktop/api/Commctrl/nf-commctrl-animate_close) to close an AVI file or AVI resource that was previously opened for the specified animation control.</span></span>

## <a name="requirements"></a><span data-ttu-id="49a95-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="49a95-132">Requirements</span></span>



| <span data-ttu-id="49a95-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="49a95-133">Requirement</span></span> | <span data-ttu-id="49a95-134">Valore</span><span class="sxs-lookup"><span data-stu-id="49a95-134">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="49a95-135">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="49a95-135">Minimum supported client</span></span><br/> | <span data-ttu-id="49a95-136">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="49a95-136">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="49a95-137">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="49a95-137">Minimum supported server</span></span><br/> | <span data-ttu-id="49a95-138">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="49a95-138">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="49a95-139">Intestazione</span><span class="sxs-lookup"><span data-stu-id="49a95-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="49a95-140"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="49a95-140"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="49a95-141">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="49a95-141">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="49a95-142">**ACM \_ OPENW** (Unicode) e **ACM \_ Opena** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="49a95-142">**ACM\_OPENW** (Unicode) and **ACM\_OPENA** (ANSI)</span></span><br/>                         |



 


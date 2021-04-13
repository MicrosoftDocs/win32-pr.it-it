---
title: Messaggio EM_GETHANDLE (winuser. h)
description: Ottiene un handle della memoria attualmente allocata per il testo di un controllo di modifica su più righe.
ms.assetid: 74271812-9715-4a46-96b3-0788134f8143
keywords:
- Controlli di Windows Message EM_GETHANDLE
topic_type:
- apiref
api_name:
- EM_GETHANDLE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88a466394b48d2d726621e50a7e2c5df2f747f08
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518298"
---
# <a name="em_gethandle-message"></a><span data-ttu-id="1a3a2-104">\_Messaggio GETHANDLE em</span><span class="sxs-lookup"><span data-stu-id="1a3a2-104">EM\_GETHANDLE message</span></span>

<span data-ttu-id="1a3a2-105">Ottiene un handle della memoria attualmente allocata per il testo di un controllo di modifica su più righe.</span><span class="sxs-lookup"><span data-stu-id="1a3a2-105">Gets a handle of the memory currently allocated for a multiline edit control's text.</span></span>

## <a name="parameters"></a><span data-ttu-id="1a3a2-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="1a3a2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1a3a2-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1a3a2-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1a3a2-108">Non utilizzato; deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="1a3a2-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="1a3a2-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1a3a2-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1a3a2-110">Non utilizzato; deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="1a3a2-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1a3a2-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1a3a2-111">Return value</span></span>

<span data-ttu-id="1a3a2-112">Il valore restituito è un handle di memoria che identifica il buffer che include il contenuto del controllo di modifica.</span><span class="sxs-lookup"><span data-stu-id="1a3a2-112">The return value is a memory handle identifying the buffer that holds the content of the edit control.</span></span> <span data-ttu-id="1a3a2-113">Se si verifica un errore, ad esempio l'invio del messaggio a un controllo di modifica a riga singola, il valore restituito è zero.</span><span class="sxs-lookup"><span data-stu-id="1a3a2-113">If an error occurs, such as sending the message to a single-line edit control, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="1a3a2-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="1a3a2-114">Remarks</span></span>

<span data-ttu-id="1a3a2-115">Se la funzione ha esito positivo, l'applicazione può accedere al contenuto del controllo di modifica eseguendo il cast del valore restituito a [**HLOCAL**](/windows/desktop/WinProg/windows-data-types) e passandolo a [**LocalLock**](/windows/desktop/api/winbase/nf-winbase-locallock).</span><span class="sxs-lookup"><span data-stu-id="1a3a2-115">If the function succeeds, the application can access the contents of the edit control by casting the return value to [**HLOCAL**](/windows/desktop/WinProg/windows-data-types) and passing it to [**LocalLock**](/windows/desktop/api/winbase/nf-winbase-locallock).</span></span> <span data-ttu-id="1a3a2-116">**LocalLock** restituisce un puntatore a un buffer che è una matrice con terminazione null di **char** s o **WCHAR** s, a seconda che una funzione ANSI o Unicode abbia creato il controllo.</span><span class="sxs-lookup"><span data-stu-id="1a3a2-116">**LocalLock** returns a pointer to a buffer that is a null-terminated array of **CHAR** s or **WCHAR** s, depending on whether an ANSI or Unicode function created the control.</span></span> <span data-ttu-id="1a3a2-117">Se, ad esempio, è stato usato [**CreateWindowExA**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) , il buffer è una matrice di **char** s, ma se è stato usato **CreateWindowExW** , il buffer è una matrice di **WCHAR** s.</span><span class="sxs-lookup"><span data-stu-id="1a3a2-117">For example, if [**CreateWindowExA**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) was used the buffer is an array of **CHAR** s, but if **CreateWindowExW** was used the buffer is an array of **WCHAR** s.</span></span> <span data-ttu-id="1a3a2-118">È possibile che l'applicazione non modifichi il contenuto del buffer.</span><span class="sxs-lookup"><span data-stu-id="1a3a2-118">The application may not change the contents of the buffer.</span></span> <span data-ttu-id="1a3a2-119">Per sbloccare il buffer, l'applicazione chiama [**LocalUnlock**](/windows/desktop/api/winbase/nf-winbase-localunlock) prima di consentire al controllo di modifica di ricevere nuovi messaggi.</span><span class="sxs-lookup"><span data-stu-id="1a3a2-119">To unlock the buffer, the application calls [**LocalUnlock**](/windows/desktop/api/winbase/nf-winbase-localunlock) before allowing the edit control to receive new messages.</span></span>

> [!Note]  
> <span data-ttu-id="1a3a2-120">Per Comctl32.dll versione 6, il buffer contiene sempre una matrice di **WCHAR**, indipendentemente dal fatto che una funzione ANSI o Unicode abbia creato il controllo di modifica.</span><span class="sxs-lookup"><span data-stu-id="1a3a2-120">For Comctl32.dll version 6, the buffer always contains an array of **WCHAR** s, regardless of whether an ANSI or Unicode function created the edit control.</span></span> <span data-ttu-id="1a3a2-121">Per altre informazioni sulle versioni di DLL, vedere [versioni di controllo comuni](common-control-versions.md).</span><span class="sxs-lookup"><span data-stu-id="1a3a2-121">For more information on DLL versions, see [Common Control Versions](common-control-versions.md).</span></span>

 

<span data-ttu-id="1a3a2-122">Se l'applicazione non può rispettare le restrizioni imposte da **em \_ GetHandle**, usare le funzioni [**GetWindowTextLength**](/windows/desktop/api/winuser/nf-winuser-getwindowtextlengtha) e [**GetWindowText**](/windows/desktop/api/winuser/nf-winuser-getwindowtexta) per copiare il contenuto del controllo di modifica in un buffer fornito dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="1a3a2-122">If your application cannot abide by the restrictions imposed by **EM\_GETHANDLE**, use the [**GetWindowTextLength**](/windows/desktop/api/winuser/nf-winuser-getwindowtextlengtha) and [**GetWindowText**](/windows/desktop/api/winuser/nf-winuser-getwindowtexta) functions to copy the contents of the edit control into an application-provided buffer.</span></span>

<span data-ttu-id="1a3a2-123">**Modifica avanzata:** Il **messaggio \_ GetHandle em** non è supportato.</span><span class="sxs-lookup"><span data-stu-id="1a3a2-123">**Rich Edit:** The **EM\_GETHANDLE** message is not supported.</span></span> <span data-ttu-id="1a3a2-124">I controlli Rich Edit non archiviano il testo come una semplice matrice di caratteri.</span><span class="sxs-lookup"><span data-stu-id="1a3a2-124">Rich edit controls do not store text as a simple array of characters.</span></span>

## <a name="requirements"></a><span data-ttu-id="1a3a2-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1a3a2-125">Requirements</span></span>



| <span data-ttu-id="1a3a2-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="1a3a2-126">Requirement</span></span> | <span data-ttu-id="1a3a2-127">Valore</span><span class="sxs-lookup"><span data-stu-id="1a3a2-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1a3a2-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1a3a2-128">Minimum supported client</span></span><br/> | <span data-ttu-id="1a3a2-129">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="1a3a2-129">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="1a3a2-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1a3a2-130">Minimum supported server</span></span><br/> | <span data-ttu-id="1a3a2-131">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="1a3a2-131">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="1a3a2-132">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1a3a2-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="1a3a2-133"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1a3a2-133"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1a3a2-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1a3a2-134">See also</span></span>

<dl> <dt>

<span data-ttu-id="1a3a2-135">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="1a3a2-135">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="1a3a2-136">**filehandle EM \_**</span><span class="sxs-lookup"><span data-stu-id="1a3a2-136">**EM\_SETHANDLE**</span></span>](em-sethandle.md)
</dt> <dt>

<span data-ttu-id="1a3a2-137">**Altre risorse**</span><span class="sxs-lookup"><span data-stu-id="1a3a2-137">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="1a3a2-138">**GetWindowText**</span><span class="sxs-lookup"><span data-stu-id="1a3a2-138">**GetWindowText**</span></span>](/windows/desktop/api/winuser/nf-winuser-getwindowtexta)
</dt> <dt>

[<span data-ttu-id="1a3a2-139">**GetWindowTextLength**</span><span class="sxs-lookup"><span data-stu-id="1a3a2-139">**GetWindowTextLength**</span></span>](/windows/desktop/api/winuser/nf-winuser-getwindowtextlengtha)
</dt> <dt>

[<span data-ttu-id="1a3a2-140">**LocalLock**</span><span class="sxs-lookup"><span data-stu-id="1a3a2-140">**LocalLock**</span></span>](/windows/desktop/api/winbase/nf-winbase-locallock)
</dt> <dt>

[<span data-ttu-id="1a3a2-141">**LocalUnlock**</span><span class="sxs-lookup"><span data-stu-id="1a3a2-141">**LocalUnlock**</span></span>](/windows/desktop/api/winbase/nf-winbase-localunlock)
</dt> </dl>

 


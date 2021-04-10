---
title: Messaggio HELPMSGSTRING (COMMDLG. h)
description: Una finestra di dialogo comune invia il messaggio registrato HELPMSGSTRING alla routine della finestra proprietaria quando l'utente fa clic sul pulsante?.
ms.assetid: 21c0fcf5-785b-4005-8133-e48347f991a8
keywords:
- Finestre di dialogo del messaggio HELPMSGSTRING
topic_type:
- apiref
api_name:
- HELPMSGSTRING
- HELPMSGSTRINGA
- HELPMSGSTRINGW
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac3f7a883f50b06c8d142cb83bedf0bfa2920191
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121326"
---
# <a name="helpmsgstring-message"></a><span data-ttu-id="5b16f-104">Messaggio HELPMSGSTRING</span><span class="sxs-lookup"><span data-stu-id="5b16f-104">HELPMSGSTRING message</span></span>

<span data-ttu-id="5b16f-105">Una finestra di dialogo comune invia il messaggio registrato **HELPMSGSTRING** alla routine della finestra proprietaria quando l'utente fa clic sul **pulsante?** .</span><span class="sxs-lookup"><span data-stu-id="5b16f-105">A common dialog box sends the **HELPMSGSTRING** registered message to the window procedure of its owner window when the user clicks the **Help** button.</span></span>


```C++
#define HELPMSGSTRING TEXT("commdlg_help")
```



## <a name="parameters"></a><span data-ttu-id="5b16f-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="5b16f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5b16f-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5b16f-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5b16f-108">Handle per la finestra di dialogo comune.</span><span class="sxs-lookup"><span data-stu-id="5b16f-108">A handle to the common dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="5b16f-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5b16f-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5b16f-110">Puntatore alla struttura di inizializzazione per la finestra di dialogo comune.</span><span class="sxs-lookup"><span data-stu-id="5b16f-110">A pointer to the initialization structure for the common dialog box.</span></span> <span data-ttu-id="5b16f-111">Questa struttura può essere una struttura [**le CHOOSECOLOR.**](/windows/win32/api/commdlg/ns-commdlg-choosecolora-r1), [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta), [**FindReplace**](/windows/win32/api/commdlg/ns-commdlg-findreplacea), [**OpenFileName**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea), [**PrintDlg**](/windows/win32/api/commdlg/ns-commdlg-printdlga) o [**PAGESETUPDLG**](/windows/win32/api/commdlg/ns-commdlg-pagesetupdlga) .</span><span class="sxs-lookup"><span data-stu-id="5b16f-111">This structure can be a [**CHOOSECOLOR**](/windows/win32/api/commdlg/ns-commdlg-choosecolora-r1), [**CHOOSEFONT**](/windows/win32/api/commdlg/ns-commdlg-choosefonta), [**FINDREPLACE**](/windows/win32/api/commdlg/ns-commdlg-findreplacea), [**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea), [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) or [**PAGESETUPDLG**](/windows/win32/api/commdlg/ns-commdlg-pagesetupdlga) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5b16f-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5b16f-112">Return value</span></span>

<span data-ttu-id="5b16f-113">Questo messaggio non restituisce alcun valore.</span><span class="sxs-lookup"><span data-stu-id="5b16f-113">This message has no return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="5b16f-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="5b16f-114">Remarks</span></span>

<span data-ttu-id="5b16f-115">È necessario specificare la costante **HELPMSGSTRING** in una chiamata alla funzione [**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea) per ottenere l'identificatore del messaggio inviato dalla finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="5b16f-115">You must specify the **HELPMSGSTRING** constant in a call to the [**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea) function to get the identifier for the message sent by the dialog box.</span></span>

<span data-ttu-id="5b16f-116">Quando si crea la finestra di dialogo, utilizzare il membro **hwndOwner** della struttura di inizializzazione per identificare la finestra per la ricezione di messaggi **HELPMSGSTRING** .</span><span class="sxs-lookup"><span data-stu-id="5b16f-116">When you create the dialog box, use the **hwndOwner** member of the initialization structure to identify the window to receive **HELPMSGSTRING** messages.</span></span>

## <a name="requirements"></a><span data-ttu-id="5b16f-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5b16f-117">Requirements</span></span>



| <span data-ttu-id="5b16f-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="5b16f-118">Requirement</span></span> | <span data-ttu-id="5b16f-119">Valore</span><span class="sxs-lookup"><span data-stu-id="5b16f-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5b16f-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5b16f-120">Minimum supported client</span></span><br/> | <span data-ttu-id="5b16f-121">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="5b16f-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="5b16f-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5b16f-122">Minimum supported server</span></span><br/> | <span data-ttu-id="5b16f-123">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="5b16f-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="5b16f-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5b16f-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="5b16f-125"><dt>COMMDLG. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5b16f-125"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="5b16f-126">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="5b16f-126">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="5b16f-127">**HELPMSGSTRINGW** (Unicode) e **HELPMSGSTRINGA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="5b16f-127">**HELPMSGSTRINGW** (Unicode) and **HELPMSGSTRINGA** (ANSI)</span></span><br/>                                    |



## <a name="see-also"></a><span data-ttu-id="5b16f-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5b16f-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="5b16f-129">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="5b16f-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="5b16f-130">**Guida della rete CDN \_**</span><span class="sxs-lookup"><span data-stu-id="5b16f-130">**CDN\_HELP**</span></span>](cdn-help.md)
</dt> <dt>

[<span data-ttu-id="5b16f-131">**LE CHOOSECOLOR.**</span><span class="sxs-lookup"><span data-stu-id="5b16f-131">**CHOOSECOLOR**</span></span>](/windows/win32/api/commdlg/ns-commdlg-choosecolora-r1)
</dt> <dt>

[<span data-ttu-id="5b16f-132">**CHOOSEFONT**</span><span class="sxs-lookup"><span data-stu-id="5b16f-132">**CHOOSEFONT**</span></span>](/windows/win32/api/commdlg/ns-commdlg-choosefonta)
</dt> <dt>

[<span data-ttu-id="5b16f-133">**FINDREPLACE**</span><span class="sxs-lookup"><span data-stu-id="5b16f-133">**FINDREPLACE**</span></span>](/windows/win32/api/commdlg/ns-commdlg-findreplacea)
</dt> <dt>

[<span data-ttu-id="5b16f-134">**OPENFILENAME**</span><span class="sxs-lookup"><span data-stu-id="5b16f-134">**OPENFILENAME**</span></span>](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)
</dt> <dt>

[<span data-ttu-id="5b16f-135">**PRINTDLG**</span><span class="sxs-lookup"><span data-stu-id="5b16f-135">**PRINTDLG**</span></span>](/windows/win32/api/commdlg/ns-commdlg-printdlga)
</dt> <dt>

[<span data-ttu-id="5b16f-136">**PAGESETUPDLG**</span><span class="sxs-lookup"><span data-stu-id="5b16f-136">**PAGESETUPDLG**</span></span>](/windows/win32/api/commdlg/ns-commdlg-pagesetupdlga)
</dt> <dt>

[<span data-ttu-id="5b16f-137">**RegisterWindowMessage**</span><span class="sxs-lookup"><span data-stu-id="5b16f-137">**RegisterWindowMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea)
</dt> <dt>

<span data-ttu-id="5b16f-138">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="5b16f-138">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="5b16f-139">Libreria finestra di dialogo comune</span><span class="sxs-lookup"><span data-stu-id="5b16f-139">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

 


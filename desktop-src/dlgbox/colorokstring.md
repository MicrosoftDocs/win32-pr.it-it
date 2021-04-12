---
title: Messaggio COLOROKSTRING (COMMDLG. h)
description: Una finestra di dialogo colore invia il messaggio registrato COLOROKSTRING alla routine hook, CCHookProc, quando l'utente seleziona un colore e fa clic sul pulsante OK.
ms.assetid: 18b28558-1262-4c88-becf-76ce799b7542
keywords:
- Finestre di dialogo del messaggio COLOROKSTRING
topic_type:
- apiref
api_name:
- COLOROKSTRING
- COLOROKSTRINGA
- COLOROKSTRINGW
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 86229c71f1234efb4b561ac73bc8aa20f6258cdc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119750"
---
# <a name="colorokstring-message"></a><span data-ttu-id="99699-104">Messaggio COLOROKSTRING</span><span class="sxs-lookup"><span data-stu-id="99699-104">COLOROKSTRING message</span></span>

<span data-ttu-id="99699-105">Una finestra di dialogo **colore** invia il messaggio registrato **COLOROKSTRING** alla routine hook, [*CCHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpcchookproc), quando l'utente seleziona un colore e fa clic sul pulsante **OK** .</span><span class="sxs-lookup"><span data-stu-id="99699-105">A **Color** dialog box sends the **COLOROKSTRING** registered message to your hook procedure, [*CCHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpcchookproc), when the user selects a color and clicks the **OK** button.</span></span> <span data-ttu-id="99699-106">La routine hook può accettare il colore e consentire la chiusura della finestra di dialogo oppure rifiutare il colore e forzare la finestra di dialogo in modo che rimanga aperta.</span><span class="sxs-lookup"><span data-stu-id="99699-106">The hook procedure can accept the color and allow the dialog box to close, or reject the color and force the dialog box to remain open.</span></span>


```C++
#define COLOROKSTRING TEXT("commdlg_ColorOK")
```



## <a name="parameters"></a><span data-ttu-id="99699-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="99699-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="99699-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="99699-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="99699-109">Questo parametro non viene usato.</span><span class="sxs-lookup"><span data-stu-id="99699-109">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="99699-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="99699-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="99699-111">Puntatore a una struttura [**le CHOOSECOLOR.**](/windows/win32/api/commdlg/ns-commdlg-choosecolora-r1) .</span><span class="sxs-lookup"><span data-stu-id="99699-111">A pointer to a [**CHOOSECOLOR**](/windows/win32/api/commdlg/ns-commdlg-choosecolora-r1) structure.</span></span> <span data-ttu-id="99699-112">Il membro **rgbResult** della struttura contiene il valore di colore RGB del colore selezionato.</span><span class="sxs-lookup"><span data-stu-id="99699-112">The **rgbResult** member of this structure contains the RGB color value of the selected color.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="99699-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="99699-113">Return value</span></span>

<span data-ttu-id="99699-114">Se la routine hook restituisce zero, la finestra di dialogo **colore** accetta il colore selezionato e si chiude.</span><span class="sxs-lookup"><span data-stu-id="99699-114">If the hook procedure returns zero, the **Color** dialog box accepts the selected color and closes.</span></span>

<span data-ttu-id="99699-115">Se la routine hook restituisce un valore diverso da zero, la finestra di dialogo **colore** rifiuta il colore selezionato e rimane aperto.</span><span class="sxs-lookup"><span data-stu-id="99699-115">If the hook procedure returns a nonzero value, the **Color** dialog box rejects the selected color and remains open.</span></span>

## <a name="remarks"></a><span data-ttu-id="99699-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="99699-116">Remarks</span></span>

<span data-ttu-id="99699-117">La routine hook deve specificare la costante **COLOROKSTRING** in una chiamata alla funzione [**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea) per ottenere l'identificatore del messaggio inviato dalla finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="99699-117">The hook procedure must specify the **COLOROKSTRING** constant in a call to the [**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea) function to get the identifier of the message sent by the dialog box.</span></span>

## <a name="requirements"></a><span data-ttu-id="99699-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="99699-118">Requirements</span></span>



| <span data-ttu-id="99699-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="99699-119">Requirement</span></span> | <span data-ttu-id="99699-120">Valore</span><span class="sxs-lookup"><span data-stu-id="99699-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="99699-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="99699-121">Minimum supported client</span></span><br/> | <span data-ttu-id="99699-122">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="99699-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="99699-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="99699-123">Minimum supported server</span></span><br/> | <span data-ttu-id="99699-124">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="99699-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="99699-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="99699-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="99699-126"><dt>COMMDLG. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="99699-126"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="99699-127">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="99699-127">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="99699-128">**COLOROKSTRINGW** (Unicode) e **COLOROKSTRINGA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="99699-128">**COLOROKSTRINGW** (Unicode) and **COLOROKSTRINGA** (ANSI)</span></span><br/>                                    |



## <a name="see-also"></a><span data-ttu-id="99699-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="99699-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="99699-130">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="99699-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="99699-131">**LE CHOOSECOLOR.**</span><span class="sxs-lookup"><span data-stu-id="99699-131">**CHOOSECOLOR**</span></span>](/windows/win32/api/commdlg/ns-commdlg-choosecolora-r1)
</dt> <dt>

[<span data-ttu-id="99699-132">**RegisterWindowMessage**</span><span class="sxs-lookup"><span data-stu-id="99699-132">**RegisterWindowMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea)
</dt> <dt>

<span data-ttu-id="99699-133">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="99699-133">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="99699-134">Libreria finestra di dialogo comune</span><span class="sxs-lookup"><span data-stu-id="99699-134">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

 


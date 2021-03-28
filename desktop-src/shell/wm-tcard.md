---
description: Inviato a un'applicazione che ha avviato una carta di formazione con la Guida di Windows.
title: Messaggio WM_TCARD (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: fdde7603-9913-4e80-9502-2142ef8a511c
api_name:
- WM_TCARD
api_type:
- HeaderDef
api_location:
- Winuser.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 5eb6a3b5a4b840549b75e152f0420bfa055138c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104227422"
---
# <a name="wm_tcard-message"></a><span data-ttu-id="dd06b-103">\_Messaggio TCARD WM</span><span class="sxs-lookup"><span data-stu-id="dd06b-103">WM\_TCARD message</span></span>

<span data-ttu-id="dd06b-104">Inviato a un'applicazione che ha avviato una carta di formazione con la Guida di Windows.</span><span class="sxs-lookup"><span data-stu-id="dd06b-104">Sent to an application that has initiated a training card with Windows Help.</span></span> <span data-ttu-id="dd06b-105">Il messaggio informa l'applicazione quando l'utente fa clic su un pulsante modificabile.</span><span class="sxs-lookup"><span data-stu-id="dd06b-105">The message informs the application when the user clicks an authorable button.</span></span> <span data-ttu-id="dd06b-106">Un'applicazione avvia una scheda di training specificando il \_ comando help TCARD in una chiamata alla funzione [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa) .</span><span class="sxs-lookup"><span data-stu-id="dd06b-106">An application initiates a training card by specifying the HELP\_TCARD command in a call to the [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa) function.</span></span>

## <a name="parameters"></a><span data-ttu-id="dd06b-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="dd06b-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dd06b-108">*idAction*</span><span class="sxs-lookup"><span data-stu-id="dd06b-108">*idAction*</span></span> 
</dt> <dd>

<span data-ttu-id="dd06b-109">Valore che indica l'azione eseguita dall'utente.</span><span class="sxs-lookup"><span data-stu-id="dd06b-109">A value that indicates the action the user has taken.</span></span> <span data-ttu-id="dd06b-110">Può corrispondere a uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="dd06b-110">This can be one of the following values.</span></span>

<dt>

<span id="IDABORT"></span><span id="idabort"></span>

<span data-ttu-id="dd06b-111"><span id="IDABORT"></span><span id="idabort"></span>**IDABORT**</span><span class="sxs-lookup"><span data-stu-id="dd06b-111"><span id="IDABORT"></span><span id="idabort"></span>**IDABORT**</span></span>


</dt> <dd>

<span data-ttu-id="dd06b-112">L'utente ha fatto clic su un pulsante **Interrompi** modificabile.</span><span class="sxs-lookup"><span data-stu-id="dd06b-112">The user clicked an authorable **Abort** button.</span></span>

</dd> <dt>

<span id="IDCANCEL"></span><span id="idcancel"></span>

<span data-ttu-id="dd06b-113"><span id="IDCANCEL"></span><span id="idcancel"></span>**IDCANCEL**</span><span class="sxs-lookup"><span data-stu-id="dd06b-113"><span id="IDCANCEL"></span><span id="idcancel"></span>**IDCANCEL**</span></span>


</dt> <dd>

<span data-ttu-id="dd06b-114">L'utente ha fatto clic su un pulsante **Annulla** modificabile.</span><span class="sxs-lookup"><span data-stu-id="dd06b-114">The user clicked an authorable **Cancel** button.</span></span>

</dd> <dt>

<span id="IDCLOSE"></span><span id="idclose"></span>

<span data-ttu-id="dd06b-115"><span id="IDCLOSE"></span><span id="idclose"></span>**IDCLOSE**</span><span class="sxs-lookup"><span data-stu-id="dd06b-115"><span id="IDCLOSE"></span><span id="idclose"></span>**IDCLOSE**</span></span>


</dt> <dd>

<span data-ttu-id="dd06b-116">L'utente ha chiuso la scheda di training.</span><span class="sxs-lookup"><span data-stu-id="dd06b-116">The user closed the training card.</span></span>

</dd> <dt>

<span id="IDHELP"></span><span id="idhelp"></span>

<span data-ttu-id="dd06b-117"><span id="IDHELP"></span><span id="idhelp"></span>**IDHELP**</span><span class="sxs-lookup"><span data-stu-id="dd06b-117"><span id="IDHELP"></span><span id="idhelp"></span>**IDHELP**</span></span>


</dt> <dd>

<span data-ttu-id="dd06b-118">L'utente ha fatto clic su un pulsante della **Guida** di Windows modificabile.</span><span class="sxs-lookup"><span data-stu-id="dd06b-118">The user clicked an authorable Windows **Help** button.</span></span>

</dd> <dt>

<span id="IDIGNORE"></span><span id="idignore"></span>

<span data-ttu-id="dd06b-119"><span id="IDIGNORE"></span><span id="idignore"></span>**IDIGNORE**</span><span class="sxs-lookup"><span data-stu-id="dd06b-119"><span id="IDIGNORE"></span><span id="idignore"></span>**IDIGNORE**</span></span>


</dt> <dd>

<span data-ttu-id="dd06b-120">L'utente ha fatto clic su un pulsante **Ignora** modificabile.</span><span class="sxs-lookup"><span data-stu-id="dd06b-120">The user clicked an authorable **Ignore** button.</span></span>

</dd> <dt>

<span id="IDOK"></span><span id="idok"></span>

<span data-ttu-id="dd06b-121"><span id="IDOK"></span><span id="idok"></span>**IDOK**</span><span class="sxs-lookup"><span data-stu-id="dd06b-121"><span id="IDOK"></span><span id="idok"></span>**IDOK**</span></span>


</dt> <dd>

<span data-ttu-id="dd06b-122">L'utente ha fatto clic su un pulsante **OK** modificabile.</span><span class="sxs-lookup"><span data-stu-id="dd06b-122">The user clicked an authorable **OK** button.</span></span>

</dd> <dt>

<span id="IDNO"></span><span id="idno"></span>

<span data-ttu-id="dd06b-123"><span id="IDNO"></span><span id="idno"></span>**IDNO**</span><span class="sxs-lookup"><span data-stu-id="dd06b-123"><span id="IDNO"></span><span id="idno"></span>**IDNO**</span></span>


</dt> <dd>

<span data-ttu-id="dd06b-124">L'utente ha fatto clic su un pulsante **non** modificabile.</span><span class="sxs-lookup"><span data-stu-id="dd06b-124">The user clicked an authorable **No** button.</span></span>

</dd> <dt>

<span id="IDRETRY"></span><span id="idretry"></span>

<span data-ttu-id="dd06b-125"><span id="IDRETRY"></span><span id="idretry"></span>**IDRETRY**</span><span class="sxs-lookup"><span data-stu-id="dd06b-125"><span id="IDRETRY"></span><span id="idretry"></span>**IDRETRY**</span></span>


</dt> <dd>

<span data-ttu-id="dd06b-126">L'utente ha fatto clic su un pulsante di **ripetizione dei tentativi** modificabile.</span><span class="sxs-lookup"><span data-stu-id="dd06b-126">The user clicked an authorable **Retry** button.</span></span>

</dd> <dt>

<span id="HELP_TCARD_DATA"></span><span id="help_tcard_data"></span>

<span data-ttu-id="dd06b-127"><span id="HELP_TCARD_DATA"></span><span id="help_tcard_data"></span>**Guida \_ ai \_ dati di TCARD**</span><span class="sxs-lookup"><span data-stu-id="dd06b-127"><span id="HELP_TCARD_DATA"></span><span id="help_tcard_data"></span>**HELP\_TCARD\_DATA**</span></span>


</dt> <dd>

<span data-ttu-id="dd06b-128">L'utente ha fatto clic su un pulsante modificabile.</span><span class="sxs-lookup"><span data-stu-id="dd06b-128">The user clicked an authorable button.</span></span> <span data-ttu-id="dd06b-129">Il parametro *dwActionData* contiene un valore long integer specificato dall'autore della guida.</span><span class="sxs-lookup"><span data-stu-id="dd06b-129">The *dwActionData* parameter contains a long integer specified by the Help author.</span></span>

</dd> <dt>

<span id="HELP_TCARD_OTHER_CALLER"></span><span id="help_tcard_other_caller"></span>

<span data-ttu-id="dd06b-130"><span id="HELP_TCARD_OTHER_CALLER"></span><span id="help_tcard_other_caller"></span>**Guida \_ TCARD \_ altro \_ chiamante**</span><span class="sxs-lookup"><span data-stu-id="dd06b-130"><span id="HELP_TCARD_OTHER_CALLER"></span><span id="help_tcard_other_caller"></span>**HELP\_TCARD\_OTHER\_CALLER**</span></span>


</dt> <dd>

<span data-ttu-id="dd06b-131">Un'altra applicazione ha richiesto le schede di formazione.</span><span class="sxs-lookup"><span data-stu-id="dd06b-131">Another application has requested training cards.</span></span>

</dd> <dt>

<span id="IDYES"></span><span id="idyes"></span>

<span data-ttu-id="dd06b-132"><span id="IDYES"></span><span id="idyes"></span>**IDYES**</span><span class="sxs-lookup"><span data-stu-id="dd06b-132"><span id="IDYES"></span><span id="idyes"></span>**IDYES**</span></span>


</dt> <dd>

<span data-ttu-id="dd06b-133">L'utente ha fatto clic su un pulsante **Sì** modificabile.</span><span class="sxs-lookup"><span data-stu-id="dd06b-133">The user clicked an authorable **Yes** button.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="dd06b-134">*dwActionData*</span><span class="sxs-lookup"><span data-stu-id="dd06b-134">*dwActionData*</span></span> 
</dt> <dd>

<span data-ttu-id="dd06b-135">Se *idAction* specifica Help \_ TCARD \_ data, questo parametro è un valore **Long** specificato dall'autore della guida.</span><span class="sxs-lookup"><span data-stu-id="dd06b-135">If *idAction* specifies HELP\_TCARD\_DATA, this parameter is a **long** specified by the Help author.</span></span> <span data-ttu-id="dd06b-136">In caso contrario, questo parametro è zero.</span><span class="sxs-lookup"><span data-stu-id="dd06b-136">Otherwise, this parameter is zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dd06b-137">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="dd06b-137">Return value</span></span>

<span data-ttu-id="dd06b-138">Il valore restituito viene ignorato; usare zero.</span><span class="sxs-lookup"><span data-stu-id="dd06b-138">The return value is ignored; use zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="dd06b-139">Requisiti</span><span class="sxs-lookup"><span data-stu-id="dd06b-139">Requirements</span></span>



| <span data-ttu-id="dd06b-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="dd06b-140">Requirement</span></span> | <span data-ttu-id="dd06b-141">Valore</span><span class="sxs-lookup"><span data-stu-id="dd06b-141">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="dd06b-142">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="dd06b-142">Minimum supported client</span></span><br/> | <span data-ttu-id="dd06b-143">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="dd06b-143">Windows XP \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="dd06b-144">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="dd06b-144">Minimum supported server</span></span><br/> | <span data-ttu-id="dd06b-145">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="dd06b-145">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="dd06b-146">Intestazione</span><span class="sxs-lookup"><span data-stu-id="dd06b-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="dd06b-147"><dt>Winuser. h</dt></span><span class="sxs-lookup"><span data-stu-id="dd06b-147"><dt>Winuser.h</dt></span></span> </dl> |



 

 





---
title: Messaggio LBSELCHSTRING (Commdlg.h)
description: Una finestra di dialogo Apri o Salva con nome invia il messaggio registrato LBSELCHSTRING alla procedura hook quando la selezione cambia in una delle caselle di riepilogo o delle caselle combinate della finestra di dialogo.
ms.assetid: 3a8ebc63-b324-43ed-bb6f-34779f6043e7
keywords:
- Finestre di dialogo del messaggio LBSELCHSTRING
topic_type:
- apiref
api_name:
- LBSELCHSTRING
- LBSELCHSTRINGA
- LBSELCHSTRINGW
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 62d61f88bd7cb6a84a94a3d8a246e6045f88a305
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/27/2021
ms.locfileid: "110550046"
---
# <a name="lbselchstring-message"></a><span data-ttu-id="37f05-104">Messaggio LBSELCHSTRING</span><span class="sxs-lookup"><span data-stu-id="37f05-104">LBSELCHSTRING message</span></span>

<span data-ttu-id="37f05-105">\[A partire da Windows Vista, le **finestre di** **dialogo** comuni Apri e Salva con nome sono state sostituite dalla finestra di dialogo [Elemento comune](../shell/common-file-dialog.md).</span><span class="sxs-lookup"><span data-stu-id="37f05-105">\[Starting with Windows Vista, the **Open** and **Save As** common dialog boxes have been superseded by the [Common Item Dialog](../shell/common-file-dialog.md).</span></span> <span data-ttu-id="37f05-106">È consigliabile usare l'API Common Item Dialog al posto di queste finestre di dialogo di Common Dialog Box Library.\]</span><span class="sxs-lookup"><span data-stu-id="37f05-106">We recommended that you use the Common Item Dialog API instead of these dialog boxes from the Common Dialog Box Library.\]</span></span>

<span data-ttu-id="37f05-107">Una **finestra di** dialogo Apri o Salva con nome invia il messaggio registrato  **LBSELCHSTRING** alla procedura hook quando la selezione cambia in una delle caselle di riepilogo o delle caselle combinate della finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="37f05-107">An **Open** or **Save As** dialog box sends the **LBSELCHSTRING** registered message to your hook procedure when the selection changes in any of the list boxes or combo boxes of the dialog box.</span></span>


```C++
#define LBSELCHSTRING TEXT("commdlg_LBSelChangedNotify")
```



## <a name="parameters"></a><span data-ttu-id="37f05-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="37f05-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="37f05-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="37f05-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="37f05-110">Identificatore della casella di riepilogo o della casella combinata in cui è stata modificata la selezione.</span><span class="sxs-lookup"><span data-stu-id="37f05-110">The identifier of the list box or combo box in which the selection changed.</span></span>

</dd> <dt>

<span data-ttu-id="37f05-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="37f05-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="37f05-112">La parola meno ordinata specifica il numero di elemento della stringa selezionata nella casella di riepilogo o nella casella combinata.</span><span class="sxs-lookup"><span data-stu-id="37f05-112">The low-order word specifies the item number of the selected string in the list box or combo box.</span></span> <span data-ttu-id="37f05-113">La parola più alta specifica il tipo di modifica della selezione.</span><span class="sxs-lookup"><span data-stu-id="37f05-113">The high-order word specifies the type of selection change.</span></span> <span data-ttu-id="37f05-114">Questo parametro può avere uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="37f05-114">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="37f05-115">Valore</span><span class="sxs-lookup"><span data-stu-id="37f05-115">Value</span></span>                                                                                                                                                                                                                       | <span data-ttu-id="37f05-116">Significato</span><span class="sxs-lookup"><span data-stu-id="37f05-116">Meaning</span></span>                                                                            |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <span id="CD_LBSELCHANGE"></span><span id="cd_lbselchange"></span><dl> <span data-ttu-id="37f05-117"><dt>**CD \_ LBSELCHANGE**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="37f05-117"><dt>**CD\_LBSELCHANGE**</dt> <dt>0</dt></span></span> </dl>     | <span data-ttu-id="37f05-118">L'elemento è l'unico elemento selezionato in una casella di riepilogo a selezione singola.</span><span class="sxs-lookup"><span data-stu-id="37f05-118">The item is the only item selected in a single-selection list box.</span></span><br/>      |
| <span id="CD_LBSELADD"></span><span id="cd_lbseladd"></span><dl> <span data-ttu-id="37f05-119"><dt>**CD \_ LBSELADD**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="37f05-119"><dt>**CD\_LBSELADD**</dt> <dt>2</dt></span></span> </dl>              | <span data-ttu-id="37f05-120">L'elemento è uno degli elementi selezionati in una casella di riepilogo a selezione multipla.</span><span class="sxs-lookup"><span data-stu-id="37f05-120">The item is one of the items selected in a multiple-selection list box.</span></span><br/> |
| <span id="CD_LBSELSUB"></span><span id="cd_lbselsub"></span><dl> <span data-ttu-id="37f05-121"><dt>**CD \_ LBSELSUB**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="37f05-121"><dt>**CD\_LBSELSUB**</dt> <dt>1</dt></span></span> </dl>              | <span data-ttu-id="37f05-122">L'elemento non è più selezionato in una casella di riepilogo a selezione multipla.</span><span class="sxs-lookup"><span data-stu-id="37f05-122">The item is no longer selected in a multiple-selection list box.</span></span><br/>        |
| <span id="CD_LBSELNOITEMS"></span><span id="cd_lbselnoitems"></span><dl> <span data-ttu-id="37f05-123"><dt>**CD \_ LBSELNOITEMS**</dt> <dt>-1</dt></span><span class="sxs-lookup"><span data-stu-id="37f05-123"><dt>**CD\_LBSELNOITEMS**</dt> <dt>-1</dt></span></span> </dl> | <span data-ttu-id="37f05-124">Non esistono elementi in una casella di riepilogo a selezione multipla.</span><span class="sxs-lookup"><span data-stu-id="37f05-124">No items exist in a multiple-selection list box.</span></span><br/>                        |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="37f05-125">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="37f05-125">Return value</span></span>

<span data-ttu-id="37f05-126">Questo messaggio non ha alcun valore restituito.</span><span class="sxs-lookup"><span data-stu-id="37f05-126">This message has no return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="37f05-127">Commenti</span><span class="sxs-lookup"><span data-stu-id="37f05-127">Remarks</span></span>

<span data-ttu-id="37f05-128">La routine hook deve specificare la costante **LBSELCHSTRING** in una chiamata alla funzione [**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea) per ottenere l'identificatore per il messaggio inviato dalla finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="37f05-128">The hook procedure must specify the **LBSELCHSTRING** constant in a call to the [**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea) function to get the identifier for the message sent by the dialog box.</span></span>

## <a name="requirements"></a><span data-ttu-id="37f05-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="37f05-129">Requirements</span></span>



| <span data-ttu-id="37f05-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="37f05-130">Requirement</span></span> | <span data-ttu-id="37f05-131">Valore</span><span class="sxs-lookup"><span data-stu-id="37f05-131">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="37f05-132">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="37f05-132">Minimum supported client</span></span><br/> | <span data-ttu-id="37f05-133">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="37f05-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="37f05-134">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="37f05-134">Minimum supported server</span></span><br/> | <span data-ttu-id="37f05-135">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="37f05-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="37f05-136">Intestazione</span><span class="sxs-lookup"><span data-stu-id="37f05-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="37f05-137"><dt>Commdlg.h (includere Windows.h)</dt></span><span class="sxs-lookup"><span data-stu-id="37f05-137"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="37f05-138">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="37f05-138">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="37f05-139">**LBSELCHSTRINGW** (Unicode) e **LBSELCHSTRINGA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="37f05-139">**LBSELCHSTRINGW** (Unicode) and **LBSELCHSTRINGA** (ANSI)</span></span><br/>                                    |



## <a name="see-also"></a><span data-ttu-id="37f05-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="37f05-140">See also</span></span>

<dl> <dt>

<span data-ttu-id="37f05-141">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="37f05-141">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="37f05-142">**\_SELCHANGE della rete CDN**</span><span class="sxs-lookup"><span data-stu-id="37f05-142">**CDN\_SELCHANGE**</span></span>](cdn-selchange.md)
</dt> <dt>

[<span data-ttu-id="37f05-143">**TIPO DI RETE \_ CDNCHANGE**</span><span class="sxs-lookup"><span data-stu-id="37f05-143">**CDN\_TYPECHANGE**</span></span>](cdn-typechange.md)
</dt> <dt>

[<span data-ttu-id="37f05-144">**RegisterWindowMessage**</span><span class="sxs-lookup"><span data-stu-id="37f05-144">**RegisterWindowMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea)
</dt> <dt>

<span data-ttu-id="37f05-145">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="37f05-145">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="37f05-146">Libreria di finestre di dialogo comuni</span><span class="sxs-lookup"><span data-stu-id="37f05-146">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>


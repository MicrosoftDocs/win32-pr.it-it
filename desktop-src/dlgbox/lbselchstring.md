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
ms.openlocfilehash: 137429b8fa7eb29fb96ec579e0240c4c282d0766
ms.sourcegitcommit: 8e083a10b3a480dec8a8d74dbd5889f49dea15e4
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/17/2021
ms.locfileid: "107590768"
---
# <a name="lbselchstring-message"></a><span data-ttu-id="bb57a-104">Messaggio LBSELCHSTRING</span><span class="sxs-lookup"><span data-stu-id="bb57a-104">LBSELCHSTRING message</span></span>

<span data-ttu-id="bb57a-105">\[A partire da Windows Vista, le **finestre di** **dialogo** comuni Apri e Salva con nome sono state sostituite dalla finestra di dialogo [Elemento comune](/windows/win32/shell/common-file-dialog).</span><span class="sxs-lookup"><span data-stu-id="bb57a-105">\[Starting with Windows Vista, the **Open** and **Save As** common dialog boxes have been superseded by the [Common Item Dialog](/windows/win32/shell/common-file-dialog).</span></span> <span data-ttu-id="bb57a-106">È consigliabile usare l'API Common Item Dialog al posto di queste finestre di dialogo di Common Dialog Box Library.\]</span><span class="sxs-lookup"><span data-stu-id="bb57a-106">We recommended that you use the Common Item Dialog API instead of these dialog boxes from the Common Dialog Box Library.\]</span></span>

<span data-ttu-id="bb57a-107">Una **finestra di** dialogo Apri o Salva con nome invia il messaggio registrato  **LBSELCHSTRING** alla procedura hook quando la selezione cambia in una delle caselle di riepilogo o delle caselle combinate della finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="bb57a-107">An **Open** or **Save As** dialog box sends the **LBSELCHSTRING** registered message to your hook procedure when the selection changes in any of the list boxes or combo boxes of the dialog box.</span></span>


```C++
#define LBSELCHSTRING TEXT("commdlg_LBSelChangedNotify")
```



## <a name="parameters"></a><span data-ttu-id="bb57a-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="bb57a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bb57a-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="bb57a-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bb57a-110">Identificatore della casella di riepilogo o della casella combinata in cui è stata modificata la selezione.</span><span class="sxs-lookup"><span data-stu-id="bb57a-110">The identifier of the list box or combo box in which the selection changed.</span></span>

</dd> <dt>

<span data-ttu-id="bb57a-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="bb57a-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bb57a-112">La parola meno ordinata specifica il numero di elemento della stringa selezionata nella casella di riepilogo o nella casella combinata.</span><span class="sxs-lookup"><span data-stu-id="bb57a-112">The low-order word specifies the item number of the selected string in the list box or combo box.</span></span> <span data-ttu-id="bb57a-113">La parola più alta specifica il tipo di modifica della selezione.</span><span class="sxs-lookup"><span data-stu-id="bb57a-113">The high-order word specifies the type of selection change.</span></span> <span data-ttu-id="bb57a-114">Questo parametro può avere uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="bb57a-114">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="bb57a-115">Valore</span><span class="sxs-lookup"><span data-stu-id="bb57a-115">Value</span></span>                                                                                                                                                                                                                       | <span data-ttu-id="bb57a-116">Significato</span><span class="sxs-lookup"><span data-stu-id="bb57a-116">Meaning</span></span>                                                                            |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <span id="CD_LBSELCHANGE"></span><span id="cd_lbselchange"></span><dl> <span data-ttu-id="bb57a-117"><dt>**CD \_ LBSELCHANGE**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="bb57a-117"><dt>**CD\_LBSELCHANGE**</dt> <dt>0</dt></span></span> </dl>     | <span data-ttu-id="bb57a-118">L'elemento è l'unico elemento selezionato in una casella di riepilogo a selezione singola.</span><span class="sxs-lookup"><span data-stu-id="bb57a-118">The item is the only item selected in a single-selection list box.</span></span><br/>      |
| <span id="CD_LBSELADD"></span><span id="cd_lbseladd"></span><dl> <span data-ttu-id="bb57a-119"><dt>**CD \_ LBSELADD**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="bb57a-119"><dt>**CD\_LBSELADD**</dt> <dt>2</dt></span></span> </dl>              | <span data-ttu-id="bb57a-120">L'elemento è uno degli elementi selezionati in una casella di riepilogo a selezione multipla.</span><span class="sxs-lookup"><span data-stu-id="bb57a-120">The item is one of the items selected in a multiple-selection list box.</span></span><br/> |
| <span id="CD_LBSELSUB"></span><span id="cd_lbselsub"></span><dl> <span data-ttu-id="bb57a-121"><dt>**CD \_ LBSELSUB**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="bb57a-121"><dt>**CD\_LBSELSUB**</dt> <dt>1</dt></span></span> </dl>              | <span data-ttu-id="bb57a-122">L'elemento non è più selezionato in una casella di riepilogo a selezione multipla.</span><span class="sxs-lookup"><span data-stu-id="bb57a-122">The item is no longer selected in a multiple-selection list box.</span></span><br/>        |
| <span id="CD_LBSELNOITEMS"></span><span id="cd_lbselnoitems"></span><dl> <span data-ttu-id="bb57a-123"><dt>**CD \_ LBSELNOITEMS**</dt> <dt>-1</dt></span><span class="sxs-lookup"><span data-stu-id="bb57a-123"><dt>**CD\_LBSELNOITEMS**</dt> <dt>-1</dt></span></span> </dl> | <span data-ttu-id="bb57a-124">Non esistono elementi in una casella di riepilogo a selezione multipla.</span><span class="sxs-lookup"><span data-stu-id="bb57a-124">No items exist in a multiple-selection list box.</span></span><br/>                        |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bb57a-125">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="bb57a-125">Return value</span></span>

<span data-ttu-id="bb57a-126">Questo messaggio non ha alcun valore restituito.</span><span class="sxs-lookup"><span data-stu-id="bb57a-126">This message has no return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="bb57a-127">Commenti</span><span class="sxs-lookup"><span data-stu-id="bb57a-127">Remarks</span></span>

<span data-ttu-id="bb57a-128">La routine hook deve specificare la costante **LBSELCHSTRING** in una chiamata alla funzione [**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea) per ottenere l'identificatore per il messaggio inviato dalla finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="bb57a-128">The hook procedure must specify the **LBSELCHSTRING** constant in a call to the [**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea) function to get the identifier for the message sent by the dialog box.</span></span>

## <a name="requirements"></a><span data-ttu-id="bb57a-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bb57a-129">Requirements</span></span>



| <span data-ttu-id="bb57a-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="bb57a-130">Requirement</span></span> | <span data-ttu-id="bb57a-131">Valore</span><span class="sxs-lookup"><span data-stu-id="bb57a-131">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bb57a-132">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bb57a-132">Minimum supported client</span></span><br/> | <span data-ttu-id="bb57a-133">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="bb57a-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="bb57a-134">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bb57a-134">Minimum supported server</span></span><br/> | <span data-ttu-id="bb57a-135">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="bb57a-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="bb57a-136">Intestazione</span><span class="sxs-lookup"><span data-stu-id="bb57a-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="bb57a-137"><dt>Commdlg.h (includere Windows.h)</dt></span><span class="sxs-lookup"><span data-stu-id="bb57a-137"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="bb57a-138">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="bb57a-138">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="bb57a-139">**LBSELCHSTRINGW** (Unicode) e **LBSELCHSTRINGA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="bb57a-139">**LBSELCHSTRINGW** (Unicode) and **LBSELCHSTRINGA** (ANSI)</span></span><br/>                                    |



## <a name="see-also"></a><span data-ttu-id="bb57a-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bb57a-140">See also</span></span>

<dl> <dt>

<span data-ttu-id="bb57a-141">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="bb57a-141">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="bb57a-142">**\_SELCHANGE della rete CDN**</span><span class="sxs-lookup"><span data-stu-id="bb57a-142">**CDN\_SELCHANGE**</span></span>](cdn-selchange.md)
</dt> <dt>

[<span data-ttu-id="bb57a-143">**TYPECHANGE della rete \_ CDN**</span><span class="sxs-lookup"><span data-stu-id="bb57a-143">**CDN\_TYPECHANGE**</span></span>](cdn-typechange.md)
</dt> <dt>

[<span data-ttu-id="bb57a-144">**RegisterWindowMessage**</span><span class="sxs-lookup"><span data-stu-id="bb57a-144">**RegisterWindowMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea)
</dt> <dt>

<span data-ttu-id="bb57a-145">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="bb57a-145">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="bb57a-146">Libreria di finestre di dialogo comuni</span><span class="sxs-lookup"><span data-stu-id="bb57a-146">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

 


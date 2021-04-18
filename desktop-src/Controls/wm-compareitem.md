---
title: Messaggio WM_COMPAREITEM (winuser. h)
description: Inviato per determinare la posizione relativa di un nuovo elemento nell'elenco ordinato di una casella combinata creata dal proprietario o di una casella di riepilogo.
ms.assetid: 22882730-9fd6-4b45-a563-d7b00ed26564
keywords:
- Controlli di Windows Message WM_COMPAREITEM
topic_type:
- apiref
api_name:
- WM_COMPAREITEM
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f269b90f00e69cce2fb84e6b4efa76e554ad96f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475113"
---
# <a name="wm_compareitem-message"></a><span data-ttu-id="4873e-104">\_Messaggio COMPAREITEM WM</span><span class="sxs-lookup"><span data-stu-id="4873e-104">WM\_COMPAREITEM message</span></span>

<span data-ttu-id="4873e-105">Inviato per determinare la posizione relativa di un nuovo elemento nell'elenco ordinato di una casella combinata creata dal proprietario o di una casella di riepilogo.</span><span class="sxs-lookup"><span data-stu-id="4873e-105">Sent to determine the relative position of a new item in the sorted list of an owner-drawn combo box or list box.</span></span> <span data-ttu-id="4873e-106">Ogni volta che l'applicazione aggiunge un nuovo elemento, il sistema invia questo messaggio al proprietario di una casella combinata o di una casella di riepilogo creata con lo stile di [**\_ ordinamento**](list-box-styles.md) [**CBS \_ Sort**](combo-box-styles.md) o lbs.</span><span class="sxs-lookup"><span data-stu-id="4873e-106">Whenever the application adds a new item, the system sends this message to the owner of a combo box or list box created with the [**CBS\_SORT**](combo-box-styles.md) or [**LBS\_SORT**](list-box-styles.md) style.</span></span>


```C++
WM_COMPAREITEM

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="4873e-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="4873e-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4873e-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="4873e-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4873e-109">Specifica l'identificatore del controllo che ha inviato il messaggio **WM \_ COMPAREITEM** .</span><span class="sxs-lookup"><span data-stu-id="4873e-109">Specifies the identifier of the control that sent the **WM\_COMPAREITEM** message.</span></span>

</dd> <dt>

<span data-ttu-id="4873e-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4873e-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4873e-111">Puntatore a una struttura [**COMPAREITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-compareitemstruct) contenente gli identificatori e i dati forniti dall'applicazione per due elementi nella casella combinata o casella di riepilogo.</span><span class="sxs-lookup"><span data-stu-id="4873e-111">Pointer to a [**COMPAREITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-compareitemstruct) structure that contains the identifiers and application-supplied data for two items in the combo or list box.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4873e-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4873e-112">Return value</span></span>

<span data-ttu-id="4873e-113">Il valore restituito indica la posizione relativa dei due elementi.</span><span class="sxs-lookup"><span data-stu-id="4873e-113">The return value indicates the relative position of the two items.</span></span> <span data-ttu-id="4873e-114">Potrebbe trattarsi di uno dei valori indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="4873e-114">It may be any of the values shown in the following table.</span></span>



| <span data-ttu-id="4873e-115">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="4873e-115">Return code</span></span>                                                                          | <span data-ttu-id="4873e-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4873e-116">Description</span></span>                                                  |
|--------------------------------------------------------------------------------------|--------------------------------------------------------------|
| <dl> <span data-ttu-id="4873e-117"><dt>**Valore**</dt></span><span class="sxs-lookup"><span data-stu-id="4873e-117"><dt>**Value**</dt></span></span> </dl> | <span data-ttu-id="4873e-118">Significato</span><span class="sxs-lookup"><span data-stu-id="4873e-118">Meaning</span></span><br/>                                           |
| <dl> <span data-ttu-id="4873e-119"><dt>**-1**</dt></span><span class="sxs-lookup"><span data-stu-id="4873e-119"><dt>**-1**</dt></span></span> </dl>    | <span data-ttu-id="4873e-120">L'elemento 1 precede l'elemento 2 nell'ordinamento.</span><span class="sxs-lookup"><span data-stu-id="4873e-120">Item 1 precedes item 2 in the sorted order.</span></span><br/>       |
| <dl> <span data-ttu-id="4873e-121"><dt>**0**</dt></span><span class="sxs-lookup"><span data-stu-id="4873e-121"><dt>**0**</dt></span></span> </dl>     | <span data-ttu-id="4873e-122">Gli elementi 1 e 2 sono equivalenti nell'ordinamento.</span><span class="sxs-lookup"><span data-stu-id="4873e-122">Items 1 and 2 are equivalent in the sorted order.</span></span><br/> |
| <dl> <span data-ttu-id="4873e-123"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="4873e-123"><dt>**1**</dt></span></span> </dl>     | <span data-ttu-id="4873e-124">L'elemento 1 segue l'elemento 2 nell'ordinamento.</span><span class="sxs-lookup"><span data-stu-id="4873e-124">Item 1 follows item 2 in the sorted order.</span></span><br/>        |



 

## <a name="remarks"></a><span data-ttu-id="4873e-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="4873e-125">Remarks</span></span>

<span data-ttu-id="4873e-126">Quando il proprietario di una casella combinata creata dal proprietario o di una casella di riepilogo riceve questo messaggio, il proprietario restituisce un valore che indica quale elemento specificato dalla struttura [**COMPAREITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-compareitemstruct) verrà visualizzato prima dell'altro.</span><span class="sxs-lookup"><span data-stu-id="4873e-126">When the owner of an owner-drawn combo box or list box receives this message, the owner returns a value indicating which of the items specified by the [**COMPAREITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-compareitemstruct) structure will appear before the other.</span></span> <span data-ttu-id="4873e-127">In genere, il sistema invia questo messaggio più volte fino a quando non determina la posizione esatta del nuovo elemento.</span><span class="sxs-lookup"><span data-stu-id="4873e-127">Typically, the system sends this message several times until it determines the exact position for the new item.</span></span>

<span data-ttu-id="4873e-128">Se una routine della finestra di dialogo gestisce questo messaggio, deve eseguire il cast del valore restituito desiderato a un **bool** e restituire direttamente il valore.</span><span class="sxs-lookup"><span data-stu-id="4873e-128">If a dialog box procedure handles this message, it should cast the desired return value to a **BOOL** and return the value directly.</span></span> <span data-ttu-id="4873e-129">Il \_ valore DWL MSGRESULT impostato dalla funzione [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="4873e-129">The DWL\_MSGRESULT value set by the [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) function is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="4873e-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4873e-130">Requirements</span></span>



| <span data-ttu-id="4873e-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="4873e-131">Requirement</span></span> | <span data-ttu-id="4873e-132">Valore</span><span class="sxs-lookup"><span data-stu-id="4873e-132">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4873e-133">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4873e-133">Minimum supported client</span></span><br/> | <span data-ttu-id="4873e-134">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="4873e-134">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="4873e-135">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4873e-135">Minimum supported server</span></span><br/> | <span data-ttu-id="4873e-136">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="4873e-136">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="4873e-137">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4873e-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="4873e-138"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4873e-138"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4873e-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4873e-139">See also</span></span>

<dl> <dt>

<span data-ttu-id="4873e-140">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="4873e-140">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="4873e-141">**COMPAREITEMSTRUCT**</span><span class="sxs-lookup"><span data-stu-id="4873e-141">**COMPAREITEMSTRUCT**</span></span>](/windows/win32/api/winuser/ns-winuser-compareitemstruct)
</dt> <dt>

<span data-ttu-id="4873e-142">**Altre risorse**</span><span class="sxs-lookup"><span data-stu-id="4873e-142">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="4873e-143">**SetWindowLong**</span><span class="sxs-lookup"><span data-stu-id="4873e-143">**SetWindowLong**</span></span>](/windows/desktop/api/winuser/nf-winuser-setwindowlonga)
</dt> </dl>

 


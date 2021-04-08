---
title: Messaggio LVM_SORTITEMS (COMmctrl. h)
description: Usa una funzione di confronto definita dall'applicazione per ordinare gli elementi di un controllo di visualizzazione elenco. L'indice di ogni elemento viene modificato per riflettere la nuova sequenza. È possibile inviare questo messaggio in modo esplicito o usando la \_ macro SortItems di ListView.
ms.assetid: ed3d5cec-69af-49a1-9cb7-eb5da1163071
keywords:
- Controlli di Windows Message LVM_SORTITEMS
topic_type:
- apiref
api_name:
- LVM_SORTITEMS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1aba6e739a15eec5e951d7c3ead04aa36a8201f7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103965017"
---
# <a name="lvm_sortitems-message"></a><span data-ttu-id="3fe29-106">\_Messaggio SORTITEMS LVM</span><span class="sxs-lookup"><span data-stu-id="3fe29-106">LVM\_SORTITEMS message</span></span>

<span data-ttu-id="3fe29-107">Usa una funzione di confronto definita dall'applicazione per ordinare gli elementi di un controllo di visualizzazione elenco.</span><span class="sxs-lookup"><span data-stu-id="3fe29-107">Uses an application-defined comparison function to sort the items of a list-view control.</span></span> <span data-ttu-id="3fe29-108">L'indice di ogni elemento viene modificato per riflettere la nuova sequenza.</span><span class="sxs-lookup"><span data-stu-id="3fe29-108">The index of each item changes to reflect the new sequence.</span></span> <span data-ttu-id="3fe29-109">È possibile inviare questo messaggio in modo esplicito o usando la macro [**\_ SortItems di ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_sortitems) .</span><span class="sxs-lookup"><span data-stu-id="3fe29-109">You can send this message explicitly or by using the [**ListView\_SortItems**](/windows/desktop/api/Commctrl/nf-commctrl-listview_sortitems) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="3fe29-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="3fe29-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3fe29-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="3fe29-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3fe29-112">Valore definito dall'applicazione passato alla funzione di confronto.</span><span class="sxs-lookup"><span data-stu-id="3fe29-112">Application-defined value that is passed to the comparison function.</span></span>

</dd> <dt>

<span data-ttu-id="3fe29-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3fe29-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3fe29-114">Puntatore alla funzione di confronto definita dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="3fe29-114">Pointer to the application-defined comparison function.</span></span> <span data-ttu-id="3fe29-115">La funzione di confronto viene chiamata durante l'operazione di ordinamento ogni volta che è necessario confrontare l'ordine relativo di due elementi dell'elenco.</span><span class="sxs-lookup"><span data-stu-id="3fe29-115">The comparison function is called during the sort operation each time the relative order of two list items needs to be compared.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3fe29-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3fe29-116">Return value</span></span>

<span data-ttu-id="3fe29-117">Restituisce **true** se l'operazione ha esito positivo o **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="3fe29-117">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="3fe29-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="3fe29-118">Remarks</span></span>

<span data-ttu-id="3fe29-119">La funzione di confronto ha il formato seguente:</span><span class="sxs-lookup"><span data-stu-id="3fe29-119">The comparison function has the following form:</span></span>

``` syntax
int CALLBACK CompareFunc(LPARAM lParam1, LPARAM lParam2, LPARAM lParamSort);
```

<span data-ttu-id="3fe29-120">Il parametro *lParam1* è il valore associato al primo elemento da confrontare e il parametro *lParam2* è il valore associato al secondo elemento.</span><span class="sxs-lookup"><span data-stu-id="3fe29-120">The *lParam1* parameter is the value associated with the first item being compared, and the *lParam2* parameter is the value associated with the second item.</span></span> <span data-ttu-id="3fe29-121">Questi sono i valori specificati nel membro **lParam** della struttura [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) degli elementi quando sono stati inseriti nell'elenco.</span><span class="sxs-lookup"><span data-stu-id="3fe29-121">These are the values that were specified in the **lParam** member of the items' [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) structure when they were inserted into the list.</span></span> <span data-ttu-id="3fe29-122">Il parametro *wParam* di [**ListView \_ SortItems**](/windows/desktop/api/Commctrl/nf-commctrl-listview_sortitems)viene passato alla funzione di callback come terzo parametro.</span><span class="sxs-lookup"><span data-stu-id="3fe29-122">The [**ListView\_SortItems**](/windows/desktop/api/Commctrl/nf-commctrl-listview_sortitems)'s *wParam* parameter is passed to the callback function as its third parameter.</span></span>

<span data-ttu-id="3fe29-123">La funzione di confronto deve restituire un valore negativo se il primo elemento deve precedere il secondo, un valore positivo se il primo elemento deve seguire il secondo oppure zero se i due elementi sono equivalenti.</span><span class="sxs-lookup"><span data-stu-id="3fe29-123">The comparison function must return a negative value if the first item should precede the second, a positive value if the first item should follow the second, or zero if the two items are equivalent.</span></span>

> [!Note]  
> <span data-ttu-id="3fe29-124">Durante il processo di ordinamento, il contenuto della visualizzazione elenco è instabile.</span><span class="sxs-lookup"><span data-stu-id="3fe29-124">During the sorting process, the list-view contents are unstable.</span></span> <span data-ttu-id="3fe29-125">Se la funzione di callback invia messaggi al controllo visualizzazione elenco oltre a [**LVM \_ GetItem**](lvm-getitem.md) ([**ListView \_ GetItem**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitem)), i risultati sono imprevedibili.</span><span class="sxs-lookup"><span data-stu-id="3fe29-125">If the callback function sends any messages to the list-view control aside from [**LVM\_GETITEM**](lvm-getitem.md) ([**ListView\_GetItem**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitem)), the results are unpredictable.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="3fe29-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3fe29-126">Requirements</span></span>



| <span data-ttu-id="3fe29-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="3fe29-127">Requirement</span></span> | <span data-ttu-id="3fe29-128">Valore</span><span class="sxs-lookup"><span data-stu-id="3fe29-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3fe29-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3fe29-129">Minimum supported client</span></span><br/> | <span data-ttu-id="3fe29-130">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3fe29-130">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="3fe29-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3fe29-131">Minimum supported server</span></span><br/> | <span data-ttu-id="3fe29-132">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="3fe29-132">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="3fe29-133">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3fe29-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="3fe29-134"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="3fe29-134"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






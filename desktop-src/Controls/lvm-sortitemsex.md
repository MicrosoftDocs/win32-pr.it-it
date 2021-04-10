---
title: Messaggio LVM_SORTITEMSEX (COMmctrl. h)
description: Usa una funzione di confronto definita dall'applicazione per ordinare gli elementi di un controllo di visualizzazione elenco. L'indice di ogni elemento viene modificato per riflettere la nuova sequenza. È possibile inviare questo messaggio in modo esplicito o usando la \_ macro SortItemsEx di ListView.
ms.assetid: eab2f6f5-68fd-4cb6-acf4-cb267ee40fdc
keywords:
- Controlli di Windows Message LVM_SORTITEMSEX
topic_type:
- apiref
api_name:
- LVM_SORTITEMSEX
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 99e524b00cb5ff1260eb68e7d86e185e5ae60c75
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104047931"
---
# <a name="lvm_sortitemsex-message"></a><span data-ttu-id="514ac-106">\_Messaggio SORTITEMSEX LVM</span><span class="sxs-lookup"><span data-stu-id="514ac-106">LVM\_SORTITEMSEX message</span></span>

<span data-ttu-id="514ac-107">Usa una funzione di confronto definita dall'applicazione per ordinare gli elementi di un controllo di visualizzazione elenco.</span><span class="sxs-lookup"><span data-stu-id="514ac-107">Uses an application-defined comparison function to sort the items of a list-view control.</span></span> <span data-ttu-id="514ac-108">L'indice di ogni elemento viene modificato per riflettere la nuova sequenza.</span><span class="sxs-lookup"><span data-stu-id="514ac-108">The index of each item changes to reflect the new sequence.</span></span> <span data-ttu-id="514ac-109">È possibile inviare questo messaggio in modo esplicito o usando la macro [**\_ SortItemsEx di ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_sortitemsex) .</span><span class="sxs-lookup"><span data-stu-id="514ac-109">You can send this message explicitly or by using the [**ListView\_SortItemsEx**](/windows/desktop/api/Commctrl/nf-commctrl-listview_sortitemsex) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="514ac-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="514ac-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="514ac-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="514ac-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="514ac-112">Valore definito dall'applicazione passato alla funzione di confronto.</span><span class="sxs-lookup"><span data-stu-id="514ac-112">Application-defined value that is passed to the comparison function.</span></span>

</dd> <dt>

<span data-ttu-id="514ac-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="514ac-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="514ac-114">Puntatore a una funzione di confronto definita dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="514ac-114">Pointer to an application-defined comparison function.</span></span> <span data-ttu-id="514ac-115">Viene chiamato durante l'operazione di ordinamento ogni volta che è necessario confrontare l'ordine relativo di due elementi dell'elenco.</span><span class="sxs-lookup"><span data-stu-id="514ac-115">It is called during the sort operation each time the relative order of two list items needs to be compared.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="514ac-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="514ac-116">Return value</span></span>

<span data-ttu-id="514ac-117">Restituisce **true** se l'operazione ha esito positivo o **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="514ac-117">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="514ac-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="514ac-118">Remarks</span></span>

<span data-ttu-id="514ac-119">La funzione di confronto ha il formato seguente:</span><span class="sxs-lookup"><span data-stu-id="514ac-119">The comparison function has the following form:</span></span>

``` syntax
int CALLBACK CompareFunc(LPARAM lParam1, LPARAM lParam2, LPARAM lParamSort);  
```

<span data-ttu-id="514ac-120">Questo messaggio è simile a [**LVM \_ SORTITEMS**](lvm-sortitems.md), eccetto il tipo di informazioni passate alla funzione di confronto.</span><span class="sxs-lookup"><span data-stu-id="514ac-120">This message is similar to [**LVM\_SORTITEMS**](lvm-sortitems.md), except for the type of information passed to the comparison function.</span></span> <span data-ttu-id="514ac-121">Con **LVM \_ SORTITEMSEX**, *lParam1* è l'indice corrente del primo elemento e *lParam2* è l'indice corrente del secondo elemento.</span><span class="sxs-lookup"><span data-stu-id="514ac-121">With **LVM\_SORTITEMSEX**, *lParam1* is the current index of the first item, and *lParam2* is the current index of the second item.</span></span> <span data-ttu-id="514ac-122">Se necessario, è possibile inviare un messaggio [**LVM \_ GETITEMTEXT**](lvm-getitemtext.md) per recuperare altre informazioni su un elemento.</span><span class="sxs-lookup"><span data-stu-id="514ac-122">You can send an [**LVM\_GETITEMTEXT**](lvm-getitemtext.md) message to retrieve more information on an item, if needed.</span></span>

<span data-ttu-id="514ac-123">La funzione di confronto deve restituire un valore negativo se il primo elemento deve precedere il secondo, un valore positivo se il primo elemento deve seguire il secondo oppure zero se i due elementi sono equivalenti.</span><span class="sxs-lookup"><span data-stu-id="514ac-123">The comparison function must return a negative value if the first item should precede the second, a positive value if the first item should follow the second, or zero if the two items are equivalent.</span></span>

> [!Note]  
> <span data-ttu-id="514ac-124">Durante il processo di ordinamento, il contenuto della visualizzazione elenco è instabile.</span><span class="sxs-lookup"><span data-stu-id="514ac-124">During the sorting process, the list-view contents are unstable.</span></span> <span data-ttu-id="514ac-125">Se la funzione di callback invia messaggi al controllo visualizzazione elenco oltre a [**LVM \_ GetItem**](lvm-getitem.md) ([**ListView \_ GetItem**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitem)), i risultati sono imprevedibili.</span><span class="sxs-lookup"><span data-stu-id="514ac-125">If the callback function sends any messages to the list-view control aside from [**LVM\_GETITEM**](lvm-getitem.md) ([**ListView\_GetItem**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitem)), the results are unpredictable.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="514ac-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="514ac-126">Requirements</span></span>



| <span data-ttu-id="514ac-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="514ac-127">Requirement</span></span> | <span data-ttu-id="514ac-128">Valore</span><span class="sxs-lookup"><span data-stu-id="514ac-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="514ac-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="514ac-129">Minimum supported client</span></span><br/> | <span data-ttu-id="514ac-130">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="514ac-130">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="514ac-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="514ac-131">Minimum supported server</span></span><br/> | <span data-ttu-id="514ac-132">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="514ac-132">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="514ac-133">Intestazione</span><span class="sxs-lookup"><span data-stu-id="514ac-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="514ac-134"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="514ac-134"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






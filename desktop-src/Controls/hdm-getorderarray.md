---
title: Messaggio HDM_GETORDERARRAY (COMmctrl. h)
description: Ottiene l'ordine da sinistra a destra corrente degli elementi in un controllo intestazione. È possibile inviare questo messaggio in modo esplicito o usare la \_ macro GetOrderArray dell'intestazione.
ms.assetid: b287d3c1-ae61-41a4-a884-dc008eb24ad8
keywords:
- Controlli di Windows Message HDM_GETORDERARRAY
topic_type:
- apiref
api_name:
- HDM_GETORDERARRAY
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e334b0023ad3441c20048273e9bc58c1b25622b9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119831"
---
# <a name="hdm_getorderarray-message"></a><span data-ttu-id="021f8-105">\_Messaggio HDM GETORDERARRAY</span><span class="sxs-lookup"><span data-stu-id="021f8-105">HDM\_GETORDERARRAY message</span></span>

<span data-ttu-id="021f8-106">Ottiene l'ordine da sinistra a destra corrente degli elementi in un controllo intestazione.</span><span class="sxs-lookup"><span data-stu-id="021f8-106">Gets the current left-to-right order of items in a header control.</span></span> <span data-ttu-id="021f8-107">È possibile inviare questo messaggio in modo esplicito o usare la macro [**\_ GetOrderArray dell'intestazione**](/windows/desktop/api/Commctrl/nf-commctrl-header_getorderarray) .</span><span class="sxs-lookup"><span data-stu-id="021f8-107">You can send this message explicitly or use the [**Header\_GetOrderArray**](/windows/desktop/api/Commctrl/nf-commctrl-header_getorderarray) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="021f8-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="021f8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="021f8-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="021f8-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="021f8-110">Numero di elementi Integer che *lParam* può mantenere.</span><span class="sxs-lookup"><span data-stu-id="021f8-110">The number of integer elements that *lParam* can hold.</span></span> <span data-ttu-id="021f8-111">Questo valore deve essere uguale al numero di elementi nel controllo (vedere [**HDM \_ GETITEMCOUNT**](hdm-getitemcount.md)).</span><span class="sxs-lookup"><span data-stu-id="021f8-111">This value must be equal to the number of items in the control (see [**HDM\_GETITEMCOUNT**](hdm-getitemcount.md)).</span></span>

</dd> <dt>

<span data-ttu-id="021f8-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="021f8-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="021f8-113">Puntatore a una matrice di numeri interi che ricevono i valori di indice per gli elementi nell'intestazione.</span><span class="sxs-lookup"><span data-stu-id="021f8-113">A pointer to an array of integers that receive the index values for items in the header.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="021f8-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="021f8-114">Return value</span></span>

<span data-ttu-id="021f8-115">Restituisce un valore diverso da zero se ha esito positivo e il buffer in *lParam* riceve il numero di elemento per ogni elemento nel controllo intestazione nell'ordine in cui appaiono da sinistra a destra.</span><span class="sxs-lookup"><span data-stu-id="021f8-115">Returns nonzero if successful, and the buffer at *lParam* receives the item number for each item in the header control in the order in which they appear from left to right.</span></span> <span data-ttu-id="021f8-116">In caso contrario, il messaggio restituisce zero.</span><span class="sxs-lookup"><span data-stu-id="021f8-116">Otherwise, the message returns zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="021f8-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="021f8-117">Remarks</span></span>

<span data-ttu-id="021f8-118">Il numero di elementi in *lParam* è specificato in *wParam* e deve essere uguale al numero di elementi nel controllo.</span><span class="sxs-lookup"><span data-stu-id="021f8-118">The number of elements in *lParam* is specified in *wParam* and must be equal to the number of items in the control.</span></span> <span data-ttu-id="021f8-119">Il frammento di codice seguente, ad esempio, riserva memoria sufficiente per mantenere i valori di indice.</span><span class="sxs-lookup"><span data-stu-id="021f8-119">For example, the following code fragment will reserve enough memory to hold the index values.</span></span>


```
int iItems,

    *lpiArray;



// Get memory for buffer.

(iItems = SendMessage(hwndHD, HDM_GETITEMCOUNT, 0,0))!=-1)

    if(!(lpiArray = calloc(iItems,sizeof(int))))

MessageBox(hwnd, "Out of memory.","Error", MB_OK);
```



## <a name="requirements"></a><span data-ttu-id="021f8-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="021f8-120">Requirements</span></span>



| <span data-ttu-id="021f8-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="021f8-121">Requirement</span></span> | <span data-ttu-id="021f8-122">Valore</span><span class="sxs-lookup"><span data-stu-id="021f8-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="021f8-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="021f8-123">Minimum supported client</span></span><br/> | <span data-ttu-id="021f8-124">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="021f8-124">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="021f8-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="021f8-125">Minimum supported server</span></span><br/> | <span data-ttu-id="021f8-126">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="021f8-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="021f8-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="021f8-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="021f8-128"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="021f8-128"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






---
title: Codice di notifica DL_CANCELDRAG (COMmctrl. h)
description: Segnala che l'utente ha annullato un'operazione di trascinamento facendo clic con il pulsante destro del mouse o premendo il tasto ESC.
ms.assetid: 62c1377f-41b6-449f-a95e-2689dc1913c6
keywords:
- Controlli di Windows per il codice di notifica DL_CANCELDRAG
topic_type:
- apiref
api_name:
- DL_CANCELDRAG
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab10f7c31184c44fabdffd4f611847e550b62cc7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121778"
---
# <a name="dl_canceldrag-notification-code"></a><span data-ttu-id="b12b4-104">\_Codice di notifica CANCELDRAG DL</span><span class="sxs-lookup"><span data-stu-id="b12b4-104">DL\_CANCELDRAG notification code</span></span>

<span data-ttu-id="b12b4-105">Segnala che l'utente ha annullato un'operazione di trascinamento facendo clic con il pulsante destro del mouse o premendo il tasto ESC.</span><span class="sxs-lookup"><span data-stu-id="b12b4-105">Signals that the user has canceled a drag operation by clicking the right mouse button or pressing the ESC key.</span></span> <span data-ttu-id="b12b4-106">Una casella di riepilogo di trascinamento Invia questo codice di notifica alla finestra padre sotto forma di messaggio elenco di trascinamento.</span><span class="sxs-lookup"><span data-stu-id="b12b4-106">A drag list box sends this notification code to its parent window in the form of a drag list message.</span></span> <span data-ttu-id="b12b4-107">Per ulteriori informazioni, vedere [trascinare i messaggi della casella di riepilogo](about-list-boxes.md).</span><span class="sxs-lookup"><span data-stu-id="b12b4-107">For more information, see [Drag List Box Messages](about-list-boxes.md).</span></span>


```C++
DL_CANCELDRAG

    pDragInfo = (LPARAM)(LPDRAGLISTINFO) lParam;
```



## <a name="parameters"></a><span data-ttu-id="b12b4-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="b12b4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b12b4-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b12b4-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b12b4-110">Puntatore a una struttura [**DRAGLISTINFO**](/windows/win32/api/commctrl/ns-commctrl-draglistinfo) che contiene il \_ codice di notifica CANCELDRAG DL, l'handle per la casella di riepilogo di trascinamento e la posizione del cursore.</span><span class="sxs-lookup"><span data-stu-id="b12b4-110">A pointer to a [**DRAGLISTINFO**](/windows/win32/api/commctrl/ns-commctrl-draglistinfo) structure that contains the DL\_CANCELDRAG notification code, the handle to the drag list box, and the cursor position.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b12b4-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b12b4-111">Return value</span></span>

<span data-ttu-id="b12b4-112">Nessun valore restituito.</span><span class="sxs-lookup"><span data-stu-id="b12b4-112">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b12b4-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="b12b4-113">Remarks</span></span>

<span data-ttu-id="b12b4-114">Elaborando il \_ codice di notifica CANCELDRAG di DL, un'applicazione può reimpostare lo stato interno per indicare che il trascinamento non è attivo.</span><span class="sxs-lookup"><span data-stu-id="b12b4-114">By processing the DL\_CANCELDRAG notification code, an application can reset its internal state to indicate that dragging is not in effect.</span></span>

## <a name="requirements"></a><span data-ttu-id="b12b4-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b12b4-115">Requirements</span></span>



| <span data-ttu-id="b12b4-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="b12b4-116">Requirement</span></span> | <span data-ttu-id="b12b4-117">Valore</span><span class="sxs-lookup"><span data-stu-id="b12b4-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b12b4-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b12b4-118">Minimum supported client</span></span><br/> | <span data-ttu-id="b12b4-119">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b12b4-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b12b4-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b12b4-120">Minimum supported server</span></span><br/> | <span data-ttu-id="b12b4-121">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="b12b4-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b12b4-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b12b4-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="b12b4-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="b12b4-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






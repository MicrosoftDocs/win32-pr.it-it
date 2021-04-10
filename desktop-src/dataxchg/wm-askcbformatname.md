---
title: Messaggio WM_ASKCBFORMATNAME (winuser. h)
description: Inviato al proprietario degli Appunti da una finestra del visualizzatore degli Appunti per richiedere il nome di un \_ formato degli Appunti di OWNERDISPLAY CF.
ms.assetid: eee026ec-58db-41b3-9705-30a17eebbd70
keywords:
- Scambio di dati del messaggio WM_ASKCBFORMATNAME
topic_type:
- apiref
api_name:
- WM_ASKCBFORMATNAME
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b14a7f2fc2ff57076d6b694061466fd60e09dce0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119358"
---
# <a name="wm_askcbformatname-message"></a><span data-ttu-id="a310b-104">\_Messaggio ASKCBFORMATNAME WM</span><span class="sxs-lookup"><span data-stu-id="a310b-104">WM\_ASKCBFORMATNAME message</span></span>

<span data-ttu-id="a310b-105">Inviato al proprietario degli Appunti da una finestra del visualizzatore degli Appunti per richiedere il nome di un formato degli Appunti di [**\_ OWNERDISPLAY CF**](standard-clipboard-formats.md) .</span><span class="sxs-lookup"><span data-stu-id="a310b-105">Sent to the clipboard owner by a clipboard viewer window to request the name of a [**CF\_OWNERDISPLAY**](standard-clipboard-formats.md) clipboard format.</span></span>

<span data-ttu-id="a310b-106">Una finestra riceve questo messaggio tramite la funzione [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="a310b-106">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_ASKCBFORMATNAME              0x030C
```



## <a name="parameters"></a><span data-ttu-id="a310b-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="a310b-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a310b-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a310b-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a310b-109">Dimensione, in caratteri, del buffer a cui punta il parametro *lParam* .</span><span class="sxs-lookup"><span data-stu-id="a310b-109">The size, in characters, of the buffer pointed to by the *lParam* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="a310b-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a310b-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a310b-111">Puntatore al buffer che deve ricevere il nome del formato degli Appunti.</span><span class="sxs-lookup"><span data-stu-id="a310b-111">A pointer to the buffer that is to receive the clipboard format name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a310b-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a310b-112">Return value</span></span>

<span data-ttu-id="a310b-113">Se un'applicazione elabora il messaggio, deve restituire zero.</span><span class="sxs-lookup"><span data-stu-id="a310b-113">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="a310b-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="a310b-114">Remarks</span></span>

<span data-ttu-id="a310b-115">In risposta a questo messaggio, il proprietario degli Appunti deve copiare il nome del formato di visualizzazione del proprietario nel buffer specificato, non superando la dimensione del buffer specificata dal parametro *wParam* .</span><span class="sxs-lookup"><span data-stu-id="a310b-115">In response to this message, the clipboard owner should copy the name of the owner-display format to the specified buffer, not exceeding the buffer size specified by the *wParam* parameter.</span></span>

<span data-ttu-id="a310b-116">Una finestra del visualizzatore degli Appunti Invia questo messaggio al proprietario degli Appunti per determinare il nome del formato [**CF \_ OWNERDISPLAY**](standard-clipboard-formats.md) , ad esempio, per inizializzare un menu che elenca i formati disponibili.</span><span class="sxs-lookup"><span data-stu-id="a310b-116">A clipboard viewer window sends this message to the clipboard owner to determine the name of the [**CF\_OWNERDISPLAY**](standard-clipboard-formats.md) format   for example, to initialize a menu listing available formats.</span></span>

## <a name="requirements"></a><span data-ttu-id="a310b-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a310b-117">Requirements</span></span>



| <span data-ttu-id="a310b-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="a310b-118">Requirement</span></span> | <span data-ttu-id="a310b-119">Valore</span><span class="sxs-lookup"><span data-stu-id="a310b-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a310b-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a310b-120">Minimum supported client</span></span><br/> | <span data-ttu-id="a310b-121">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="a310b-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="a310b-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a310b-122">Minimum supported server</span></span><br/> | <span data-ttu-id="a310b-123">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="a310b-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="a310b-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a310b-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="a310b-125"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a310b-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a310b-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a310b-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a310b-127">Cenni preliminari sugli Appunti</span><span class="sxs-lookup"><span data-stu-id="a310b-127">Clipboard Overview</span></span>](clipboard.md)
</dt> </dl>

 


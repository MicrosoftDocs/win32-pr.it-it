---
title: Messaggio WM_COPYDATA (winuser. h)
description: Un'applicazione invia il \_ messaggio WM COPYDATA per passare i dati a un'altra applicazione.
ms.assetid: d937a260-9fd2-4450-a762-20120f589ab1
keywords:
- Scambio di dati del messaggio WM_COPYDATA
topic_type:
- apiref
api_name:
- WM_COPYDATA
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8160c88b11fa109e8bbfaa06f0f6c45c9b7daed0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477177"
---
# <a name="wm_copydata-message"></a><span data-ttu-id="6f925-104">\_Messaggio COPYDATA WM</span><span class="sxs-lookup"><span data-stu-id="6f925-104">WM\_COPYDATA message</span></span>

<span data-ttu-id="6f925-105">Un'applicazione invia il messaggio **WM \_ COPYDATA** per passare i dati a un'altra applicazione.</span><span class="sxs-lookup"><span data-stu-id="6f925-105">An application sends the **WM\_COPYDATA** message to pass data to another application.</span></span>


```C++
#define WM_COPYDATA                     0x004A
```



## <a name="parameters"></a><span data-ttu-id="6f925-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="6f925-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6f925-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6f925-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6f925-108">Handle per la finestra che passa i dati.</span><span class="sxs-lookup"><span data-stu-id="6f925-108">A handle to the window passing the data.</span></span>

</dd> <dt>

<span data-ttu-id="6f925-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6f925-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6f925-110">Puntatore a una struttura [**COPYDATASTRUCT**](/windows/win32/api/winuser/ns-winuser-copydatastruct) che contiene i dati da passare.</span><span class="sxs-lookup"><span data-stu-id="6f925-110">A pointer to a [**COPYDATASTRUCT**](/windows/win32/api/winuser/ns-winuser-copydatastruct) structure that contains the data to be passed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6f925-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6f925-111">Return value</span></span>

<span data-ttu-id="6f925-112">Se l'applicazione ricevente elabora questo messaggio, deve restituire **true**; in caso contrario, deve restituire **false**.</span><span class="sxs-lookup"><span data-stu-id="6f925-112">If the receiving application processes this message, it should return **TRUE**; otherwise, it should return **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="6f925-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="6f925-113">Remarks</span></span>

<span data-ttu-id="6f925-114">I dati passati non devono contenere puntatori o altri riferimenti a oggetti non accessibili all'applicazione che riceve i dati.</span><span class="sxs-lookup"><span data-stu-id="6f925-114">The data being passed must not contain pointers or other references to objects not accessible to the application receiving the data.</span></span>

<span data-ttu-id="6f925-115">Durante l'invio di questo messaggio, i dati a cui si fa riferimento non devono essere modificati da un altro thread del processo di invio.</span><span class="sxs-lookup"><span data-stu-id="6f925-115">While this message is being sent, the referenced data must not be changed by another thread of the sending process.</span></span>

<span data-ttu-id="6f925-116">L'applicazione ricevente deve considerare i dati di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="6f925-116">The receiving application should consider the data read-only.</span></span> <span data-ttu-id="6f925-117">Il parametro *lParam* è valido solo durante l'elaborazione del messaggio.</span><span class="sxs-lookup"><span data-stu-id="6f925-117">The *lParam* parameter is valid only during the processing of the message.</span></span> <span data-ttu-id="6f925-118">L'applicazione ricevente non deve liberare la memoria a cui fa riferimento *lParam*.</span><span class="sxs-lookup"><span data-stu-id="6f925-118">The receiving application should not free the memory referenced by *lParam*.</span></span> <span data-ttu-id="6f925-119">Se l'applicazione ricevente deve accedere ai dati dopo la restituzione di [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) , deve copiare i dati in un buffer locale.</span><span class="sxs-lookup"><span data-stu-id="6f925-119">If the receiving application must access the data after [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) returns, it must copy the data into a local buffer.</span></span>

## <a name="examples"></a><span data-ttu-id="6f925-120">Esempio</span><span class="sxs-lookup"><span data-stu-id="6f925-120">Examples</span></span>

<span data-ttu-id="6f925-121">Per un esempio, vedere [uso della copia dei dati](using-data-copy.md).</span><span class="sxs-lookup"><span data-stu-id="6f925-121">For an example, see [Using Data Copy](using-data-copy.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6f925-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6f925-122">Requirements</span></span>



| <span data-ttu-id="6f925-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="6f925-123">Requirement</span></span> | <span data-ttu-id="6f925-124">Valore</span><span class="sxs-lookup"><span data-stu-id="6f925-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6f925-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6f925-125">Minimum supported client</span></span><br/> | <span data-ttu-id="6f925-126">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="6f925-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="6f925-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6f925-127">Minimum supported server</span></span><br/> | <span data-ttu-id="6f925-128">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="6f925-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="6f925-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6f925-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="6f925-130"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6f925-130"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6f925-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6f925-131">See also</span></span>

<dl> <dt>

<span data-ttu-id="6f925-132">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="6f925-132">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="6f925-133">**SendMessage**</span><span class="sxs-lookup"><span data-stu-id="6f925-133">**SendMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-sendmessage)
</dt> <dt>

[<span data-ttu-id="6f925-134">**COPYDATASTRUCT**</span><span class="sxs-lookup"><span data-stu-id="6f925-134">**COPYDATASTRUCT**</span></span>](/windows/win32/api/winuser/ns-winuser-copydatastruct)
</dt> </dl>

 


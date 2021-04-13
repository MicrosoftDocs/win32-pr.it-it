---
title: Messaggio WM_RENDERFORMAT (winuser. h)
description: Inviato al proprietario degli Appunti se è stato posticipato il rendering di un formato degli Appunti specifico e se un'applicazione ha richiesto dati in tale formato.
ms.assetid: 81638109-4c5e-4b4c-b2db-4208b6ee83cc
keywords:
- Scambio di dati del messaggio WM_RENDERFORMAT
topic_type:
- apiref
api_name:
- WM_RENDERFORMAT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab9d0e8539dc666c7a791a24c9ba7ac772c3c2c0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340712"
---
# <a name="wm_renderformat-message"></a><span data-ttu-id="e1427-104">\_Messaggio RENDERFORMAT WM</span><span class="sxs-lookup"><span data-stu-id="e1427-104">WM\_RENDERFORMAT message</span></span>

<span data-ttu-id="e1427-105">Inviato al proprietario degli Appunti se è stato posticipato il rendering di un formato degli Appunti specifico e se un'applicazione ha richiesto dati in tale formato.</span><span class="sxs-lookup"><span data-stu-id="e1427-105">Sent to the clipboard owner if it has delayed rendering a specific clipboard format and if an application has requested data in that format.</span></span> <span data-ttu-id="e1427-106">Il proprietario degli Appunti deve eseguire il rendering dei dati nel formato specificato e posizionarli negli Appunti chiamando la funzione [**SetClipboardData**](/windows/win32/api/winuser/nf-winuser-setclipboarddata) .</span><span class="sxs-lookup"><span data-stu-id="e1427-106">The clipboard owner must render data in the specified format and place it on the clipboard by calling the [**SetClipboardData**](/windows/win32/api/winuser/nf-winuser-setclipboarddata) function.</span></span>


```C++
#define WM_RENDERFORMAT                 0x0305
```



## <a name="parameters"></a><span data-ttu-id="e1427-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="e1427-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e1427-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e1427-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e1427-109">[Formato degli Appunti](standard-clipboard-formats.md) di cui eseguire il rendering.</span><span class="sxs-lookup"><span data-stu-id="e1427-109">The [clipboard format](standard-clipboard-formats.md) to be rendered.</span></span>

</dd> <dt>

<span data-ttu-id="e1427-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e1427-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e1427-111">Questo parametro non viene usato.</span><span class="sxs-lookup"><span data-stu-id="e1427-111">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e1427-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e1427-112">Return value</span></span>

<span data-ttu-id="e1427-113">Se un'applicazione elabora il messaggio, deve restituire zero.</span><span class="sxs-lookup"><span data-stu-id="e1427-113">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="e1427-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="e1427-114">Remarks</span></span>

<span data-ttu-id="e1427-115">Quando si risponde a un messaggio **WM \_ RENDERFORMAT** , il proprietario degli Appunti non deve aprire gli Appunti prima di chiamare [**SetClipboardData**](/windows/win32/api/winuser/nf-winuser-setclipboarddata).</span><span class="sxs-lookup"><span data-stu-id="e1427-115">When responding to a **WM\_RENDERFORMAT** message, the clipboard owner must not open the clipboard before calling [**SetClipboardData**](/windows/win32/api/winuser/nf-winuser-setclipboarddata).</span></span> <span data-ttu-id="e1427-116">Non è necessario aprire gli Appunti prima di inserire i dati in risposta a **WM \_ RENDERFORMAT** e qualsiasi tentativo di aprire gli appunti avrà esito negativo perché gli Appunti sono attualmente mantenuti aperti dall'applicazione che ha richiesto il rendering del formato.</span><span class="sxs-lookup"><span data-stu-id="e1427-116">Opening the clipboard is not necessary before placing data in response to **WM\_RENDERFORMAT**, and any attempt to open the clipboard will fail because the clipboard is currently being held open by the application that requested the format to be rendered.</span></span>

## <a name="requirements"></a><span data-ttu-id="e1427-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e1427-117">Requirements</span></span>



| <span data-ttu-id="e1427-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="e1427-118">Requirement</span></span> | <span data-ttu-id="e1427-119">Valore</span><span class="sxs-lookup"><span data-stu-id="e1427-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e1427-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e1427-120">Minimum supported client</span></span><br/> | <span data-ttu-id="e1427-121">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="e1427-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="e1427-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e1427-122">Minimum supported server</span></span><br/> | <span data-ttu-id="e1427-123">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="e1427-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="e1427-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e1427-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="e1427-125"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e1427-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e1427-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e1427-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="e1427-127">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="e1427-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="e1427-128">**SetClipboardData**</span><span class="sxs-lookup"><span data-stu-id="e1427-128">**SetClipboardData**</span></span>](/windows/win32/api/winuser/nf-winuser-setclipboarddata)
</dt> <dt>

[<span data-ttu-id="e1427-129">**\_RENDERALLFORMATS WM**</span><span class="sxs-lookup"><span data-stu-id="e1427-129">**WM\_RENDERALLFORMATS**</span></span>](wm-renderallformats.md)
</dt> <dt>

<span data-ttu-id="e1427-130">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="e1427-130">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="e1427-131">Appunti</span><span class="sxs-lookup"><span data-stu-id="e1427-131">Clipboard</span></span>](clipboard.md)
</dt> </dl>

 

 






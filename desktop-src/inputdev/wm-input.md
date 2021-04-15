---
title: Messaggio WM_INPUT (winuser. h)
description: Inviato alla finestra che sta ricevendo l'input non elaborato. Una finestra riceve questo messaggio tramite la funzione WindowProc.
ms.assetid: a014d68c-841c-4120-b752-4b3fac60e12d
keywords:
- Input della tastiera e del mouse WM_INPUT messaggio
topic_type:
- apiref
api_name:
- WM_INPUT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 04/17/2020
ms.openlocfilehash: ffe64a5ca79bbe886ddae31661c06dae695259a7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400505"
---
# <a name="wm_input-message"></a><span data-ttu-id="b4499-105">\_Messaggio di input WM</span><span class="sxs-lookup"><span data-stu-id="b4499-105">WM\_INPUT message</span></span>

<span data-ttu-id="b4499-106">Inviato alla finestra che sta ricevendo l'input non elaborato.</span><span class="sxs-lookup"><span data-stu-id="b4499-106">Sent to the window that is getting raw input.</span></span>

<span data-ttu-id="b4499-107">Una finestra riceve questo messaggio tramite la funzione [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="b4499-107">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```cpp
#define WM_INPUT 0x00FF
```

## <a name="parameters"></a><span data-ttu-id="b4499-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="b4499-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b4499-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b4499-109">*wParam*</span></span>

</dt> <dd>

<span data-ttu-id="b4499-110">Codice di input.</span><span class="sxs-lookup"><span data-stu-id="b4499-110">The input code.</span></span> <span data-ttu-id="b4499-111">Per ottenere il valore, usare [**get \_ rawinput \_ Code \_ wParam**](/windows/win32/api/winuser/nf-winuser-get_rawinput_code_wparam) macro.</span><span class="sxs-lookup"><span data-stu-id="b4499-111">Use [**GET\_RAWINPUT\_CODE\_WPARAM**](/windows/win32/api/winuser/nf-winuser-get_rawinput_code_wparam) macro to get the value.</span></span>

<span data-ttu-id="b4499-112">I possibili valori sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="b4499-112">Can be one of the following values:</span></span>

| <span data-ttu-id="b4499-113">Valore</span><span class="sxs-lookup"><span data-stu-id="b4499-113">Value</span></span> | <span data-ttu-id="b4499-114">Significato</span><span class="sxs-lookup"><span data-stu-id="b4499-114">Meaning</span></span> |
|---|---|
| <span id="RIM_INPUT"></span><span id="rim_input"></span><dl> <span data-ttu-id="b4499-115"><dt>**Cerchio \_ INPUT**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="b4499-115"><dt>**RIM\_INPUT**</dt> <dt>0</dt></span></span> </dl> | <span data-ttu-id="b4499-116">L'input si è verificato mentre l'applicazione era in primo piano.</span><span class="sxs-lookup"><span data-stu-id="b4499-116">Input occurred while the application was in the foreground.</span></span> </br> <span data-ttu-id="b4499-117">L'applicazione deve chiamare [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) in modo che il sistema possa eseguire la pulizia.</span><span class="sxs-lookup"><span data-stu-id="b4499-117">The application must call [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) so the system can perform cleanup.</span></span> |
| <span id="RIM_INPUTSINK"></span><span id="rim_inputsink"></span><dl> <span data-ttu-id="b4499-118"><dt>**Cerchio \_ INPUTSINK**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="b4499-118"><dt>**RIM\_INPUTSINK**</dt> <dt>1</dt></span></span> </dl> | <span data-ttu-id="b4499-119">Si è verificato un input mentre l'applicazione non è in primo piano.</span><span class="sxs-lookup"><span data-stu-id="b4499-119">Input occurred while the application was not in the foreground.</span></span> |

</dd> <dt>

<span data-ttu-id="b4499-120">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b4499-120">*lParam*</span></span> 

</dt> <dd>

<span data-ttu-id="b4499-121">Handle **HRAWINPUT** per la struttura [**rawinput**](/windows/win32/api/winuser/ns-winuser-rawinput) che contiene l'input non elaborato dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b4499-121">A **HRAWINPUT** handle to the [**RAWINPUT**](/windows/win32/api/winuser/ns-winuser-rawinput) structure that contains the raw input from the device.</span></span> <span data-ttu-id="b4499-122">Per ottenere i dati non elaborati, usare questo handle nella chiamata a [**GetRawInputData**](/windows/win32/api/winuser/nf-winuser-getrawinputdata).</span><span class="sxs-lookup"><span data-stu-id="b4499-122">To get the raw data, use this handle in the call to [**GetRawInputData**](/windows/win32/api/winuser/nf-winuser-getrawinputdata).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b4499-123">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b4499-123">Return value</span></span>

<span data-ttu-id="b4499-124">Se un'applicazione elabora il messaggio, deve restituire zero.</span><span class="sxs-lookup"><span data-stu-id="b4499-124">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="b4499-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="b4499-125">Remarks</span></span>

<span data-ttu-id="b4499-126">L'input non elaborato è disponibile solo quando l'applicazione chiama [**RegisterRawInputDevices**](/windows/win32/api/winuser/nf-winuser-registerrawinputdevices) con specifiche del dispositivo valide.</span><span class="sxs-lookup"><span data-stu-id="b4499-126">Raw input is available only when the application calls [**RegisterRawInputDevices**](/windows/win32/api/winuser/nf-winuser-registerrawinputdevices) with valid device specifications.</span></span>

## <a name="requirements"></a><span data-ttu-id="b4499-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b4499-127">Requirements</span></span>

| <span data-ttu-id="b4499-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="b4499-128">Requirement</span></span> | <span data-ttu-id="b4499-129">Valore</span><span class="sxs-lookup"><span data-stu-id="b4499-129">Value</span></span> |
|--------------------------|-------------------------------------------|
| <span data-ttu-id="b4499-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b4499-130">Minimum supported client</span></span> | <span data-ttu-id="b4499-131">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="b4499-131">Windows XP \[desktop apps only\]</span></span> |
| <span data-ttu-id="b4499-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b4499-132">Minimum supported server</span></span> | <span data-ttu-id="b4499-133">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="b4499-133">Windows Server 2003 \[desktop apps only\]</span></span> |
| <span data-ttu-id="b4499-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b4499-134">Header</span></span> | <dl> <span data-ttu-id="b4499-135"><dt>**Winuser. h (include Windows. h)**</dt></span><span class="sxs-lookup"><span data-stu-id="b4499-135"><dt>**Winuser.h (include Windows.h)** </dt></span></span> </dl> |

## <a name="see-also"></a><span data-ttu-id="b4499-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b4499-136">See also</span></span>

<span data-ttu-id="b4499-137">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="b4499-137">**Reference**</span></span>

[<span data-ttu-id="b4499-138">**GetRawInputData**</span><span class="sxs-lookup"><span data-stu-id="b4499-138">**GetRawInputData**</span></span>](/windows/win32/api/winuser/nf-winuser-getrawinputdata)

[<span data-ttu-id="b4499-139">**RegisterRawInputDevices**</span><span class="sxs-lookup"><span data-stu-id="b4499-139">**RegisterRawInputDevices**</span></span>](/windows/win32/api/winuser/nf-winuser-registerrawinputdevices)

[<span data-ttu-id="b4499-140">**RAWINPUT**</span><span class="sxs-lookup"><span data-stu-id="b4499-140">**RAWINPUT**</span></span>](/windows/win32/api/winuser/ns-winuser-rawinput)

[<span data-ttu-id="b4499-141">**OTTENERE \_ il \_ codice rawinput \_ wParam**</span><span class="sxs-lookup"><span data-stu-id="b4499-141">**GET\_RAWINPUT\_CODE\_WPARAM**</span></span>](/windows/win32/api/winuser/nf-winuser-get_rawinput_code_wparam)

<span data-ttu-id="b4499-142">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="b4499-142">**Conceptual**</span></span>

[<span data-ttu-id="b4499-143">Input non elaborato</span><span class="sxs-lookup"><span data-stu-id="b4499-143">Raw Input</span></span>](raw-input.md)

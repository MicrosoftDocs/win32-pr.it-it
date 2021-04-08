---
title: Messaggio WM_INPUT_DEVICE_CHANGE (winuser. h)
description: Inviato alla finestra registrata per ricevere input non elaborato. Una finestra riceve questo messaggio tramite la funzione WindowProc.
ms.assetid: 2f98d8ea-b47b-4dea-9c38-f9697b18053a
keywords:
- Input della tastiera e del mouse WM_INPUT_DEVICE_CHANGE messaggio
topic_type:
- apiref
api_name:
- WM_INPUT_DEVICE_CHANGE
api_location:
- Winuser.h
api_type:
- HeaderDef
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0edb6dbfbcfa9e024ba85613e3b7671e5f416397
ms.sourcegitcommit: 47d1f3859035a69340571bf50c3d36e0abeb2126
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/10/2020
ms.locfileid: "104047537"
---
# <a name="wm_input_device_change-message"></a><span data-ttu-id="0012e-105">Messaggio WM_INPUT_DEVICE_CHANGE</span><span class="sxs-lookup"><span data-stu-id="0012e-105">WM_INPUT_DEVICE_CHANGE message</span></span>

## <a name="description"></a><span data-ttu-id="0012e-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0012e-106">Description</span></span>

<span data-ttu-id="0012e-107">Inviato alla finestra registrata per ricevere input non elaborato.</span><span class="sxs-lookup"><span data-stu-id="0012e-107">Sent to the window that registered to receive raw input.</span></span> 

<span data-ttu-id="0012e-108">Le notifiche di input non elaborate sono disponibili solo dopo che l'applicazione chiama [RegisterRawInputDevices](/windows/win32/api/winuser/nf-winuser-registerrawinputdevices) con [RIDEV_DEVNOTIFY](/windows/win32/api/winuser/ns-winuser-rawinputdevice) flag.</span><span class="sxs-lookup"><span data-stu-id="0012e-108">Raw input notifications are available only after the application calls [RegisterRawInputDevices](/windows/win32/api/winuser/nf-winuser-registerrawinputdevices) with [RIDEV_DEVNOTIFY](/windows/win32/api/winuser/ns-winuser-rawinputdevice) flag.</span></span>

<span data-ttu-id="0012e-109">Una finestra riceve questo messaggio tramite la funzione [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="0012e-109">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>

```C++
#define WM_INPUT_DEVICE_CHANGE          0x00FE
```

## <a name="parameters"></a><span data-ttu-id="0012e-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="0012e-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0012e-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0012e-111">*wParam*</span></span>

</dt> <dd>

<span data-ttu-id="0012e-112">Tipo: **wParam**</span><span class="sxs-lookup"><span data-stu-id="0012e-112">Type: **WPARAM**</span></span>

<span data-ttu-id="0012e-113">Questo parametro può avere uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="0012e-113">This parameter can be one of the following values.</span></span>

| <span data-ttu-id="0012e-114">Valore</span><span class="sxs-lookup"><span data-stu-id="0012e-114">Value</span></span>                    | <span data-ttu-id="0012e-115">Significato</span><span class="sxs-lookup"><span data-stu-id="0012e-115">Meaning</span></span>                                    |
|--------------------------|--------------------------------------------|
| <span data-ttu-id="0012e-116">**GIDC \_ arrivo**</span><span class="sxs-lookup"><span data-stu-id="0012e-116">**GIDC\_ARRIVAL**</span></span> </br><span data-ttu-id="0012e-117">1</span><span class="sxs-lookup"><span data-stu-id="0012e-117">1</span></span> | <span data-ttu-id="0012e-118">Al sistema è stato aggiunto un nuovo dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0012e-118">A new device has been added to the system.</span></span> </br> <span data-ttu-id="0012e-119">È possibile chiamare [GetRawInputDeviceInfo](/windows/win32/api/winuser/nf-winuser-getrawinputdeviceinfoa) per ottenere altre informazioni sul dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0012e-119">You can call [GetRawInputDeviceInfo](/windows/win32/api/winuser/nf-winuser-getrawinputdeviceinfoa) to get more information regarding the device.</span></span> |
| <span data-ttu-id="0012e-120">**rimozione di GIDC \_**</span><span class="sxs-lookup"><span data-stu-id="0012e-120">**GIDC\_REMOVAL**</span></span> </br><span data-ttu-id="0012e-121">2</span><span class="sxs-lookup"><span data-stu-id="0012e-121">2</span></span> | <span data-ttu-id="0012e-122">Un dispositivo è stato rimosso dal sistema.</span><span class="sxs-lookup"><span data-stu-id="0012e-122">A device has been removed from the system.</span></span> |

</dd> <dt>

<span data-ttu-id="0012e-123">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0012e-123">*lParam*</span></span> 

</dt> <dd>

<span data-ttu-id="0012e-124">Tipo: **lParam**</span><span class="sxs-lookup"><span data-stu-id="0012e-124">Type: **LPARAM**</span></span>

<span data-ttu-id="0012e-125">**Handle** per il dispositivo di input non elaborato.</span><span class="sxs-lookup"><span data-stu-id="0012e-125">The **HANDLE** to the raw input device.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0012e-126">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0012e-126">Return value</span></span>

<span data-ttu-id="0012e-127">Se un'applicazione elabora il messaggio, deve restituire zero.</span><span class="sxs-lookup"><span data-stu-id="0012e-127">If an application processes this message, it should return zero.</span></span>

## <a name="see-also"></a><span data-ttu-id="0012e-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0012e-128">See also</span></span>

<span data-ttu-id="0012e-129">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="0012e-129">**Conceptual**</span></span>

[<span data-ttu-id="0012e-130">Input non elaborato</span><span class="sxs-lookup"><span data-stu-id="0012e-130">Raw Input</span></span>](/windows/desktop/inputdev/raw-input)

<span data-ttu-id="0012e-131">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="0012e-131">**Reference**</span></span>

[<span data-ttu-id="0012e-132">RegisterRawInputDevices</span><span class="sxs-lookup"><span data-stu-id="0012e-132">RegisterRawInputDevices</span></span>](/windows/win32/api/winuser/nf-winuser-registerrawinputdevices)

[<span data-ttu-id="0012e-133">Struttura RAWINPUTDEVICE</span><span class="sxs-lookup"><span data-stu-id="0012e-133">RAWINPUTDEVICE structure</span></span>](/windows/win32/api/winuser/ns-winuser-rawinputdevice)
 


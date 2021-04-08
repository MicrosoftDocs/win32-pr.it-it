---
title: Messaggio di MCIWNDM_NOTIFYMODE (VFW. h)
description: Il \_ messaggio MCIWNDM NOTIFYMODE notifica alla finestra padre di un'applicazione che la modalità operativa del dispositivo MCI è cambiata.
ms.assetid: 08adfa8b-4d88-4953-acd8-8a4728f9e1b6
keywords:
- MCIWNDM_NOTIFYMODE messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- MCIWNDM_NOTIFYMODE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7fe75048a53023dab67bef4048d6149438ad54d2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104047830"
---
# <a name="mciwndm_notifymode-message"></a><span data-ttu-id="d7a66-104">\_Messaggio MCIWNDM NOTIFYMODE</span><span class="sxs-lookup"><span data-stu-id="d7a66-104">MCIWNDM\_NOTIFYMODE message</span></span>

<span data-ttu-id="d7a66-105">Il messaggio **MCIWNDM \_ NOTIFYMODE** notifica alla finestra padre di un'applicazione che la modalità operativa del dispositivo MCI è cambiata.</span><span class="sxs-lookup"><span data-stu-id="d7a66-105">The **MCIWNDM\_NOTIFYMODE** message notifies the parent window of an application that the operating mode of the MCI device has changed.</span></span>


```C++
MCIWNDM_NOTIFYMODE 
wParam = (WPARAM) (HWND) hwnd; 
lParam = (LPARAM) (LONG) mode; 
```



## <a name="parameters"></a><span data-ttu-id="d7a66-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="d7a66-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d7a66-107"><span id="hwnd"></span><span id="HWND"></span>*HWND*</span><span class="sxs-lookup"><span data-stu-id="d7a66-107"><span id="hwnd"></span><span id="HWND"></span>*hwnd*</span></span>
</dt> <dd>

<span data-ttu-id="d7a66-108">Handle per la finestra MCIWnd.</span><span class="sxs-lookup"><span data-stu-id="d7a66-108">Handle to the MCIWnd window.</span></span>

</dd> <dt>

<span data-ttu-id="d7a66-109"><span id="mode"></span><span id="MODE"></span>*modalità*</span><span class="sxs-lookup"><span data-stu-id="d7a66-109"><span id="mode"></span><span id="MODE"></span>*mode*</span></span>
</dt> <dd>

<span data-ttu-id="d7a66-110">Intero corrispondente alla modalità MCI.</span><span class="sxs-lookup"><span data-stu-id="d7a66-110">Integer corresponding to the MCI mode.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d7a66-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="d7a66-111">Remarks</span></span>

<span data-ttu-id="d7a66-112">È possibile abilitare la notifica delle modifiche alla modalità di un dispositivo MCI specificando lo \_ stile della finestra NOTIFYMODE di MCIWNDF.</span><span class="sxs-lookup"><span data-stu-id="d7a66-112">You can enable notification of mode changes of an MCI device by specifying the MCIWNDF\_NOTIFYMODE window style.</span></span>

## <a name="requirements"></a><span data-ttu-id="d7a66-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d7a66-113">Requirements</span></span>



| <span data-ttu-id="d7a66-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="d7a66-114">Requirement</span></span> | <span data-ttu-id="d7a66-115">Valore</span><span class="sxs-lookup"><span data-stu-id="d7a66-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="d7a66-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d7a66-116">Minimum supported client</span></span><br/> | <span data-ttu-id="d7a66-117">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="d7a66-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="d7a66-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d7a66-118">Minimum supported server</span></span><br/> | <span data-ttu-id="d7a66-119">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="d7a66-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="d7a66-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d7a66-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="d7a66-121"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="d7a66-121"><dt>Vfw.h</dt></span></span> </dl> |



 

 






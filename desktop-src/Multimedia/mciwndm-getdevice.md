---
title: Messaggio di MCIWNDM_GETDEVICE (VFW. h)
description: Il \_ messaggio MCIWNDM GetDevice Recupera il nome del dispositivo MCI attualmente aperto. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro MCIWndGetDevice.
ms.assetid: e69a73a6-a927-4536-98c7-ee7d5b16668a
keywords:
- MCIWNDM_GETDEVICE messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- MCIWNDM_GETDEVICE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 32664508a577db9d5a077e3cb4fd00aab34fbdf3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475533"
---
# <a name="mciwndm_getdevice-message"></a><span data-ttu-id="9de30-105">\_Messaggio GETDEVICE MCIWNDM</span><span class="sxs-lookup"><span data-stu-id="9de30-105">MCIWNDM\_GETDEVICE message</span></span>

<span data-ttu-id="9de30-106">Il messaggio **MCIWNDM \_ GetDevice** Recupera il nome del dispositivo MCI attualmente aperto.</span><span class="sxs-lookup"><span data-stu-id="9de30-106">The **MCIWNDM\_GETDEVICE** message retrieves the name of the currently open MCI device.</span></span> <span data-ttu-id="9de30-107">È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**MCIWndGetDevice**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetdevice) .</span><span class="sxs-lookup"><span data-stu-id="9de30-107">You can send this message explicitly or by using the [**MCIWndGetDevice**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetdevice) macro.</span></span>


```C++
MCIWNDM_GETDEVICE 
wParam = (WPARAM) (UINT) len; 
lParam = (LPARAM) (LPVOID) lp; 
```



## <a name="parameters"></a><span data-ttu-id="9de30-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="9de30-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9de30-109"><span id="len"></span><span id="LEN"></span>*Len*</span><span class="sxs-lookup"><span data-stu-id="9de30-109"><span id="len"></span><span id="LEN"></span>*len*</span></span>
</dt> <dd>

<span data-ttu-id="9de30-110">Dimensione, in byte, del buffer.</span><span class="sxs-lookup"><span data-stu-id="9de30-110">Size, in bytes, of the buffer.</span></span>

</dd> <dt>

<span data-ttu-id="9de30-111"><span id="lp"></span><span id="LP"></span>*LP*</span><span class="sxs-lookup"><span data-stu-id="9de30-111"><span id="lp"></span><span id="LP"></span>*lp*</span></span>
</dt> <dd>

<span data-ttu-id="9de30-112">Puntatore a un buffer definito dall'applicazione per restituire il nome del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9de30-112">Pointer to an application-defined buffer to return the device name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9de30-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9de30-113">Return Value</span></span>

<span data-ttu-id="9de30-114">Restituisce zero in caso di esito positivo o un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="9de30-114">Returns zero if successful or a nonzero value otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="9de30-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="9de30-115">Remarks</span></span>

<span data-ttu-id="9de30-116">Se la stringa con terminazione null che contiene il nome del dispositivo è più lunga del buffer, MCIWnd lo tronca.</span><span class="sxs-lookup"><span data-stu-id="9de30-116">If the null-terminated string containing the device name is longer than the buffer, MCIWnd truncates it.</span></span>

## <a name="requirements"></a><span data-ttu-id="9de30-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9de30-117">Requirements</span></span>



| <span data-ttu-id="9de30-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="9de30-118">Requirement</span></span> | <span data-ttu-id="9de30-119">Valore</span><span class="sxs-lookup"><span data-stu-id="9de30-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="9de30-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9de30-120">Minimum supported client</span></span><br/> | <span data-ttu-id="9de30-121">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="9de30-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="9de30-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9de30-122">Minimum supported server</span></span><br/> | <span data-ttu-id="9de30-123">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="9de30-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="9de30-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9de30-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="9de30-125"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="9de30-125"><dt>Vfw.h</dt></span></span> </dl> |



 

 






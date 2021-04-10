---
title: Messaggio di MCIWNDM_NOTIFYSIZE (VFW. h)
description: Il \_ messaggio MCIWNDM NOTIFYSIZE notifica alla finestra padre di un'applicazione che le dimensioni della finestra sono state modificate.
ms.assetid: 76e1f663-bfc6-4d3c-9486-c8c7f79e4265
keywords:
- MCIWNDM_NOTIFYSIZE messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- MCIWNDM_NOTIFYSIZE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 59db02d69302127937a7203729de9cc8b98a58f4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119539"
---
# <a name="mciwndm_notifysize-message"></a><span data-ttu-id="8f2e2-104">\_Messaggio MCIWNDM NOTIFYSIZE</span><span class="sxs-lookup"><span data-stu-id="8f2e2-104">MCIWNDM\_NOTIFYSIZE message</span></span>

<span data-ttu-id="8f2e2-105">Il messaggio **MCIWNDM \_ NOTIFYSIZE** notifica alla finestra padre di un'applicazione che le dimensioni della finestra sono state modificate.</span><span class="sxs-lookup"><span data-stu-id="8f2e2-105">The **MCIWNDM\_NOTIFYSIZE** message notifies the parent window of an application that the window size has changed.</span></span>


```C++
MCIWNDM_NOTIFYSIZE 
wParam = (WPARAM) (HWND) hwnd; 
lParam = 0; 
```



## <a name="parameters"></a><span data-ttu-id="8f2e2-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="8f2e2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8f2e2-107"><span id="hwnd"></span><span id="HWND"></span>*HWND*</span><span class="sxs-lookup"><span data-stu-id="8f2e2-107"><span id="hwnd"></span><span id="HWND"></span>*hwnd*</span></span>
</dt> <dd>

<span data-ttu-id="8f2e2-108">Handle per la finestra MCIWnd.</span><span class="sxs-lookup"><span data-stu-id="8f2e2-108">Handle to the MCIWnd window.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8f2e2-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="8f2e2-109">Remarks</span></span>

<span data-ttu-id="8f2e2-110">È possibile abilitare la notifica delle modifiche apportate alle dimensioni di una finestra MCIWnd specificando lo \_ stile della finestra NOTIFYSIZE MCIWNDF.</span><span class="sxs-lookup"><span data-stu-id="8f2e2-110">You can enable notification of changes in the size of an MCIWnd window by specifying the MCIWNDF\_NOTIFYSIZE window style.</span></span>

## <a name="requirements"></a><span data-ttu-id="8f2e2-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8f2e2-111">Requirements</span></span>



| <span data-ttu-id="8f2e2-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="8f2e2-112">Requirement</span></span> | <span data-ttu-id="8f2e2-113">Valore</span><span class="sxs-lookup"><span data-stu-id="8f2e2-113">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="8f2e2-114">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8f2e2-114">Minimum supported client</span></span><br/> | <span data-ttu-id="8f2e2-115">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="8f2e2-115">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="8f2e2-116">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8f2e2-116">Minimum supported server</span></span><br/> | <span data-ttu-id="8f2e2-117">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="8f2e2-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="8f2e2-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8f2e2-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="8f2e2-119"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="8f2e2-119"><dt>Vfw.h</dt></span></span> </dl> |



 

 






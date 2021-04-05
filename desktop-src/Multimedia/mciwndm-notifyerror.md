---
title: Messaggio di MCIWNDM_NOTIFYERROR (VFW. h)
description: Il \_ messaggio MCIWNDM NOTIFYERROR notifica alla finestra padre di un'applicazione che si è verificato un errore MCI.
ms.assetid: 0f54886a-77dc-43cc-be46-2d322c75471a
keywords:
- MCIWNDM_NOTIFYERROR messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- MCIWNDM_NOTIFYERROR
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bbef9180c31091f3bd1a85f23a08990c2f7e7ea0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048235"
---
# <a name="mciwndm_notifyerror-message"></a><span data-ttu-id="15b51-104">\_Messaggio MCIWNDM NOTIFYERROR</span><span class="sxs-lookup"><span data-stu-id="15b51-104">MCIWNDM\_NOTIFYERROR message</span></span>

<span data-ttu-id="15b51-105">Il messaggio **MCIWNDM \_ NOTIFYERROR** notifica alla finestra padre di un'applicazione che si è verificato un errore MCI.</span><span class="sxs-lookup"><span data-stu-id="15b51-105">The **MCIWNDM\_NOTIFYERROR** message notifies the parent window of an application that an MCI error occurred.</span></span>


```C++
MCIWNDM_NOTIFYERROR 
wParam = (WPARAM) (HWND) hwnd; 
lParam = (LPARAM) (LONG) errorCode; 
```



## <a name="parameters"></a><span data-ttu-id="15b51-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="15b51-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="15b51-107"><span id="hwnd"></span><span id="HWND"></span>*HWND*</span><span class="sxs-lookup"><span data-stu-id="15b51-107"><span id="hwnd"></span><span id="HWND"></span>*hwnd*</span></span>
</dt> <dd>

<span data-ttu-id="15b51-108">Handle per la finestra MCIWnd.</span><span class="sxs-lookup"><span data-stu-id="15b51-108">Handle to the MCIWnd window.</span></span>

</dd> <dt>

<span data-ttu-id="15b51-109"><span id="errorCode"></span><span id="errorcode"></span><span id="ERRORCODE"></span>*errorCode*</span><span class="sxs-lookup"><span data-stu-id="15b51-109"><span id="errorCode"></span><span id="errorcode"></span><span id="ERRORCODE"></span>*errorCode*</span></span>
</dt> <dd>

<span data-ttu-id="15b51-110">Codice numerico per l'errore MCI.</span><span class="sxs-lookup"><span data-stu-id="15b51-110">Numerical code for the MCI error.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="15b51-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="15b51-111">Remarks</span></span>

<span data-ttu-id="15b51-112">È possibile abilitare la notifica di errore MCI specificando lo \_ stile della finestra NOTIFYERROR di MCIWNDF.</span><span class="sxs-lookup"><span data-stu-id="15b51-112">You can enable MCI error notification by specifying the MCIWNDF\_NOTIFYERROR window style.</span></span>

## <a name="requirements"></a><span data-ttu-id="15b51-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="15b51-113">Requirements</span></span>



| <span data-ttu-id="15b51-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="15b51-114">Requirement</span></span> | <span data-ttu-id="15b51-115">Valore</span><span class="sxs-lookup"><span data-stu-id="15b51-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="15b51-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="15b51-116">Minimum supported client</span></span><br/> | <span data-ttu-id="15b51-117">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="15b51-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="15b51-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="15b51-118">Minimum supported server</span></span><br/> | <span data-ttu-id="15b51-119">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="15b51-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="15b51-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="15b51-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="15b51-121"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="15b51-121"><dt>Vfw.h</dt></span></span> </dl> |



 

 






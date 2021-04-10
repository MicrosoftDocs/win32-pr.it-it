---
title: Messaggio di MCIWNDM_NOTIFYPOS (VFW. h)
description: Il \_ messaggio MCIWNDM NOTIFYPOS notifica alla finestra padre di un'applicazione che la posizione della finestra è cambiata.
ms.assetid: ccc8903b-ad79-495a-8003-20e120ad28ff
keywords:
- MCIWNDM_NOTIFYPOS messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- MCIWNDM_NOTIFYPOS
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5bebb3a8facd6478c21888cf0cf5ca81e3735ff8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964722"
---
# <a name="mciwndm_notifypos-message"></a><span data-ttu-id="a3ec7-104">\_Messaggio MCIWNDM NOTIFYPOS</span><span class="sxs-lookup"><span data-stu-id="a3ec7-104">MCIWNDM\_NOTIFYPOS message</span></span>

<span data-ttu-id="a3ec7-105">Il messaggio **MCIWNDM \_ NOTIFYPOS** notifica alla finestra padre di un'applicazione che la posizione della finestra è cambiata.</span><span class="sxs-lookup"><span data-stu-id="a3ec7-105">The **MCIWNDM\_NOTIFYPOS** message notifies the parent window of an application that the window position has changed.</span></span>


```C++
MCIWNDM_NOTIFYPOS 
wParam = (WPARAM) (HWND) hwnd; 
lParam = (LPARAM) (LONG) pos; 
```



## <a name="parameters"></a><span data-ttu-id="a3ec7-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="a3ec7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a3ec7-107"><span id="hwnd"></span><span id="HWND"></span>*HWND*</span><span class="sxs-lookup"><span data-stu-id="a3ec7-107"><span id="hwnd"></span><span id="HWND"></span>*hwnd*</span></span>
</dt> <dd>

<span data-ttu-id="a3ec7-108">Handle per la finestra MCIWnd.</span><span class="sxs-lookup"><span data-stu-id="a3ec7-108">Handle to the MCIWnd window.</span></span>

</dd> <dt>

<span data-ttu-id="a3ec7-109"><span id="pos"></span><span id="POS"></span>*POS*</span><span class="sxs-lookup"><span data-stu-id="a3ec7-109"><span id="pos"></span><span id="POS"></span>*pos*</span></span>
</dt> <dd>

<span data-ttu-id="a3ec7-110">Descrive la nuova posizione.</span><span class="sxs-lookup"><span data-stu-id="a3ec7-110">Describes the new position.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a3ec7-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="a3ec7-111">Remarks</span></span>

<span data-ttu-id="a3ec7-112">È possibile abilitare la notifica delle modifiche nella posizione di una finestra MCIWnd specificando lo \_ stile della finestra NOTIFYPOS MCIWNDF.</span><span class="sxs-lookup"><span data-stu-id="a3ec7-112">You can enable notification of changes in the position of an MCIWnd window by specifying the MCIWNDF\_NOTIFYPOS window style.</span></span>

## <a name="requirements"></a><span data-ttu-id="a3ec7-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a3ec7-113">Requirements</span></span>



| <span data-ttu-id="a3ec7-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="a3ec7-114">Requirement</span></span> | <span data-ttu-id="a3ec7-115">Valore</span><span class="sxs-lookup"><span data-stu-id="a3ec7-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="a3ec7-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a3ec7-116">Minimum supported client</span></span><br/> | <span data-ttu-id="a3ec7-117">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="a3ec7-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="a3ec7-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a3ec7-118">Minimum supported server</span></span><br/> | <span data-ttu-id="a3ec7-119">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="a3ec7-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="a3ec7-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a3ec7-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="a3ec7-121"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="a3ec7-121"><dt>Vfw.h</dt></span></span> </dl> |



 

 






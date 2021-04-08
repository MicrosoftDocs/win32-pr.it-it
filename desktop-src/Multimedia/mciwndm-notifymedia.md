---
title: Messaggio di MCIWNDM_NOTIFYMEDIA (VFW. h)
description: Il \_ messaggio MCIWNDM NOTIFYMEDIA notifica alla finestra padre di un'applicazione che il supporto è stato modificato.
ms.assetid: cc31502d-09a9-4580-9ff8-9c2be51c8e35
keywords:
- MCIWNDM_NOTIFYMEDIA messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- MCIWNDM_NOTIFYMEDIA
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7026bd984e1d79775aac52caad56c87be6e8098e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741151"
---
# <a name="mciwndm_notifymedia-message"></a><span data-ttu-id="ab964-104">\_Messaggio MCIWNDM NOTIFYMEDIA</span><span class="sxs-lookup"><span data-stu-id="ab964-104">MCIWNDM\_NOTIFYMEDIA message</span></span>

<span data-ttu-id="ab964-105">Il messaggio **MCIWNDM \_ NOTIFYMEDIA** notifica alla finestra padre di un'applicazione che il supporto è stato modificato.</span><span class="sxs-lookup"><span data-stu-id="ab964-105">The **MCIWNDM\_NOTIFYMEDIA** message notifies the parent window of an application that the media has changed.</span></span>


```C++
MCIWNDM_NOTIFYMEDIA 
wParam = (WPARAM) (HWND) hwnd; 
lParam = (LPARAM) (LPSTR) lp; 
```



## <a name="parameters"></a><span data-ttu-id="ab964-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="ab964-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ab964-107"><span id="hwnd"></span><span id="HWND"></span>*HWND*</span><span class="sxs-lookup"><span data-stu-id="ab964-107"><span id="hwnd"></span><span id="HWND"></span>*hwnd*</span></span>
</dt> <dd>

<span data-ttu-id="ab964-108">Handle per la finestra MCIWnd.</span><span class="sxs-lookup"><span data-stu-id="ab964-108">Handle to the MCIWnd window.</span></span>

</dd> <dt>

<span data-ttu-id="ab964-109"><span id="lp"></span><span id="LP"></span>*LP*</span><span class="sxs-lookup"><span data-stu-id="ab964-109"><span id="lp"></span><span id="LP"></span>*lp*</span></span>
</dt> <dd>

<span data-ttu-id="ab964-110">Puntatore a una stringa con terminazione null che contiene il nuovo nome file.</span><span class="sxs-lookup"><span data-stu-id="ab964-110">Pointer to a null-terminated string containing the new filename.</span></span> <span data-ttu-id="ab964-111">Se il supporto è in chiusura, specifica una stringa null.</span><span class="sxs-lookup"><span data-stu-id="ab964-111">If the media is closing, it specifies a null string.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ab964-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="ab964-112">Remarks</span></span>

<span data-ttu-id="ab964-113">È possibile abilitare la notifica delle modifiche dei supporti specificando lo \_ stile della finestra NOTIFYMEDIA di MCIWNDF.</span><span class="sxs-lookup"><span data-stu-id="ab964-113">You can enable notification of media changes by specifying the MCIWNDF\_NOTIFYMEDIA window style.</span></span>

## <a name="requirements"></a><span data-ttu-id="ab964-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ab964-114">Requirements</span></span>



| <span data-ttu-id="ab964-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="ab964-115">Requirement</span></span> | <span data-ttu-id="ab964-116">Valore</span><span class="sxs-lookup"><span data-stu-id="ab964-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="ab964-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ab964-117">Minimum supported client</span></span><br/> | <span data-ttu-id="ab964-118">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="ab964-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="ab964-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ab964-119">Minimum supported server</span></span><br/> | <span data-ttu-id="ab964-120">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="ab964-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="ab964-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ab964-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="ab964-122"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="ab964-122"><dt>Vfw.h</dt></span></span> </dl> |



 

 






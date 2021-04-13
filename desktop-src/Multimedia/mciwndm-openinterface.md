---
title: Messaggio di MCIWNDM_OPENINTERFACE (VFW. h)
description: Il \_ messaggio MCIWNDM OPENINTERFACE associa il flusso di dati o il file associato all'interfaccia specificata a una finestra di MCIWnd. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro MCIWndOpenInterface.
ms.assetid: 73cbd637-d315-4b39-a978-2b72aed1f303
keywords:
- MCIWNDM_OPENINTERFACE messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- MCIWNDM_OPENINTERFACE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c40453f4d587429508a5aae19bc432fc46088ae
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400219"
---
# <a name="mciwndm_openinterface-message"></a><span data-ttu-id="665fd-105">\_Messaggio MCIWNDM OPENINTERFACE</span><span class="sxs-lookup"><span data-stu-id="665fd-105">MCIWNDM\_OPENINTERFACE message</span></span>

<span data-ttu-id="665fd-106">Il messaggio **MCIWNDM \_ OPENINTERFACE** associa il flusso di dati o il file associato all'interfaccia specificata a una finestra di MCIWnd.</span><span class="sxs-lookup"><span data-stu-id="665fd-106">The **MCIWNDM\_OPENINTERFACE** message attaches the data stream or file associated with the specified interface to an MCIWnd window.</span></span> <span data-ttu-id="665fd-107">È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**MCIWndOpenInterface**](/windows/desktop/api/Vfw/nf-vfw-mciwndopeninterface) .</span><span class="sxs-lookup"><span data-stu-id="665fd-107">You can send this message explicitly or by using the [**MCIWndOpenInterface**](/windows/desktop/api/Vfw/nf-vfw-mciwndopeninterface) macro.</span></span>


```C++
MCIWNDM_OPENINTERFACE 
wParam = 0; 
lParam = (LPARAM) (LPUNKNOWN) pUnk; 
```



## <a name="parameters"></a><span data-ttu-id="665fd-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="665fd-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="665fd-109"><span id="pUnk"></span><span id="punk"></span><span id="PUNK"></span>*pUnk*</span><span class="sxs-lookup"><span data-stu-id="665fd-109"><span id="pUnk"></span><span id="punk"></span><span id="PUNK"></span>*pUnk*</span></span>
</dt> <dd>

<span data-ttu-id="665fd-110">Puntatore a un'interfaccia IAVI che punta a un file o a un flusso di dati in un file.</span><span class="sxs-lookup"><span data-stu-id="665fd-110">Pointer to an IAVI interface that points to a file or a data stream in a file.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="665fd-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="665fd-111">Return Value</span></span>

<span data-ttu-id="665fd-112">Restituisce zero in caso di esito positivo o un errore.</span><span class="sxs-lookup"><span data-stu-id="665fd-112">Returns zero if successful or an error otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="665fd-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="665fd-113">Requirements</span></span>



| <span data-ttu-id="665fd-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="665fd-114">Requirement</span></span> | <span data-ttu-id="665fd-115">Valore</span><span class="sxs-lookup"><span data-stu-id="665fd-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="665fd-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="665fd-116">Minimum supported client</span></span><br/> | <span data-ttu-id="665fd-117">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="665fd-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="665fd-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="665fd-118">Minimum supported server</span></span><br/> | <span data-ttu-id="665fd-119">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="665fd-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="665fd-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="665fd-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="665fd-121"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="665fd-121"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="665fd-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="665fd-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="665fd-123">**MCIWndOpenInterface**</span><span class="sxs-lookup"><span data-stu-id="665fd-123">**MCIWndOpenInterface**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndopeninterface)
</dt> </dl>

 

 






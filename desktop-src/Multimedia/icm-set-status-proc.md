---
title: Messaggio di ICM_SET_STATUS_PROC (VFW. h)
description: Il \_ messaggio ICM set \_ status \_ proc fornisce una funzione di callback di stato con lo stato di un'operazione di lunga durata.
ms.assetid: a1bcd840-b94b-487e-91d6-67411a8a3a2d
keywords:
- ICM_SET_STATUS_PROC messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- ICM_SET_STATUS_PROC
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 53d7ad2745ab53c2e04a1588ddbf1b1e5d755202
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104479390"
---
# <a name="icm_set_status_proc-message"></a><span data-ttu-id="dbfbd-104">Messaggio di procedura di \_ impostazione \_ stato ICM \_</span><span class="sxs-lookup"><span data-stu-id="dbfbd-104">ICM\_SET\_STATUS\_PROC message</span></span>

<span data-ttu-id="dbfbd-105">Il messaggio **ICM \_ set \_ status \_ proc** fornisce una funzione di callback di stato con lo stato di un'operazione di lunga durata.</span><span class="sxs-lookup"><span data-stu-id="dbfbd-105">The **ICM\_SET\_STATUS\_PROC** message provides a status callback function with the status of a lengthy operation.</span></span>


```C++
ICM_SET_STATUS_PROC 
wParam = (DWORD_PTR)icsetstatusProc; 
lParam = sizeof(ICSETSTATUSPROC); 
```



## <a name="parameters"></a><span data-ttu-id="dbfbd-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="dbfbd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dbfbd-107"><span id="icsetstatusProc"></span><span id="icsetstatusproc"></span><span id="ICSETSTATUSPROC"></span>*icsetstatusProc*</span><span class="sxs-lookup"><span data-stu-id="dbfbd-107"><span id="icsetstatusProc"></span><span id="icsetstatusproc"></span><span id="ICSETSTATUSPROC"></span>*icsetstatusProc*</span></span>
</dt> <dd>

<span data-ttu-id="dbfbd-108">Puntatore a una struttura [**ICSETSTATUSPROC**](/windows/desktop/api/Vfw/ns-vfw-icsetstatusproc) .</span><span class="sxs-lookup"><span data-stu-id="dbfbd-108">Pointer to an [**ICSETSTATUSPROC**](/windows/desktop/api/Vfw/ns-vfw-icsetstatusproc) structure.</span></span>

</dd> <dt>

<span data-ttu-id="dbfbd-109"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="dbfbd-109"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="dbfbd-110">Dimensioni, in byte, di **ICSETSTATUSPROC**.</span><span class="sxs-lookup"><span data-stu-id="dbfbd-110">Size, in bytes, of **ICSETSTATUSPROC**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dbfbd-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="dbfbd-111">Return Value</span></span>

<span data-ttu-id="dbfbd-112">Restituisce ICERR \_ OK se ha esito positivo o un errore in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="dbfbd-112">Returns ICERR\_OK if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="dbfbd-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="dbfbd-113">Remarks</span></span>

<span data-ttu-id="dbfbd-114">Il supporto di questo messaggio è facoltativo ma fortemente consigliato se la compressione o la decompressione richiede più di circa un decimo di secondo.</span><span class="sxs-lookup"><span data-stu-id="dbfbd-114">Support of this message is optional but strongly recommended if compression or decompression takes longer than approximately one-tenth of a second.</span></span>

<span data-ttu-id="dbfbd-115">Un'applicazione può inviare questo messaggio periodicamente a una funzione di callback dello stato durante le operazioni di lunga durata.</span><span class="sxs-lookup"><span data-stu-id="dbfbd-115">An application can send this message periodically to a status callback function during lengthy operations.</span></span>

## <a name="requirements"></a><span data-ttu-id="dbfbd-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="dbfbd-116">Requirements</span></span>



| <span data-ttu-id="dbfbd-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="dbfbd-117">Requirement</span></span> | <span data-ttu-id="dbfbd-118">Valore</span><span class="sxs-lookup"><span data-stu-id="dbfbd-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="dbfbd-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="dbfbd-119">Minimum supported client</span></span><br/> | <span data-ttu-id="dbfbd-120">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="dbfbd-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="dbfbd-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="dbfbd-121">Minimum supported server</span></span><br/> | <span data-ttu-id="dbfbd-122">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="dbfbd-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="dbfbd-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="dbfbd-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="dbfbd-124"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="dbfbd-124"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dbfbd-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="dbfbd-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dbfbd-126">Gestione compressione video</span><span class="sxs-lookup"><span data-stu-id="dbfbd-126">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="dbfbd-127">Messaggi di compressione video</span><span class="sxs-lookup"><span data-stu-id="dbfbd-127">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 






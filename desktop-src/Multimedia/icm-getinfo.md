---
title: Messaggio di ICM_GETINFO (VFW. h)
description: Il \_ messaggio ICM GetInfo esegue una query su un driver di compressione video per restituirne una descrizione in una struttura ICINFO.
ms.assetid: 8029f247-9777-4a34-9e84-908482094493
keywords:
- ICM_GETINFO messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- ICM_GETINFO
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 634803b7dd9a3b8900c35fabedcadb99908c2b31
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301759"
---
# <a name="icm_getinfo-message"></a><span data-ttu-id="4bb14-104">\_Messaggio ICM GETinfo</span><span class="sxs-lookup"><span data-stu-id="4bb14-104">ICM\_GETINFO message</span></span>

<span data-ttu-id="4bb14-105">Il messaggio **ICM \_ GetInfo** esegue una query su un driver di compressione video per restituirne una descrizione in una struttura [**ICINFO**](/windows/desktop/api/Vfw/ns-vfw-icinfo) .</span><span class="sxs-lookup"><span data-stu-id="4bb14-105">The **ICM\_GETINFO** message queries a video compression driver to return a description of itself in an [**ICINFO**](/windows/desktop/api/Vfw/ns-vfw-icinfo) structure.</span></span>


```C++
ICM_GETINFO 
wParam = (DWORD) (LPVOID) lpicinfo; 
lParam = sizeof(ICINFO); 
```



## <a name="parameters"></a><span data-ttu-id="4bb14-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="4bb14-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4bb14-107"><span id="lpicinfo"></span><span id="LPICINFO"></span>*lpicinfo*</span><span class="sxs-lookup"><span data-stu-id="4bb14-107"><span id="lpicinfo"></span><span id="LPICINFO"></span>*lpicinfo*</span></span>
</dt> <dd>

<span data-ttu-id="4bb14-108">Puntatore a una struttura **ICINFO** per contenere informazioni.</span><span class="sxs-lookup"><span data-stu-id="4bb14-108">Pointer to an **ICINFO** structure to contain information.</span></span>

</dd> <dt>

<span data-ttu-id="4bb14-109"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="4bb14-109"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="4bb14-110">Dimensioni, in byte, di **ICINFO**.</span><span class="sxs-lookup"><span data-stu-id="4bb14-110">Size, in bytes, of **ICINFO**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4bb14-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4bb14-111">Return Value</span></span>

<span data-ttu-id="4bb14-112">Restituisce la dimensione, in byte, di [**ICINFO**](/windows/desktop/api/Vfw/ns-vfw-icinfo) o zero se si verifica un errore.</span><span class="sxs-lookup"><span data-stu-id="4bb14-112">Returns the size, in bytes, of [**ICINFO**](/windows/desktop/api/Vfw/ns-vfw-icinfo) or zero if an error occurs..</span></span>

## <a name="remarks"></a><span data-ttu-id="4bb14-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="4bb14-113">Remarks</span></span>

<span data-ttu-id="4bb14-114">In genere, le applicazioni inviano questo messaggio per visualizzare un elenco dei commediatori installati.</span><span class="sxs-lookup"><span data-stu-id="4bb14-114">Typically, applications send this message to display a list of the installed compressors.</span></span>

<span data-ttu-id="4bb14-115">Il driver deve riempire tutti i membri della struttura [**ICINFO**](/windows/desktop/api/Vfw/ns-vfw-icinfo) ad eccezione di **szDriver**.</span><span class="sxs-lookup"><span data-stu-id="4bb14-115">The driver should fill all members of the [**ICINFO**](/windows/desktop/api/Vfw/ns-vfw-icinfo) structure except **szDriver**.</span></span>

## <a name="requirements"></a><span data-ttu-id="4bb14-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4bb14-116">Requirements</span></span>



| <span data-ttu-id="4bb14-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="4bb14-117">Requirement</span></span> | <span data-ttu-id="4bb14-118">Valore</span><span class="sxs-lookup"><span data-stu-id="4bb14-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="4bb14-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4bb14-119">Minimum supported client</span></span><br/> | <span data-ttu-id="4bb14-120">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="4bb14-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="4bb14-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4bb14-121">Minimum supported server</span></span><br/> | <span data-ttu-id="4bb14-122">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="4bb14-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="4bb14-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4bb14-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="4bb14-124"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="4bb14-124"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4bb14-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4bb14-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4bb14-126">Gestione compressione video</span><span class="sxs-lookup"><span data-stu-id="4bb14-126">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="4bb14-127">Messaggi di compressione video</span><span class="sxs-lookup"><span data-stu-id="4bb14-127">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 






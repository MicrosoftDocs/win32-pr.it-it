---
title: Messaggio di ICM_COMPRESS_FRAMES_INFO (VFW. h)
description: Il \_ \_ \_ messaggio di informazioni su Comprimi frame MCI notifica a un driver di compressione di impostare i parametri per la compressione in sospeso.
ms.assetid: d2f6f3b7-dff6-4fef-a642-cb77b00119af
keywords:
- ICM_COMPRESS_FRAMES_INFO messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- ICM_COMPRESS_FRAMES_INFO
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cbb6df0eab7706ebfc03a5e3069d4323be26ecdb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478466"
---
# <a name="icm_compress_frames_info-message"></a><span data-ttu-id="e830f-104">\_ \_ Messaggio informazioni sui frame compressi MCI \_</span><span class="sxs-lookup"><span data-stu-id="e830f-104">ICM\_COMPRESS\_FRAMES\_INFO message</span></span>

<span data-ttu-id="e830f-105">Il messaggio di **\_ informazioni su Comprimi \_ frame \_ MCI** notifica a un driver di compressione di impostare i parametri per la compressione in sospeso.</span><span class="sxs-lookup"><span data-stu-id="e830f-105">The **ICM\_COMPRESS\_FRAMES\_INFO** message notifies a compression driver to set the parameters for the pending compression.</span></span>


```C++
ICM_COMPRESS_FRAMES_INFO 
wParam = (DWORD) (LPVOID) &icf; 
lParam = sizeof(ICCOMPRESSFRAMES); 
```



## <a name="parameters"></a><span data-ttu-id="e830f-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="e830f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e830f-107"><span id="icf"></span><span id="ICF"></span>*ICF*</span><span class="sxs-lookup"><span data-stu-id="e830f-107"><span id="icf"></span><span id="ICF"></span>*icf*</span></span>
</dt> <dd>

<span data-ttu-id="e830f-108">Puntatore a una struttura [**ICCOMPRESSFRAMES**](/windows/desktop/api/Vfw/ns-vfw-iccompressframes) .</span><span class="sxs-lookup"><span data-stu-id="e830f-108">Pointer to an [**ICCOMPRESSFRAMES**](/windows/desktop/api/Vfw/ns-vfw-iccompressframes) structure.</span></span> <span data-ttu-id="e830f-109">I membri **GetData** e **PutData** di questa struttura non vengono utilizzati con questo messaggio.</span><span class="sxs-lookup"><span data-stu-id="e830f-109">The **GetData** and **PutData** members of this structure are not used with this message.</span></span>

</dd> <dt>

<span data-ttu-id="e830f-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="e830f-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="e830f-111">Dimensioni, in byte, di [**ICCOMPRESSFRAMES**](/windows/desktop/api/Vfw/ns-vfw-iccompressframes).</span><span class="sxs-lookup"><span data-stu-id="e830f-111">Size, in bytes, of [**ICCOMPRESSFRAMES**](/windows/desktop/api/Vfw/ns-vfw-iccompressframes).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e830f-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e830f-112">Return Value</span></span>

<span data-ttu-id="e830f-113">Restituisce ICERR \_ OK se ha esito positivo o un errore in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="e830f-113">Returns ICERR\_OK if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="e830f-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="e830f-114">Remarks</span></span>

<span data-ttu-id="e830f-115">Un compressore può utilizzare questo messaggio per determinare la quantità di spazio da allocare per ogni fotogramma durante la compressione.</span><span class="sxs-lookup"><span data-stu-id="e830f-115">A compressor can use this message to determine how much space to allocate for each frame while compressing.</span></span>

## <a name="requirements"></a><span data-ttu-id="e830f-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e830f-116">Requirements</span></span>



| <span data-ttu-id="e830f-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="e830f-117">Requirement</span></span> | <span data-ttu-id="e830f-118">Valore</span><span class="sxs-lookup"><span data-stu-id="e830f-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="e830f-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e830f-119">Minimum supported client</span></span><br/> | <span data-ttu-id="e830f-120">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="e830f-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="e830f-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e830f-121">Minimum supported server</span></span><br/> | <span data-ttu-id="e830f-122">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="e830f-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="e830f-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e830f-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="e830f-124"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="e830f-124"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e830f-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e830f-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e830f-126">Gestione compressione video</span><span class="sxs-lookup"><span data-stu-id="e830f-126">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="e830f-127">Messaggi di compressione video</span><span class="sxs-lookup"><span data-stu-id="e830f-127">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 






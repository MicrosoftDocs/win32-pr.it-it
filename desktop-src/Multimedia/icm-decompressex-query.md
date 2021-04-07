---
title: Messaggio di ICM_DECOMPRESSEX_QUERY (VFW. h)
description: Il \_ \_ messaggio di query ICM DECOMPRESSEX esegue una query su un driver di compressione video per determinare se supporta un formato di input specifico o se può decomprimere un formato di input specifico in un formato di output specifico.
ms.assetid: 7778a52d-2ed8-495c-8656-c6beb1863499
keywords:
- ICM_DECOMPRESSEX_QUERY messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- ICM_DECOMPRESSEX_QUERY
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e5b2ef5999b9e0619ccbd9ccabd9bc5223b3bf2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874297"
---
# <a name="icm_decompressex_query-message"></a><span data-ttu-id="d02a9-104">\_Messaggio di \_ query DECOMPRESSEX ICM</span><span class="sxs-lookup"><span data-stu-id="d02a9-104">ICM\_DECOMPRESSEX\_QUERY message</span></span>

<span data-ttu-id="d02a9-105">Il messaggio di **\_ \_ query ICM DECOMPRESSEX** esegue una query su un driver di compressione video per determinare se supporta un formato di input specifico o se può decomprimere un formato di input specifico in un formato di output specifico.</span><span class="sxs-lookup"><span data-stu-id="d02a9-105">The **ICM\_DECOMPRESSEX\_QUERY** message queries a video compression driver to determine if it supports a specific input format or if it can decompress a specific input format to a specific output format.</span></span>


```C++
ICM_DECOMPRESSEX_QUERY 
wParam = (DWORD_PTR) (LPVOID) &icdex; 
lParam = sizeof(ICDECOMPRESSEX); 
```



## <a name="parameters"></a><span data-ttu-id="d02a9-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="d02a9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d02a9-107"><span id="icdex"></span><span id="ICDEX"></span>*icdex*</span><span class="sxs-lookup"><span data-stu-id="d02a9-107"><span id="icdex"></span><span id="ICDEX"></span>*icdex*</span></span>
</dt> <dd>

<span data-ttu-id="d02a9-108">Puntatore a una struttura [**ICDECOMPRESSEX**](/windows/desktop/api/Vfw/ns-vfw-icdecompressex) contenente il formato di input.</span><span class="sxs-lookup"><span data-stu-id="d02a9-108">Pointer to a [**ICDECOMPRESSEX**](/windows/desktop/api/Vfw/ns-vfw-icdecompressex) structure containing the input format.</span></span>

</dd> <dt>

<span data-ttu-id="d02a9-109"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="d02a9-109"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="d02a9-110">Dimensioni, in byte, di [**ICDECOMPRESSEX**](/windows/desktop/api/Vfw/ns-vfw-icdecompressex).</span><span class="sxs-lookup"><span data-stu-id="d02a9-110">Size, in bytes, of [**ICDECOMPRESSEX**](/windows/desktop/api/Vfw/ns-vfw-icdecompressex).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d02a9-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d02a9-111">Return Value</span></span>

<span data-ttu-id="d02a9-112">Restituisce ICERR \_ OK se la decompressione specificata è supportata o ICERR \_ BADFORMAT in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="d02a9-112">Returns ICERR\_OK if the specified decompression is supported or ICERR\_BADFORMAT otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="d02a9-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d02a9-113">Requirements</span></span>



| <span data-ttu-id="d02a9-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="d02a9-114">Requirement</span></span> | <span data-ttu-id="d02a9-115">Valore</span><span class="sxs-lookup"><span data-stu-id="d02a9-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="d02a9-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d02a9-116">Minimum supported client</span></span><br/> | <span data-ttu-id="d02a9-117">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="d02a9-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="d02a9-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d02a9-118">Minimum supported server</span></span><br/> | <span data-ttu-id="d02a9-119">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="d02a9-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="d02a9-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d02a9-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="d02a9-121"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="d02a9-121"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d02a9-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d02a9-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d02a9-123">Gestione compressione video</span><span class="sxs-lookup"><span data-stu-id="d02a9-123">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="d02a9-124">Messaggi di compressione video</span><span class="sxs-lookup"><span data-stu-id="d02a9-124">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 






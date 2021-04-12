---
title: Struttura BG_FILE_RANGE (Deliveryoptimization. h)
description: La struttura BG_FILE_RANGE identifica un intervallo di byte da scaricare da un file.
ms.assetid: 58993C51-E42E-4E44-9E8A-15E982B25413
keywords:
- Struttura BG_FILE_RANGE
topic_type:
- apiref
api_name:
- BG_FILE_RANGE
api_location:
- deliveryoptimization.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cedabfb066a5905adb2ed8eac9996fd77c0e12be
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400841"
---
# <a name="bg_file_range-structure"></a><span data-ttu-id="42205-104">Struttura BG_FILE_RANGE</span><span class="sxs-lookup"><span data-stu-id="42205-104">BG_FILE_RANGE structure</span></span>

<span data-ttu-id="42205-105">La struttura **BG_FILE_RANGE** identifica un intervallo di byte da scaricare da un file.</span><span class="sxs-lookup"><span data-stu-id="42205-105">The **BG_FILE_RANGE** structure identifies a range of bytes to download from a file.</span></span>

## <a name="syntax"></a><span data-ttu-id="42205-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="42205-106">Syntax</span></span>


```C++
typedef struct {
  UINT64 InitialOffset;
  UINT64 Length;
} BG_FILE_RANGE;
```



## <a name="members"></a><span data-ttu-id="42205-107">Members</span><span class="sxs-lookup"><span data-stu-id="42205-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="42205-108">**InitialOffset**</span><span class="sxs-lookup"><span data-stu-id="42205-108">**InitialOffset**</span></span>
</dt> <dd>

<span data-ttu-id="42205-109">Offset in base zero all'inizio dell'intervallo di byte da scaricare da un file.</span><span class="sxs-lookup"><span data-stu-id="42205-109">Zero-based offset to the beginning of the range of bytes to download from a file.</span></span>

</dd> <dt>

<span data-ttu-id="42205-110">**Length**</span><span class="sxs-lookup"><span data-stu-id="42205-110">**Length**</span></span>
</dt> <dd>

<span data-ttu-id="42205-111">Lunghezza dell'intervallo, in byte.</span><span class="sxs-lookup"><span data-stu-id="42205-111">The length of the range, in bytes.</span></span> <span data-ttu-id="42205-112">Non specificare una lunghezza pari a zero byte.</span><span class="sxs-lookup"><span data-stu-id="42205-112">Do not specify a zero byte length.</span></span> <span data-ttu-id="42205-113">Per indicare che l'intervallo si estende fino alla fine del file, specificare **BG_LENGTH_TO_EOF**.</span><span class="sxs-lookup"><span data-stu-id="42205-113">To indicate that the range extends to the end of the file, specify **BG_LENGTH_TO_EOF**.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="42205-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="42205-114">Remarks</span></span>

<span data-ttu-id="42205-115">L'intervallo deve esistere nel file o generare un errore di **DO_E_INVALID_RANGE** .</span><span class="sxs-lookup"><span data-stu-id="42205-115">The range must exist in the file or DO generates an **DO_E_INVALID_RANGE** error.</span></span>

## <a name="requirements"></a><span data-ttu-id="42205-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="42205-116">Requirements</span></span>



| <span data-ttu-id="42205-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="42205-117">Requirement</span></span> | <span data-ttu-id="42205-118">Valore</span><span class="sxs-lookup"><span data-stu-id="42205-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="42205-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="42205-119">Minimum supported client</span></span><br/> | <span data-ttu-id="42205-120">Solo app desktop Windows 10 versione 1709 \[\]</span><span class="sxs-lookup"><span data-stu-id="42205-120">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="42205-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="42205-121">Minimum supported server</span></span><br/> | <span data-ttu-id="42205-122">Windows Server, versione 1709 \[ solo per le app desktop\]</span><span class="sxs-lookup"><span data-stu-id="42205-122">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="42205-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="42205-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="42205-124"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="42205-124"><dt>Deliveryoptimization.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="42205-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="42205-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="42205-126">**IBackgroundCopyFile2::GetFileRanges**</span><span class="sxs-lookup"><span data-stu-id="42205-126">**IBackgroundCopyFile2::GetFileRanges**</span></span>](ibackgroundcopyfile2-getfileranges-method.md)
</dt> </dl>

 

 






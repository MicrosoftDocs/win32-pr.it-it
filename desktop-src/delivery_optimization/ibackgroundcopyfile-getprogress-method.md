---
title: Metodo getProgress IBackgroundCopyFile (Deliveryoptimization. h)
description: Recupera le informazioni sullo stato di avanzamento del trasferimento di file.
ms.assetid: 3D8AFD65-AF34-4000-A4A9-8A187427E85C
keywords:
- Metodo getProgress
- Metodo getProgress, interfaccia IBackgroundCopyFile
- Interfaccia IBackgroundCopyFile, metodo getProgress
topic_type:
- apiref
api_name:
- IBackgroundCopyFile.GetProgress
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f0828105822700f9d34cd180c8877634bc3a6013
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476373"
---
# <a name="ibackgroundcopyfilegetprogress-method"></a><span data-ttu-id="345ef-106">Metodo IBackgroundCopyFile:: getProgress</span><span class="sxs-lookup"><span data-stu-id="345ef-106">IBackgroundCopyFile::GetProgress method</span></span>

<span data-ttu-id="345ef-107">Recupera le informazioni sullo stato di avanzamento del trasferimento di file.</span><span class="sxs-lookup"><span data-stu-id="345ef-107">Retrieves information on the progress of the file transfer.</span></span>

## <a name="syntax"></a><span data-ttu-id="345ef-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="345ef-108">Syntax</span></span>


```C++
HRESULT GetProgress(
  [out] BG_FILE_PROGRESS *pProgress
);
```



## <a name="parameters"></a><span data-ttu-id="345ef-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="345ef-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="345ef-110">*pProgress* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="345ef-110">*pProgress* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="345ef-111">Struttura i cui membri indicano lo stato di avanzamento del trasferimento di file.</span><span class="sxs-lookup"><span data-stu-id="345ef-111">Structure whose members indicate the progress of the file transfer.</span></span> <span data-ttu-id="345ef-112">Per informazioni dettagliate sul tipo di informazioni sullo stato di avanzamento disponibili, vedere la struttura [**BG_FILE_PROGRESS**](bg-file-progress.md) .</span><span class="sxs-lookup"><span data-stu-id="345ef-112">For details on the type of progress information available, see the [**BG_FILE_PROGRESS**](bg-file-progress.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="345ef-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="345ef-113">Return value</span></span>

<span data-ttu-id="345ef-114">Questo metodo restituisce **S_OK** in esito positivo o uno dei valori **HRESULT** com standard in errore.</span><span class="sxs-lookup"><span data-stu-id="345ef-114">This method returns **S_OK** on success or one of the standard COM **HRESULT** values on error.</span></span>

## <a name="requirements"></a><span data-ttu-id="345ef-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="345ef-115">Requirements</span></span>



| <span data-ttu-id="345ef-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="345ef-116">Requirement</span></span> | <span data-ttu-id="345ef-117">Valore</span><span class="sxs-lookup"><span data-stu-id="345ef-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="345ef-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="345ef-118">Minimum supported client</span></span><br/> | <span data-ttu-id="345ef-119">Solo app desktop Windows 10 versione 1709 \[\]</span><span class="sxs-lookup"><span data-stu-id="345ef-119">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="345ef-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="345ef-120">Minimum supported server</span></span><br/> | <span data-ttu-id="345ef-121">Windows Server, versione 1709 \[ solo per le app desktop\]</span><span class="sxs-lookup"><span data-stu-id="345ef-121">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="345ef-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="345ef-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="345ef-123"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="345ef-123"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="345ef-124">IDL</span><span class="sxs-lookup"><span data-stu-id="345ef-124">IDL</span></span><br/>                      | <dl> <span data-ttu-id="345ef-125"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="345ef-125"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="345ef-126">Libreria</span><span class="sxs-lookup"><span data-stu-id="345ef-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="345ef-127"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="345ef-127"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="345ef-128">DLL</span><span class="sxs-lookup"><span data-stu-id="345ef-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="345ef-129"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="345ef-129"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="345ef-130">IID</span><span class="sxs-lookup"><span data-stu-id="345ef-130">IID</span></span><br/>                      | <span data-ttu-id="345ef-131">IID_IBackgroundCopyFile viene definito come 01B7BD23-FB88-4A77-8490-5891D3E4653A</span><span class="sxs-lookup"><span data-stu-id="345ef-131">IID_IBackgroundCopyFile is defined as 01B7BD23-FB88-4A77-8490-5891D3E4653A</span></span><br/>              |



## <a name="see-also"></a><span data-ttu-id="345ef-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="345ef-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="345ef-133">**BG_FILE_PROGRESS**</span><span class="sxs-lookup"><span data-stu-id="345ef-133">**BG_FILE_PROGRESS**</span></span>](bg-file-progress.md)
</dt> <dt>

[<span data-ttu-id="345ef-134">**IBackgroundCopyFile**</span><span class="sxs-lookup"><span data-stu-id="345ef-134">**IBackgroundCopyFile**</span></span>](ibackgroundcopyfile.md)
</dt> <dt>

[<span data-ttu-id="345ef-135">**Metodo ibackgroundcopyjob:: getProgress**</span><span class="sxs-lookup"><span data-stu-id="345ef-135">**IBackgroundCopyJob::GetProgress**</span></span>](ibackgroundcopyjob-getprogress.md)
</dt> </dl>

 

 






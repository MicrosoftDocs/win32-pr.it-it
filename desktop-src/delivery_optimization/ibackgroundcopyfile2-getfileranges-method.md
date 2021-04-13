---
title: Metodo IBackgroundCopyFile2 GetFileRanges (Deliveryoptimization. h)
description: Recupera gli intervalli che si desidera scaricare dal file remoto.
ms.assetid: 19B7B4FC-371F-482B-B997-C240B5483F4D
keywords:
- Metodo GetFileRanges
- Metodo GetFileRanges, interfaccia IBackgroundCopyFile2
- Interfaccia IBackgroundCopyFile2, metodo GetFileRanges
topic_type:
- apiref
api_name:
- IBackgroundCopyFile2.GetFileRanges
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 37352176ca460587343bed0a154ee992c12c2fff
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400551"
---
# <a name="ibackgroundcopyfile2getfileranges-method"></a><span data-ttu-id="ece15-106">Metodo IBackgroundCopyFile2:: GetFileRanges</span><span class="sxs-lookup"><span data-stu-id="ece15-106">IBackgroundCopyFile2::GetFileRanges method</span></span>

<span data-ttu-id="ece15-107">Recupera gli intervalli che si desidera scaricare dal file remoto.</span><span class="sxs-lookup"><span data-stu-id="ece15-107">Retrieves the ranges that you want to download from the remote file.</span></span>

## <a name="syntax"></a><span data-ttu-id="ece15-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ece15-108">Syntax</span></span>


```C++
HRESULT GetFileRanges(
  [in, out] DWORD         *RangeCount,
  [out]     BG_FILE_RANGE **Ranges
);
```



## <a name="parameters"></a><span data-ttu-id="ece15-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="ece15-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ece15-110">*RangeCount* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="ece15-110">*RangeCount* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="ece15-111">Numero di elementi negli *intervalli*.</span><span class="sxs-lookup"><span data-stu-id="ece15-111">Number of elements in *Ranges*.</span></span>

</dd> <dt>

<span data-ttu-id="ece15-112">*Intervalli* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="ece15-112">*Ranges* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ece15-113">Matrice di strutture di [**BG_FILE_RANGE**](bg-file-range.md) che specificano gli intervalli da scaricare.</span><span class="sxs-lookup"><span data-stu-id="ece15-113">Array of [**BG_FILE_RANGE**](bg-file-range.md) structures that specify the ranges to download.</span></span> <span data-ttu-id="ece15-114">Al termine, chiamare la funzione [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) per liberare gli *intervalli*.</span><span class="sxs-lookup"><span data-stu-id="ece15-114">When done, call the [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) function to free *Ranges*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ece15-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ece15-115">Return value</span></span>

<span data-ttu-id="ece15-116">Questo metodo restituisce i valori restituiti seguenti e altri.</span><span class="sxs-lookup"><span data-stu-id="ece15-116">This method returns the following return values, as well as others.</span></span>



| <span data-ttu-id="ece15-117">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="ece15-117">Return code</span></span>                                                                              | <span data-ttu-id="ece15-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ece15-118">Description</span></span>                                                                                                                                   |
|------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="ece15-119"><dt>S_OK \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="ece15-119"><dt>\*\*\*\*S_OK\*\*\*\*</dt></span></span> </dl> | <span data-ttu-id="ece15-120">Operazione riuscita</span><span class="sxs-lookup"><span data-stu-id="ece15-120">Success</span></span><br/>                                                                                                                            |
| <dl> <span data-ttu-id="ece15-121"><dt>**S_FALSE**</dt></span><span class="sxs-lookup"><span data-stu-id="ece15-121"><dt>**S_FALSE**</dt></span></span> </dl>  | <span data-ttu-id="ece15-122">Non è stato specificato alcun intervallo oppure il processo è un processo di caricamento o di caricamento-risposta.</span><span class="sxs-lookup"><span data-stu-id="ece15-122">No ranges were specified or the job is an upload or upload-reply job.</span></span> <span data-ttu-id="ece15-123">*RangeCount* è impostato su zero e l' *intervallo* è impostato su **null**.</span><span class="sxs-lookup"><span data-stu-id="ece15-123">*RangeCount* is set to zero and *Ranges* is set to **NULL**.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="ece15-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ece15-124">Requirements</span></span>



| <span data-ttu-id="ece15-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="ece15-125">Requirement</span></span> | <span data-ttu-id="ece15-126">Valore</span><span class="sxs-lookup"><span data-stu-id="ece15-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ece15-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ece15-127">Minimum supported client</span></span><br/> | <span data-ttu-id="ece15-128">Solo app desktop Windows 10 versione 1709 \[\]</span><span class="sxs-lookup"><span data-stu-id="ece15-128">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="ece15-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ece15-129">Minimum supported server</span></span><br/> | <span data-ttu-id="ece15-130">Windows Server, versione 1709 \[ solo per le app desktop\]</span><span class="sxs-lookup"><span data-stu-id="ece15-130">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="ece15-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ece15-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="ece15-132"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="ece15-132"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="ece15-133">IDL</span><span class="sxs-lookup"><span data-stu-id="ece15-133">IDL</span></span><br/>                      | <dl> <span data-ttu-id="ece15-134"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="ece15-134"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="ece15-135">Libreria</span><span class="sxs-lookup"><span data-stu-id="ece15-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="ece15-136"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ece15-136"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="ece15-137">DLL</span><span class="sxs-lookup"><span data-stu-id="ece15-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ece15-138"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ece15-138"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="ece15-139">IID</span><span class="sxs-lookup"><span data-stu-id="ece15-139">IID</span></span><br/>                      | <span data-ttu-id="ece15-140">IID_IBackgroundCopyFile2 viene definito come 83e81b93-0873-474d-8A8C-f2018b1a939c</span><span class="sxs-lookup"><span data-stu-id="ece15-140">IID_IBackgroundCopyFile2 is defined as 83e81b93-0873-474d-8a8c-f2018b1a939c</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="ece15-141">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ece15-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ece15-142">**BG_FILE_RANGE**</span><span class="sxs-lookup"><span data-stu-id="ece15-142">**BG_FILE_RANGE**</span></span>](bg-file-range.md)
</dt> <dt>

[<span data-ttu-id="ece15-143">**IBackgroundCopyFile2**</span><span class="sxs-lookup"><span data-stu-id="ece15-143">**IBackgroundCopyFile2**</span></span>](ibackgroundcopyfile2.md)
</dt> </dl>

 


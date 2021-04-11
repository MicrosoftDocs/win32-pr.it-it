---
title: Metodo metodo ibackgroundcopyjob EnumFiles (Deliveryoptimization. h)
description: Recupera un puntatore a interfaccia IEnumBackgroundCopyFiles che viene usato per enumerare i file in un processo.
ms.assetid: 94FA5D7B-08C1-497E-9813-571D35AE3BCF
keywords:
- Metodo EnumFiles
- Metodo EnumFiles, interfaccia metodo ibackgroundcopyjob
- Interfaccia metodo ibackgroundcopyjob, metodo EnumFiles
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.EnumFiles
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a4b0315f98594357d67fd5dbfed3bf2561f41f71
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120034"
---
# <a name="ibackgroundcopyjobenumfiles-method"></a><span data-ttu-id="0df82-106">Metodo metodo ibackgroundcopyjob:: EnumFiles</span><span class="sxs-lookup"><span data-stu-id="0df82-106">IBackgroundCopyJob::EnumFiles method</span></span>

<span data-ttu-id="0df82-107">Recupera un puntatore a interfaccia [**IEnumBackgroundCopyFiles**](ienumbackgroundcopyfiles-.md) che viene usato per enumerare i file in un processo.</span><span class="sxs-lookup"><span data-stu-id="0df82-107">Retrieves an [**IEnumBackgroundCopyFiles**](ienumbackgroundcopyfiles-.md) interface pointer that you use to enumerate the files in a job.</span></span>

## <a name="syntax"></a><span data-ttu-id="0df82-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0df82-108">Syntax</span></span>


```C++
HRESULT EnumFiles(
  [out] IEnumBackgroundCopyFiles **ppEnumFiles
);
```



## <a name="parameters"></a><span data-ttu-id="0df82-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="0df82-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0df82-110">*ppEnumFiles* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="0df82-110">*ppEnumFiles* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0df82-111">Puntatore all'interfaccia [**IEnumBackgroundCopyFiles**](ienumbackgroundcopyfiles-.md) usato per enumerare i file nel processo.</span><span class="sxs-lookup"><span data-stu-id="0df82-111">[**IEnumBackgroundCopyFiles**](ienumbackgroundcopyfiles-.md) interface pointer that you use to enumerate the files in the job.</span></span> <span data-ttu-id="0df82-112">Rilasciare *ppEnumFiles* al termine.</span><span class="sxs-lookup"><span data-stu-id="0df82-112">Release *ppEnumFiles* when done.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0df82-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0df82-113">Return value</span></span>

<span data-ttu-id="0df82-114">Questo metodo restituisce **S_OK** in esito positivo o uno dei valori **HRESULT** com standard in errore.</span><span class="sxs-lookup"><span data-stu-id="0df82-114">This method returns **S_OK** on success or one of the standard COM **HRESULT** values on error.</span></span>

## <a name="requirements"></a><span data-ttu-id="0df82-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0df82-115">Requirements</span></span>



| <span data-ttu-id="0df82-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="0df82-116">Requirement</span></span> | <span data-ttu-id="0df82-117">Valore</span><span class="sxs-lookup"><span data-stu-id="0df82-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0df82-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0df82-118">Minimum supported client</span></span><br/> | <span data-ttu-id="0df82-119">Solo app desktop Windows 10 versione 1709 \[\]</span><span class="sxs-lookup"><span data-stu-id="0df82-119">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="0df82-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0df82-120">Minimum supported server</span></span><br/> | <span data-ttu-id="0df82-121">Windows Server, versione 1709 \[ solo per le app desktop\]</span><span class="sxs-lookup"><span data-stu-id="0df82-121">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="0df82-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0df82-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="0df82-123"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="0df82-123"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="0df82-124">IDL</span><span class="sxs-lookup"><span data-stu-id="0df82-124">IDL</span></span><br/>                      | <dl> <span data-ttu-id="0df82-125"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="0df82-125"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="0df82-126">Libreria</span><span class="sxs-lookup"><span data-stu-id="0df82-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="0df82-127"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0df82-127"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="0df82-128">DLL</span><span class="sxs-lookup"><span data-stu-id="0df82-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0df82-129"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0df82-129"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="0df82-130">IID</span><span class="sxs-lookup"><span data-stu-id="0df82-130">IID</span></span><br/>                      | <span data-ttu-id="0df82-131">IID_IBackgroundCopyJob viene definito come 37668D37-507E-4160-9316-26306D150B12</span><span class="sxs-lookup"><span data-stu-id="0df82-131">IID_IBackgroundCopyJob is defined as 37668D37-507E-4160-9316-26306D150B12</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="0df82-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0df82-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0df82-133">**Metodo ibackgroundcopyjob**</span><span class="sxs-lookup"><span data-stu-id="0df82-133">**IBackgroundCopyJob**</span></span>](ibackgroundcopyjob-.md)
</dt> <dt>

[<span data-ttu-id="0df82-134">**IEnumBackgroundCopyFiles**</span><span class="sxs-lookup"><span data-stu-id="0df82-134">**IEnumBackgroundCopyFiles**</span></span>](ienumbackgroundcopyfiles-.md)
</dt> </dl>

 

 






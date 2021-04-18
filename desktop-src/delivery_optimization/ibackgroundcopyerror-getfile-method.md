---
title: Metodo GetFile IBackgroundCopyError (Deliveryoptimization. h)
description: Recupera un puntatore di interfaccia all'oggetto file associato all'errore.
ms.assetid: 7E1DB3EE-0690-4D0E-BA98-70F5FBDCF12F
keywords:
- Metodo GetFile
- Metodo GetFile, interfaccia IBackgroundCopyError
- Interfaccia IBackgroundCopyError, metodo GetFile
topic_type:
- apiref
api_name:
- IBackgroundCopyError.GetFile
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b84396797378c77a6f774b4c63a3966b0d601b7f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301486"
---
# <a name="ibackgroundcopyerrorgetfile-method"></a><span data-ttu-id="01ef6-106">Metodo IBackgroundCopyError:: GetFile</span><span class="sxs-lookup"><span data-stu-id="01ef6-106">IBackgroundCopyError::GetFile method</span></span>

<span data-ttu-id="01ef6-107">Recupera un puntatore di interfaccia all'oggetto file associato all'errore.</span><span class="sxs-lookup"><span data-stu-id="01ef6-107">Retrieves an interface pointer to the file object associated with the error.</span></span>

## <a name="syntax"></a><span data-ttu-id="01ef6-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="01ef6-108">Syntax</span></span>


```C++
HRESULT GetFile(
  [out] IBackgroundCopyFile **ppFile
);
```



## <a name="parameters"></a><span data-ttu-id="01ef6-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="01ef6-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="01ef6-110">*ppFile* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="01ef6-110">*ppFile* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="01ef6-111">Puntatore all'interfaccia [**IBackgroundCopyFile**](ibackgroundcopyfile.md) i cui metodi vengono utilizzati per determinare i nomi file locali e remoti associati all'errore.</span><span class="sxs-lookup"><span data-stu-id="01ef6-111">An [**IBackgroundCopyFile**](ibackgroundcopyfile.md) interface pointer whose methods you use to determine the local and remote file names associated with the error.</span></span> <span data-ttu-id="01ef6-112">Il parametro *ppFile* è impostato su **null** se l'errore non è associato al file locale o remoto.</span><span class="sxs-lookup"><span data-stu-id="01ef6-112">The *ppFile* parameter is set to **NULL** if the error is not associated with the local or remote file.</span></span> <span data-ttu-id="01ef6-113">Al termine, rilasciare *ppFile*.</span><span class="sxs-lookup"><span data-stu-id="01ef6-113">When done, release *ppFile*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="01ef6-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="01ef6-114">Return value</span></span>

<span data-ttu-id="01ef6-115">Questo metodo restituisce i valori **HRESULT** seguenti.</span><span class="sxs-lookup"><span data-stu-id="01ef6-115">This method returns the following **HRESULT** values.</span></span>



| <span data-ttu-id="01ef6-116">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="01ef6-116">Return code</span></span>                                                                                                | <span data-ttu-id="01ef6-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="01ef6-117">Description</span></span>                                                                                                    |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="01ef6-118"><dt>S_OK \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="01ef6-118"><dt>\*\*\*\*S_OK\*\*\*\*</dt></span></span> </dl>                   | <span data-ttu-id="01ef6-119">Il puntatore di interfaccia all'oggetto file è stato recuperato.</span><span class="sxs-lookup"><span data-stu-id="01ef6-119">Successfully retrieved an interface pointer to the file object.</span></span><br/>                                     |
| <dl> <span data-ttu-id="01ef6-120"><dt>**DO_E_FILE_NOT_AVAILABLE**</dt></span><span class="sxs-lookup"><span data-stu-id="01ef6-120"><dt>**DO_E_FILE_NOT_AVAILABLE**</dt></span></span> </dl> | <span data-ttu-id="01ef6-121">L'errore non è associato a un file locale o remoto.</span><span class="sxs-lookup"><span data-stu-id="01ef6-121">The error is not associated with a local or remote file.</span></span> <span data-ttu-id="01ef6-122">Il parametro *ppFile* è impostato su **null**.</span><span class="sxs-lookup"><span data-stu-id="01ef6-122">The *ppFile* parameter is set to **NULL**.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="01ef6-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="01ef6-123">Requirements</span></span>



| <span data-ttu-id="01ef6-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="01ef6-124">Requirement</span></span> | <span data-ttu-id="01ef6-125">Valore</span><span class="sxs-lookup"><span data-stu-id="01ef6-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="01ef6-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="01ef6-126">Minimum supported client</span></span><br/> | <span data-ttu-id="01ef6-127">Solo app desktop Windows 10 versione 1709 \[\]</span><span class="sxs-lookup"><span data-stu-id="01ef6-127">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="01ef6-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="01ef6-128">Minimum supported server</span></span><br/> | <span data-ttu-id="01ef6-129">Windows Server, versione 1709 \[ solo per le app desktop\]</span><span class="sxs-lookup"><span data-stu-id="01ef6-129">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="01ef6-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="01ef6-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="01ef6-131"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="01ef6-131"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="01ef6-132">IDL</span><span class="sxs-lookup"><span data-stu-id="01ef6-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="01ef6-133"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="01ef6-133"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="01ef6-134">Libreria</span><span class="sxs-lookup"><span data-stu-id="01ef6-134">Library</span></span><br/>                  | <dl> <span data-ttu-id="01ef6-135"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="01ef6-135"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="01ef6-136">DLL</span><span class="sxs-lookup"><span data-stu-id="01ef6-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="01ef6-137"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="01ef6-137"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="01ef6-138">IID</span><span class="sxs-lookup"><span data-stu-id="01ef6-138">IID</span></span><br/>                      | <span data-ttu-id="01ef6-139">IID_IBackgroundCopyError viene definito come 19C613A0-FCB8-4F28-81AE-897C3D078F81</span><span class="sxs-lookup"><span data-stu-id="01ef6-139">IID_IBackgroundCopyError is defined as 19C613A0-FCB8-4F28-81AE-897C3D078F81</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="01ef6-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="01ef6-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="01ef6-141">**IBackgroundCopyError**</span><span class="sxs-lookup"><span data-stu-id="01ef6-141">**IBackgroundCopyError**</span></span>](ibackgroundcopyerror.md)
</dt> <dt>

[<span data-ttu-id="01ef6-142">**IBackgroundCopyError:: GetError**</span><span class="sxs-lookup"><span data-stu-id="01ef6-142">**IBackgroundCopyError::GetError**</span></span>](ibackgroundcopyerror-geterror-method.md)
</dt> </dl>

 

 






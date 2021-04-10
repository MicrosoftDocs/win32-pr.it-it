---
title: Metodo IDeliveryOptimizationJob2 AddFile
description: Il metodo AddFile aggiunge un singolo file a un processo DO esistente.
keywords:
- AddFile (metodo)
- Metodo AddFile, interfaccia IDeliveryOptimizationJob2
- Interfaccia IDeliveryOptimizationJob2, metodo AddFile
topic_type:
- apiref
api_name:
- IDeliveryOptimizationJob2.AddFile
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 01/18/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8225db8cccb1e1d3bb364ba1dc29f30526fe36b7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119351"
---
# <a name="ideliveryoptimizationjob2addfilewithranges-method"></a><span data-ttu-id="91011-106">Metodo IDeliveryOptimizationJob2:: AddFileWithRanges</span><span class="sxs-lookup"><span data-stu-id="91011-106">IDeliveryOptimizationJob2::AddFileWithRanges method</span></span>

<span data-ttu-id="91011-107">Il metodo AddFile aggiunge un singolo file a un processo DO esistente.</span><span class="sxs-lookup"><span data-stu-id="91011-107">The AddFile method adds a single file to an existing DO job.</span></span>

## <a name="syntax"></a><span data-ttu-id="91011-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="91011-108">Syntax</span></span>

```C++
HRESULT AddFile(
  [in]                              LPCWSTR       fileId,
  [in, unique]                      LPCWSTR       remoteUrl,
  [in]                              DWORD         rangeCount,
  [in, size_is(rangeCount), unique] BG_FILE_RANGE ranges[],
  [in]                              REFIID        riid,
  [out]                             void          **object
);
```

## <a name="parameters"></a><span data-ttu-id="91011-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="91011-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="91011-110">*fileId* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="91011-110">*fileId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="91011-111">Stringa ID file, che identifica in modo univoco il file da scaricare.</span><span class="sxs-lookup"><span data-stu-id="91011-111">The file ID string, which uniquely identifies the file to be downloaded.</span></span>

</dd> <dt>

<span data-ttu-id="91011-112">*remoteUrl* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="91011-112">*remoteUrl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="91011-113">L'URL del file che tenterà di connettersi per scaricare il file.</span><span class="sxs-lookup"><span data-stu-id="91011-113">The file URL that DO will attempt to connect to download the file.</span></span>

</dd> <dt>

<span data-ttu-id="91011-114">*rangeCount* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="91011-114">*rangeCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="91011-115">Numero di elementi contenuti in *intervalli*.</span><span class="sxs-lookup"><span data-stu-id="91011-115">The number of items contained in *ranges*.</span></span> <span data-ttu-id="91011-116">Un valore pari a zero indica che per il file non viene utilizzato alcun intervallo.</span><span class="sxs-lookup"><span data-stu-id="91011-116">A zero value means that no ranges are used for the file.</span></span>

</dd> <dt>

<span data-ttu-id="91011-117">*intervalli* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="91011-117">*ranges* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="91011-118">Elenco di intervalli facoltativo.</span><span class="sxs-lookup"><span data-stu-id="91011-118">The optional range list.</span></span> <span data-ttu-id="91011-119">Ogni intervallo nell'elenco è una struttura [**BG_FILE_RANGE**](bg-file-range.md) .</span><span class="sxs-lookup"><span data-stu-id="91011-119">Each range in the list is a [**BG_FILE_RANGE**](bg-file-range.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="91011-120">*riid* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="91011-120">*riid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="91011-121">Tipo di oggetto contenuto nell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="91011-121">The type of object contained in object.</span></span> <span data-ttu-id="91011-122">Deve essere di tipo IID_IDeliveryOptimizationFile.</span><span class="sxs-lookup"><span data-stu-id="91011-122">This must by of type IID_IDeliveryOptimizationFile.</span></span>

</dd> <dt>

<span data-ttu-id="91011-123">*oggetto* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="91011-123">*object* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="91011-124">Oggetto IDeliveryOptimizationFile, che rappresenta il file di download.</span><span class="sxs-lookup"><span data-stu-id="91011-124">The IDeliveryOptimizationFile object, which represents the download file.</span></span> 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="91011-125">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="91011-125">Return value</span></span>

<span data-ttu-id="91011-126">Questo metodo restituisce S_OK in esito positivo o uno dei valori HRESULT standard in errore.</span><span class="sxs-lookup"><span data-stu-id="91011-126">This method returns S_OK on success or one of the standard HRESULT values on error.</span></span>

## <a name="requirements"></a><span data-ttu-id="91011-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="91011-127">Requirements</span></span>

| <span data-ttu-id="91011-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="91011-128">Requirement</span></span> | <span data-ttu-id="91011-129">Valore</span><span class="sxs-lookup"><span data-stu-id="91011-129">Value</span></span> |
|---------------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="91011-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="91011-130">Minimum supported client</span></span>  | <span data-ttu-id="91011-131">Solo app desktop Windows 10 versione 1803 \[\]</span><span class="sxs-lookup"><span data-stu-id="91011-131">Windows 10, version 1803 \[desktop apps only\]</span></span>                                  |
| <span data-ttu-id="91011-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="91011-132">Minimum supported server</span></span>  | <span data-ttu-id="91011-133">Windows Server, versione 1709 \[ solo per le app desktop\]</span><span class="sxs-lookup"><span data-stu-id="91011-133">Windows Server, version 1709 \[desktop apps only\]</span></span>                              |
| <span data-ttu-id="91011-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="91011-134">Header</span></span>                    | <span data-ttu-id="91011-135">Deliveryoptimization. h</span><span class="sxs-lookup"><span data-stu-id="91011-135">Deliveryoptimization.h</span></span>                                                          |
| <span data-ttu-id="91011-136">IDL</span><span class="sxs-lookup"><span data-stu-id="91011-136">IDL</span></span>                       | <span data-ttu-id="91011-137">DeliveryOptimization. idl</span><span class="sxs-lookup"><span data-stu-id="91011-137">DeliveryOptimization.idl</span></span>                                                        |
| <span data-ttu-id="91011-138">Libreria</span><span class="sxs-lookup"><span data-stu-id="91011-138">Library</span></span>                   | <span data-ttu-id="91011-139">Dosvc. lib</span><span class="sxs-lookup"><span data-stu-id="91011-139">Dosvc.lib</span></span>                                                                       |
| <span data-ttu-id="91011-140">DLL</span><span class="sxs-lookup"><span data-stu-id="91011-140">DLL</span></span>                       | <span data-ttu-id="91011-141">Dosvc.dll</span><span class="sxs-lookup"><span data-stu-id="91011-141">Dosvc.dll</span></span>                                                                       |
| <span data-ttu-id="91011-142">IID</span><span class="sxs-lookup"><span data-stu-id="91011-142">IID</span></span>                       | <span data-ttu-id="91011-143">IID_IDeliveryOptimizationJob viene definito come EE2584CF-A69C-4848-B633-2649962B3EF7</span><span class="sxs-lookup"><span data-stu-id="91011-143">IID_IDeliveryOptimizationJob is defined as EE2584CF-A69C-4848-B633-2649962B3EF7</span></span> |

## <a name="see-also"></a><span data-ttu-id="91011-144">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="91011-144">See also</span></span>

[<span data-ttu-id="91011-145">**IDeliveryOptimizationJob2**</span><span class="sxs-lookup"><span data-stu-id="91011-145">**IDeliveryOptimizationJob2**</span></span>](ideliveryoptimizationjob2.md)

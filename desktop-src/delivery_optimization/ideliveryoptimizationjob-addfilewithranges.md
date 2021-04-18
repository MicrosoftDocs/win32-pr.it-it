---
title: Metodo IDeliveryOptimizationJob AddFileWithRanges (Deliveryoptimization. h)
description: Aggiunge un file a un processo di download e specifica gli intervalli del file che si desidera scaricare.
ms.assetid: 23F0A39F-670F-4030-A3B3-4F9277FFA8AB
keywords:
- Metodo AddFileWithRanges
- Metodo AddFileWithRanges, interfaccia IDeliveryOptimizationJob
- Interfaccia IDeliveryOptimizationJob, metodo AddFileWithRanges
topic_type:
- apiref
api_name:
- IDeliveryOptimizationJob.AddFileWithRanges
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cc147f5cb3f91a2fe0b8518493dba72798ce8056
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302656"
---
# <a name="ideliveryoptimizationjobaddfilewithranges-method"></a><span data-ttu-id="b1313-106">Metodo IDeliveryOptimizationJob:: AddFileWithRanges</span><span class="sxs-lookup"><span data-stu-id="b1313-106">IDeliveryOptimizationJob::AddFileWithRanges method</span></span>

<span data-ttu-id="b1313-107">Aggiunge un file a un processo di download e specifica gli intervalli del file che si desidera scaricare.</span><span class="sxs-lookup"><span data-stu-id="b1313-107">Adds a file to a download job and specifies the ranges of the file you want to download.</span></span>

## <a name="syntax"></a><span data-ttu-id="b1313-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b1313-108">Syntax</span></span>


```C++
HRESULT AddFileWithRanges(
  [in]           LPCWSTR       fileId,
  [in]           LPCWSTR       remoteUrl,
  [in]           LPCWSTR       localName,
  [in, optional] DWORD         rangeCount,
  [in, optional] BG_FILE_RANGE ranges[],
  [in, optional] ULONG64       fileSize
);
```



## <a name="parameters"></a><span data-ttu-id="b1313-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="b1313-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b1313-110">*fileId* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b1313-110">*fileId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b1313-111">Stringa con terminazione null che è un identificatore univoco del contenuto pubblicato.</span><span class="sxs-lookup"><span data-stu-id="b1313-111">Null terminated string that s an unique identifier of the published content.</span></span> <span data-ttu-id="b1313-112">Per il contenuto non pubblicato, può trattarsi di qualsiasi stringa univoca che il chiamante può usare per identificare i file all'interno di un processo.</span><span class="sxs-lookup"><span data-stu-id="b1313-112">For non-published content, this can be any unique string that caller can use to identify files within a job.</span></span>

</dd> <dt>

<span data-ttu-id="b1313-113">*remoteUrl* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b1313-113">*remoteUrl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b1313-114">Stringa con terminazione null che contiene il nome del file nel server.</span><span class="sxs-lookup"><span data-stu-id="b1313-114">Null-terminated string that contains the name of the file on the server.</span></span>

</dd> <dt>

<span data-ttu-id="b1313-115">*localName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b1313-115">*localName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b1313-116">Stringa con terminazione null che contiene il nome del file nel client.</span><span class="sxs-lookup"><span data-stu-id="b1313-116">Null-terminated string that contains the name of the file on the client.</span></span>

</dd> <dt>

<span data-ttu-id="b1313-117">*rangeCount* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="b1313-117">*rangeCount* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b1313-118">Numero di elementi negli *intervalli*.</span><span class="sxs-lookup"><span data-stu-id="b1313-118">Number of elements in *Ranges*.</span></span>

</dd> <dt>

<span data-ttu-id="b1313-119">*intervalli* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="b1313-119">*ranges* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b1313-120">Matrice di una o più strutture di [**BG_FILE_RANGE**](/windows/desktop/api/bits2_0/ns-bits2_0-bg_file_range) che specificano gli intervalli da scaricare.</span><span class="sxs-lookup"><span data-stu-id="b1313-120">Array of one or more [**BG_FILE_RANGE**](/windows/desktop/api/bits2_0/ns-bits2_0-bg_file_range) structures that specify the ranges to download.</span></span> <span data-ttu-id="b1313-121">Non specificare intervalli duplicati o sovrapposti.</span><span class="sxs-lookup"><span data-stu-id="b1313-121">Do not specify duplicate or overlapping ranges.</span></span>

</dd> <dt>

<span data-ttu-id="b1313-122">*Filesize* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="b1313-122">*fileSize* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b1313-123">Dimensioni del file, in byte.</span><span class="sxs-lookup"><span data-stu-id="b1313-123">Size of the file in bytes.</span></span> <span data-ttu-id="b1313-124">Passare **DO_UNKNOWN_FILE_SIZE** se le dimensioni non sono note all'applicazione chiamante.</span><span class="sxs-lookup"><span data-stu-id="b1313-124">Pass in **DO_UNKNOWN_FILE_SIZE** if size is not known to the caller application.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b1313-125">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b1313-125">Return value</span></span>

<span data-ttu-id="b1313-126">Questo metodo restituisce i valori restituiti seguenti e altri.</span><span class="sxs-lookup"><span data-stu-id="b1313-126">This method returns the following return values, as well as others.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b1313-127">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="b1313-127">Return code</span></span></th>
<th><span data-ttu-id="b1313-128">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b1313-128">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><dl> <span data-ttu-id="b1313-129"><dt><strong><strong>S_OK</strong></strong></dt> </span><span class="sxs-lookup"><span data-stu-id="b1313-129"><dt><strong><strong>S_OK</strong></strong></dt> </span></span></dl></td>
<td><span data-ttu-id="b1313-130">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="b1313-130">Success.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="b1313-131"><dt><strong>E_INVALIDARG</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="b1313-131"><dt><strong>E_INVALIDARG</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="b1313-132">Il nome del file locale è NULL o una stringa vuota.</span><span class="sxs-lookup"><span data-stu-id="b1313-132">The local file name is NULL or empty string.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="b1313-133"><dt><strong>E_ACCESSDENIED</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="b1313-133"><dt><strong>E_ACCESSDENIED</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="b1313-134">L'utente non dispone delle autorizzazioni necessarie per scrivere nella directory specificata nel client.</span><span class="sxs-lookup"><span data-stu-id="b1313-134">User does not have permission to write to the specified directory on the client.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="b1313-135"><dt><strong>DO_E_INVALID_RANGE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="b1313-135"><dt><strong>DO_E_INVALID_RANGE</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="b1313-136">Uno degli intervalli non è valido.</span><span class="sxs-lookup"><span data-stu-id="b1313-136">One of the ranges is invalid.</span></span> <span data-ttu-id="b1313-137">Ad esempio, InitialOffset è impostato su <strong>BG_LENGTH_TO_EOF</strong>.</span><span class="sxs-lookup"><span data-stu-id="b1313-137">For example, InitialOffset is set to <strong>BG_LENGTH_TO_EOF</strong>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="b1313-138"><dt><strong>DO_E_OVERLAPPING_RANGES</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="b1313-138"><dt><strong>DO_E_OVERLAPPING_RANGES</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="b1313-139">Non è possibile specificare intervalli duplicati o sovrapposti.</span><span class="sxs-lookup"><span data-stu-id="b1313-139">You cannot specify duplicate or overlapping ranges.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="b1313-140">Gli intervalli sono ordinati in base all'offset del valore, non alla lunghezza.</span><span class="sxs-lookup"><span data-stu-id="b1313-140">The ranges are sorted by the offset of the value, not the length.</span></span> <span data-ttu-id="b1313-141">Se vengono immessi intervalli con lo stesso offset, ma in ordine inverso, viene restituito questo errore.</span><span class="sxs-lookup"><span data-stu-id="b1313-141">If ranges are entered that have the same offset, but are in reverse order, then this error will be returned.</span></span> <span data-ttu-id="b1313-142">Se, ad esempio, vengono immessi 100,5 e 100,0 in questo ordine, non sarà possibile aggiungere il file al processo.</span><span class="sxs-lookup"><span data-stu-id="b1313-142">For example, if 100.5 and 100.0 are entered in that order, then you will not be able to add the file to the job.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="b1313-143"><dt><strong>DO_E_INVALID_STATE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="b1313-143"><dt><strong>DO_E_INVALID_STATE</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="b1313-144">Lo stato del processo non può essere <strong>BG_JOB_STATE_CANCELLED</strong> o <strong>BG_JOB_STATE_ACKNOWLEDGED</strong>.</span><span class="sxs-lookup"><span data-stu-id="b1313-144">The state of the job cannot be <strong>BG_JOB_STATE_CANCELLED</strong> or <strong>BG_JOB_STATE_ACKNOWLEDGED</strong>.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="b1313-145">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b1313-145">Requirements</span></span>



| <span data-ttu-id="b1313-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="b1313-146">Requirement</span></span> | <span data-ttu-id="b1313-147">Valore</span><span class="sxs-lookup"><span data-stu-id="b1313-147">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b1313-148">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b1313-148">Minimum supported client</span></span><br/> | <span data-ttu-id="b1313-149">Solo app desktop Windows 10 versione 1709 \[\]</span><span class="sxs-lookup"><span data-stu-id="b1313-149">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="b1313-150">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b1313-150">Minimum supported server</span></span><br/> | <span data-ttu-id="b1313-151">Windows Server, versione 1709 \[ solo per le app desktop\]</span><span class="sxs-lookup"><span data-stu-id="b1313-151">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="b1313-152">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b1313-152">Header</span></span><br/>                   | <dl> <span data-ttu-id="b1313-153"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="b1313-153"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="b1313-154">IDL</span><span class="sxs-lookup"><span data-stu-id="b1313-154">IDL</span></span><br/>                      | <dl> <span data-ttu-id="b1313-155"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="b1313-155"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="b1313-156">Libreria</span><span class="sxs-lookup"><span data-stu-id="b1313-156">Library</span></span><br/>                  | <dl> <span data-ttu-id="b1313-157"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b1313-157"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="b1313-158">DLL</span><span class="sxs-lookup"><span data-stu-id="b1313-158">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b1313-159"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b1313-159"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="b1313-160">IID</span><span class="sxs-lookup"><span data-stu-id="b1313-160">IID</span></span><br/>                      | <span data-ttu-id="b1313-161">IID_IDeliveryOptimizationJob viene definito come EE2584CF-A69C-4848-B633-2649962B3EF7</span><span class="sxs-lookup"><span data-stu-id="b1313-161">IID_IDeliveryOptimizationJob is defined as EE2584CF-A69C-4848-B633-2649962B3EF7</span></span><br/>         |



## <a name="see-also"></a><span data-ttu-id="b1313-162">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b1313-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b1313-163">**IDeliveryOptimizationJob**</span><span class="sxs-lookup"><span data-stu-id="b1313-163">**IDeliveryOptimizationJob**</span></span>](ideliveryoptimizationjob.md)
</dt> </dl>

 


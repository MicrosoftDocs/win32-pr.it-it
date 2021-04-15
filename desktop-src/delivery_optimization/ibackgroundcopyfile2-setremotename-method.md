---
title: Metodo IBackgroundCopyFile2 seremotename (Deliveryoptimization. h)
description: Consente di modificare il nome remoto in un nuovo URL in un processo di download.
ms.assetid: 344D4193-C96E-4B94-AA53-F9307FEB2565
keywords:
- Seremotename (metodo)
- Metodo seremotename, interfaccia IBackgroundCopyFile2
- Interfaccia IBackgroundCopyFile2, metodo seremotename
topic_type:
- apiref
api_name:
- IBackgroundCopyFile2.SetRemoteName
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4afb5448144867c799bd401bc2d7c180d3958f2a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476366"
---
# <a name="ibackgroundcopyfile2setremotename-method"></a><span data-ttu-id="9cf86-106">Metodo IBackgroundCopyFile2:: seremotename</span><span class="sxs-lookup"><span data-stu-id="9cf86-106">IBackgroundCopyFile2::SetRemoteName method</span></span>

<span data-ttu-id="9cf86-107">Consente di modificare il nome remoto in un nuovo URL in un processo di download.</span><span class="sxs-lookup"><span data-stu-id="9cf86-107">Changes the remote name to a new URL in a download job.</span></span>

## <a name="syntax"></a><span data-ttu-id="9cf86-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9cf86-108">Syntax</span></span>


```C++
HRESULT SetRemoteName(
  [in] LPCWSTR RemoteName
);
```



## <a name="parameters"></a><span data-ttu-id="9cf86-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="9cf86-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9cf86-110">*RemoteName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9cf86-110">*RemoteName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9cf86-111">Stringa con terminazione null che contiene il nome del file nel server.</span><span class="sxs-lookup"><span data-stu-id="9cf86-111">Null-terminated string that contains the name of the file on the server.</span></span> <span data-ttu-id="9cf86-112">Per informazioni su come specificare il nome remoto, vedere il membro **RemoteName** .</span><span class="sxs-lookup"><span data-stu-id="9cf86-112">For information on specifying the remote name, see the **RemoteName** member.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9cf86-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9cf86-113">Return value</span></span>

<span data-ttu-id="9cf86-114">Questo metodo restituisce i valori restituiti seguenti e altri.</span><span class="sxs-lookup"><span data-stu-id="9cf86-114">This method returns the following return values, as well as others.</span></span>



| <span data-ttu-id="9cf86-115">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="9cf86-115">Return code</span></span>                                                                                  | <span data-ttu-id="9cf86-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9cf86-116">Description</span></span>                                                                                                           |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="9cf86-117"><dt>S_OK \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="9cf86-117"><dt>\*\*\*\*S_OK\*\*\*\*</dt></span></span> </dl>     | <span data-ttu-id="9cf86-118">Operazione riuscita</span><span class="sxs-lookup"><span data-stu-id="9cf86-118">Success</span></span><br/>                                                                                                    |
| <dl> <span data-ttu-id="9cf86-119"><dt>**E_INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="9cf86-119"><dt>**E_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="9cf86-120">Il nuovo nome remoto è un URL non valido o il nuovo URL è troppo lungo (l'URL non può superare i 2.200 caratteri).</span><span class="sxs-lookup"><span data-stu-id="9cf86-120">The new remote name is an invalid URL or the new URL is too long (the URL cannot exceed 2,200 characters).</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="9cf86-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="9cf86-121">Remarks</span></span>

<span data-ttu-id="9cf86-122">In genere, questo metodo viene chiamato se si vuole modificare l'URL usato per trasferire il file o se si vuole modificare il nome o il percorso del file.</span><span class="sxs-lookup"><span data-stu-id="9cf86-122">Typically, you call this method if you want to change the URL used to transfer the file or if you want to change the file name or path.</span></span>

<span data-ttu-id="9cf86-123">Questo metodo non serializza quando restituisce.</span><span class="sxs-lookup"><span data-stu-id="9cf86-123">This method does not serialize when it returns.</span></span> <span data-ttu-id="9cf86-124">Per serializzare la modifica, [**sospendere**](ibackgroundcopyjob-suspend.md) il processo, chiamare questo metodo (se si modificano più file nel processo, usare un ciclo) e [**riprendere**](ibackgroundcopyjob-resume.md) il processo.</span><span class="sxs-lookup"><span data-stu-id="9cf86-124">To serialize the change, [**suspend**](ibackgroundcopyjob-suspend.md) the job, call this method (if changing multiple files in the job, use a loop), and [**resume**](ibackgroundcopyjob-resume.md) the job.</span></span> <span data-ttu-id="9cf86-125">La chiamata al metodo **Metodo ibackgroundcopyjob:: Resume** serializza la modifica.</span><span class="sxs-lookup"><span data-stu-id="9cf86-125">Calling the **IBackgroundCopyJob::Resume** method serializes the change.</span></span>

<span data-ttu-id="9cf86-126">Se il timestamp o le dimensioni del file del nuovo nome remoto sono diverse dal nome remoto precedente o se il nuovo server non supporta il ripristino del checkpoint (per i nomi remoti HTTP), riavviare il download.</span><span class="sxs-lookup"><span data-stu-id="9cf86-126">If the time stamp or file size of the new remote name is different from the previous remote name or the new server does not support checkpoint resume (for HTTP remote names), DO restarts the download.</span></span> <span data-ttu-id="9cf86-127">In caso contrario, il trasferimento riprende dalla stessa posizione nel nuovo server.</span><span class="sxs-lookup"><span data-stu-id="9cf86-127">Otherwise, the transfer resumes from the same position on the new server.</span></span> <span data-ttu-id="9cf86-128">DO non riavvia i file già trasferiti.</span><span class="sxs-lookup"><span data-stu-id="9cf86-128">DO does not restart already transferred files.</span></span>

## <a name="requirements"></a><span data-ttu-id="9cf86-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9cf86-129">Requirements</span></span>



| <span data-ttu-id="9cf86-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="9cf86-130">Requirement</span></span> | <span data-ttu-id="9cf86-131">Valore</span><span class="sxs-lookup"><span data-stu-id="9cf86-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9cf86-132">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9cf86-132">Minimum supported client</span></span><br/> | <span data-ttu-id="9cf86-133">Solo app desktop Windows 10 versione 1709 \[\]</span><span class="sxs-lookup"><span data-stu-id="9cf86-133">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="9cf86-134">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9cf86-134">Minimum supported server</span></span><br/> | <span data-ttu-id="9cf86-135">Windows Server, versione 1709 \[ solo per le app desktop\]</span><span class="sxs-lookup"><span data-stu-id="9cf86-135">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="9cf86-136">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9cf86-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="9cf86-137"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="9cf86-137"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="9cf86-138">IDL</span><span class="sxs-lookup"><span data-stu-id="9cf86-138">IDL</span></span><br/>                      | <dl> <span data-ttu-id="9cf86-139"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="9cf86-139"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="9cf86-140">Libreria</span><span class="sxs-lookup"><span data-stu-id="9cf86-140">Library</span></span><br/>                  | <dl> <span data-ttu-id="9cf86-141"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9cf86-141"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="9cf86-142">DLL</span><span class="sxs-lookup"><span data-stu-id="9cf86-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9cf86-143"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9cf86-143"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="9cf86-144">IID</span><span class="sxs-lookup"><span data-stu-id="9cf86-144">IID</span></span><br/>                      | <span data-ttu-id="9cf86-145">IID_IBackgroundCopyFile2 viene definito come 83e81b93-0873-474d-8A8C-f2018b1a939c</span><span class="sxs-lookup"><span data-stu-id="9cf86-145">IID_IBackgroundCopyFile2 is defined as 83e81b93-0873-474d-8a8c-f2018b1a939c</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="9cf86-146">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9cf86-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9cf86-147">**IBackgroundCopyFile2**</span><span class="sxs-lookup"><span data-stu-id="9cf86-147">**IBackgroundCopyFile2**</span></span>](ibackgroundcopyfile2.md)
</dt> </dl>

 

 






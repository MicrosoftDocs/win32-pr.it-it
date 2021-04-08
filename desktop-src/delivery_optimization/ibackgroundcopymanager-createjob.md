---
title: Metodo IBackgroundCopyManager CreateJob (Deliveryoptimization. h)
description: Crea un processo.
ms.assetid: BDE5BE4D-9AE9-463D-B900-850D255EAB58
keywords:
- Metodo CreateJob
- Metodo CreateJob, interfaccia IBackgroundCopyManager
- Interfaccia IBackgroundCopyManager, metodo CreateJob
topic_type:
- apiref
api_name:
- IBackgroundCopyManager.CreateJob
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: de7f0b61cdbc5d5776039c3bf13b83ca0a6f8fdc
ms.sourcegitcommit: ea73413ee4f69fa573ee0cd4422f20d17bd42e1f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/27/2021
ms.locfileid: "104058393"
---
# <a name="ibackgroundcopymanagercreatejob-method"></a><span data-ttu-id="11dd1-106">Metodo IBackgroundCopyManager:: CreateJob</span><span class="sxs-lookup"><span data-stu-id="11dd1-106">IBackgroundCopyManager::CreateJob method</span></span>

<span data-ttu-id="11dd1-107">Crea un processo.</span><span class="sxs-lookup"><span data-stu-id="11dd1-107">Creates a job.</span></span>

## <a name="syntax"></a><span data-ttu-id="11dd1-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="11dd1-108">Syntax</span></span>


```C++
HRESULT CreateJob(
  [in]  LPCWSTR            pDisplayName,
  [in]  BG_JOB_TYPE        Type,
  [out] GUID               *pJobID,
  [out] IBackgroundCopyJob **ppJob
);
```



## <a name="parameters"></a><span data-ttu-id="11dd1-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="11dd1-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="11dd1-110">*pDisplayName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="11dd1-110">*pDisplayName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="11dd1-111">Stringa con terminazione null che contiene un nome visualizzato per il processo.</span><span class="sxs-lookup"><span data-stu-id="11dd1-111">Null-terminated string that contains a display name for the job.</span></span> <span data-ttu-id="11dd1-112">In genere, il nome visualizzato viene usato per identificare il processo in un'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="11dd1-112">Typically, the display name is used to identify the job in a user interface.</span></span> <span data-ttu-id="11dd1-113">Si noti che più processi possono avere lo stesso nome visualizzato.</span><span class="sxs-lookup"><span data-stu-id="11dd1-113">Note that more than one job may have the same display name.</span></span> <span data-ttu-id="11dd1-114">Non può essere **null**.</span><span class="sxs-lookup"><span data-stu-id="11dd1-114">Must not be **NULL**.</span></span> <span data-ttu-id="11dd1-115">Il nome è limitato a 256 caratteri, escluso il carattere di terminazione null.</span><span class="sxs-lookup"><span data-stu-id="11dd1-115">The name is limited to 256 characters, not including the null terminator.</span></span>

</dd> <dt>

<span data-ttu-id="11dd1-116">*Tipo* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="11dd1-116">*Type* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="11dd1-117">Tipo di processo di trasferimento, ad esempio BG_JOB_TYPE_DOWNLOAD.</span><span class="sxs-lookup"><span data-stu-id="11dd1-117">Type of transfer job, such as BG_JOB_TYPE_DOWNLOAD.</span></span> <span data-ttu-id="11dd1-118">Per un elenco dei tipi di trasferimento, vedere l'enumerazione [**BG_JOB_TYPE**](bg-job-type.md) .</span><span class="sxs-lookup"><span data-stu-id="11dd1-118">For a list of transfer types, see the [**BG_JOB_TYPE**](bg-job-type.md) enumeration.</span></span>

</dd> <dt>

<span data-ttu-id="11dd1-119">*pJobID* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="11dd1-119">*pJobID* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="11dd1-120">Identifica in modo univoco il processo nella coda.</span><span class="sxs-lookup"><span data-stu-id="11dd1-120">Uniquely identifies your job in the queue.</span></span> <span data-ttu-id="11dd1-121">Usare questo identificatore quando si chiama il metodo [**IBackgroundCopyManager:: GetJob**](ibackgroundcopymanager-getjob.md) per ottenere un processo dalla coda.</span><span class="sxs-lookup"><span data-stu-id="11dd1-121">Use this identifier when you call the [**IBackgroundCopyManager::GetJob**](ibackgroundcopymanager-getjob.md) method to get a job from the queue.</span></span>

</dd> <dt>

<span data-ttu-id="11dd1-122">*ppJob* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="11dd1-122">*ppJob* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="11dd1-123">Puntatore a interfaccia [**Metodo ibackgroundcopyjob**](ibackgroundcopyjob-.md) che consente di modificare le proprietà del processo e di specificare i file da trasferire.</span><span class="sxs-lookup"><span data-stu-id="11dd1-123">An [**IBackgroundCopyJob**](ibackgroundcopyjob-.md) interface pointer that you use to modify the job's properties and specify the files to be transferred.</span></span> <span data-ttu-id="11dd1-124">Per attivare il processo nella coda, chiamare il metodo [**Metodo ibackgroundcopyjob:: Resume**](ibackgroundcopyjob-resume.md) .</span><span class="sxs-lookup"><span data-stu-id="11dd1-124">To activate the job in the queue, call the [**IBackgroundCopyJob::Resume**](ibackgroundcopyjob-resume.md) method.</span></span> <span data-ttu-id="11dd1-125">Rilasciare *ppJob* al termine.</span><span class="sxs-lookup"><span data-stu-id="11dd1-125">Release *ppJob* when done.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="11dd1-126">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="11dd1-126">Return value</span></span>

<span data-ttu-id="11dd1-127">Questo metodo restituisce i valori **HRESULT** seguenti e altri.</span><span class="sxs-lookup"><span data-stu-id="11dd1-127">This method returns the following **HRESULT** values, as well as others.</span></span>



| <span data-ttu-id="11dd1-128">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="11dd1-128">Return code</span></span>                                                                              | <span data-ttu-id="11dd1-129">Descrizione</span><span class="sxs-lookup"><span data-stu-id="11dd1-129">Description</span></span>                                    |
|------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="11dd1-130"><dt>S_OK \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="11dd1-130"><dt>\*\*\*\*S_OK\*\*\*\*</dt></span></span> </dl> | <span data-ttu-id="11dd1-131">Generazione del nuovo processo completata.</span><span class="sxs-lookup"><span data-stu-id="11dd1-131">Successfully generated the new job.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="11dd1-132">Commenti</span><span class="sxs-lookup"><span data-stu-id="11dd1-132">Remarks</span></span>

<span data-ttu-id="11dd1-133">Solo l'utente che crea il processo o un utente con privilegi di amministratore può [aggiungere file al processo](https://www.bing.com/search?q=add+files+to+the+job) e [modificare le proprietà del processo](https://www.bing.com/search?q=change+the+job's+properties).</span><span class="sxs-lookup"><span data-stu-id="11dd1-133">Only the user who creates the job or a user with administrator privileges can [add files to the job](https://www.bing.com/search?q=add+files+to+the+job) and [change the job's properties](https://www.bing.com/search?q=change+the+job's+properties).</span></span>

## <a name="requirements"></a><span data-ttu-id="11dd1-134">Requisiti</span><span class="sxs-lookup"><span data-stu-id="11dd1-134">Requirements</span></span>



| <span data-ttu-id="11dd1-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="11dd1-135">Requirement</span></span> | <span data-ttu-id="11dd1-136">Valore</span><span class="sxs-lookup"><span data-stu-id="11dd1-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="11dd1-137">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="11dd1-137">Minimum supported client</span></span><br/> | <span data-ttu-id="11dd1-138">Solo app desktop Windows 10 versione 1709 \[\]</span><span class="sxs-lookup"><span data-stu-id="11dd1-138">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="11dd1-139">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="11dd1-139">Minimum supported server</span></span><br/> | <span data-ttu-id="11dd1-140">Windows Server, versione 1709 \[ solo per le app desktop\]</span><span class="sxs-lookup"><span data-stu-id="11dd1-140">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="11dd1-141">Intestazione</span><span class="sxs-lookup"><span data-stu-id="11dd1-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="11dd1-142"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="11dd1-142"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="11dd1-143">IDL</span><span class="sxs-lookup"><span data-stu-id="11dd1-143">IDL</span></span><br/>                      | <dl> <span data-ttu-id="11dd1-144"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="11dd1-144"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="11dd1-145">Libreria</span><span class="sxs-lookup"><span data-stu-id="11dd1-145">Library</span></span><br/>                  | <dl> <span data-ttu-id="11dd1-146"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="11dd1-146"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="11dd1-147">DLL</span><span class="sxs-lookup"><span data-stu-id="11dd1-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="11dd1-148"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="11dd1-148"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="11dd1-149">IID</span><span class="sxs-lookup"><span data-stu-id="11dd1-149">IID</span></span><br/>                      | <span data-ttu-id="11dd1-150">IID_IBackgroundCopyManager viene definito come 5CE34C0D-0DC9-4C1F-897C-DAA1B78CEE7C</span><span class="sxs-lookup"><span data-stu-id="11dd1-150">IID_IBackgroundCopyManager is defined as 5CE34C0D-0DC9-4C1F-897C-DAA1B78CEE7C</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="11dd1-151">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="11dd1-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="11dd1-152">**IBackgroundCopyManager**</span><span class="sxs-lookup"><span data-stu-id="11dd1-152">**IBackgroundCopyManager**</span></span>](ibackgroundcopymanager.md)
</dt> <dt>

[<span data-ttu-id="11dd1-153">**Metodo ibackgroundcopyjob**</span><span class="sxs-lookup"><span data-stu-id="11dd1-153">**IBackgroundCopyJob**</span></span>](ibackgroundcopyjob-.md)
</dt> <dt>

[<span data-ttu-id="11dd1-154">**Metodo ibackgroundcopyjob:: Resume**</span><span class="sxs-lookup"><span data-stu-id="11dd1-154">**IBackgroundCopyJob::Resume**</span></span>](ibackgroundcopyjob-resume.md)
</dt> </dl>

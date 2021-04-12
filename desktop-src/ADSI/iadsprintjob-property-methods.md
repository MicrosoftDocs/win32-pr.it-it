---
title: Metodi di proprietà IADsPrintJob (IADs. h)
description: I metodi di proprietà per l'interfaccia IADsPrintJob ottengono o impostano le proprietà descritte nella tabella seguente. Per altre informazioni, vedere Metodi della proprietà di interfaccia.
ms.assetid: 23e7cbf3-09ce-44ce-b618-2c0fa6b34428
ms.tgt_platform: multiple
keywords:
- Metodi di proprietà IADsPrintJob ADSI
topic_type:
- apiref
api_name:
- IADsPrintJob Property Methods
- IADsPrintJob.Description
- IADsPrintJob.get_Description
- IADsPrintJob.put_Description
- IADsPrintJob.HostPrintQueue
- IADsPrintJob.get_HostPrintQueue
- IADsPrintJob.Notify
- IADsPrintJob.get_Notify
- IADsPrintJob.put_Notify
- IADsPrintJob.NotifyPath
- IADsPrintJob.get_NotifyPath
- IADsPrintJob.put_NotifyPath
- IADsPrintJob.Priority
- IADsPrintJob.get_Priority
- IADsPrintJob.put_Priority
- IADsPrintJob.Size
- IADsPrintJob.get_Size
- IADsPrintJob.StartTime
- IADsPrintJob.get_StartTime
- IADsPrintJob.put_StartTime
- IADsPrintJob.TimeSubmitted
- IADsPrintJob.get_TimeSubmitted
- IADsPrintJob.TotalPages
- IADsPrintJob.get_TotalPages
- IADsPrintJob.UntilTime
- IADsPrintJob.get_UntilTime
- IADsPrintJob.User
- IADsPrintJob.get_User
- IADsPrintJob.UserPath
- IADsPrintJob.get_UserPath
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d1680484ff16d563ef5bc89de6d5abbfec2ce6a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478119"
---
# <a name="iadsprintjob-property-methods"></a><span data-ttu-id="66c33-105">Metodi di proprietà IADsPrintJob</span><span class="sxs-lookup"><span data-stu-id="66c33-105">IADsPrintJob Property Methods</span></span>

<span data-ttu-id="66c33-106">I metodi di proprietà per l'interfaccia [**IADsPrintJob**](/windows/desktop/api/Iads/nn-iads-iadsprintjob) ottengono o impostano le proprietà descritte nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="66c33-106">Property methods for the [**IADsPrintJob**](/windows/desktop/api/Iads/nn-iads-iadsprintjob) interface get or set the properties described in the following table.</span></span> <span data-ttu-id="66c33-107">Per altre informazioni, vedere [metodi della proprietà di interfaccia](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="66c33-107">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="66c33-108">Proprietà</span><span class="sxs-lookup"><span data-stu-id="66c33-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="66c33-109">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="66c33-109">**Description**</span></span>
<span data-ttu-id="66c33-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="66c33-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="66c33-111">Descrizione del processo di stampa.</span><span class="sxs-lookup"><span data-stu-id="66c33-111">The description of the print job.</span></span>

<dt>

<span data-ttu-id="66c33-112">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="66c33-112">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="66c33-113">Tipo di dati di scripting: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="66c33-113">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Description(
  [out] BSTR* pbstrDescription
);
HRESULT put_Description(
  [in] BSTR bstrDescription
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="66c33-114">**HostPrintQueue**</span><span class="sxs-lookup"><span data-stu-id="66c33-114">**HostPrintQueue**</span></span>
<span data-ttu-id="66c33-115"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="66c33-115"></dt> <dd> <dl></span></span>

<span data-ttu-id="66c33-116">Stringa ADsPath della coda di stampa che elabora il processo di stampa.</span><span class="sxs-lookup"><span data-stu-id="66c33-116">The ADsPath string of the Print Queue that processes the print job.</span></span>

<dt>

<span data-ttu-id="66c33-117">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="66c33-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="66c33-118">Tipo di dati di scripting: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="66c33-118">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_HostPrintQueue(
  [out] BSTR* pbstrHostPrintQueue
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="66c33-119">**Notificare**</span><span class="sxs-lookup"><span data-stu-id="66c33-119">**Notify**</span></span>
<span data-ttu-id="66c33-120"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="66c33-120"></dt> <dd> <dl></span></span>

<span data-ttu-id="66c33-121">Utente a cui inviare una notifica quando il processo viene completato.</span><span class="sxs-lookup"><span data-stu-id="66c33-121">The user to be notified when job is completed.</span></span>

<dt>

<span data-ttu-id="66c33-122">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="66c33-122">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="66c33-123">Tipo di dati di scripting: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="66c33-123">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Notify(
  [out] BSTR* pbstrNotify
);
HRESULT put_Notify(
  [in] BSTR bstrNotify
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="66c33-124">**NotifyPath**</span><span class="sxs-lookup"><span data-stu-id="66c33-124">**NotifyPath**</span></span>
<span data-ttu-id="66c33-125"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="66c33-125"></dt> <dd> <dl></span></span>

<span data-ttu-id="66c33-126">Stringa ADsPath dell'oggetto utente a cui inviare una notifica al termine del processo di stampa.</span><span class="sxs-lookup"><span data-stu-id="66c33-126">The ADsPath string of the user object to be notified when the print job is completed.</span></span>

<dt>

<span data-ttu-id="66c33-127">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="66c33-127">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="66c33-128">Tipo di dati di scripting: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="66c33-128">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_NotifyPath(
  [out] BSTR* pbstrNotifyPath
);
HRESULT put_NotifyPath(
  [in] BSTR bstrNotifyPath
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="66c33-129">**Priorità**</span><span class="sxs-lookup"><span data-stu-id="66c33-129">**Priority**</span></span>
<span data-ttu-id="66c33-130"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="66c33-130"></dt> <dd> <dl></span></span>

<span data-ttu-id="66c33-131">Priorità del processo di stampa.</span><span class="sxs-lookup"><span data-stu-id="66c33-131">The priority of the print job.</span></span>

<dt>

<span data-ttu-id="66c33-132">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="66c33-132">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="66c33-133">Tipo di dati di scripting: **Long**</span><span class="sxs-lookup"><span data-stu-id="66c33-133">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Priority(
  [out] LONG* plPriority
);
HRESULT put_Priority(
  [in] LONG lPriority
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="66c33-134">**Dimensioni**</span><span class="sxs-lookup"><span data-stu-id="66c33-134">**Size**</span></span>
<span data-ttu-id="66c33-135"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="66c33-135"></dt> <dd> <dl></span></span>

<span data-ttu-id="66c33-136">Dimensione, in byte, del processo di stampa.</span><span class="sxs-lookup"><span data-stu-id="66c33-136">The size, in bytes, of the print job.</span></span>

<dt>

<span data-ttu-id="66c33-137">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="66c33-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="66c33-138">Tipo di dati di scripting: **Long**</span><span class="sxs-lookup"><span data-stu-id="66c33-138">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Size(
  [out] LONG* plSize
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="66c33-139">**StartTime**</span><span class="sxs-lookup"><span data-stu-id="66c33-139">**StartTime**</span></span>
<span data-ttu-id="66c33-140"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="66c33-140"></dt> <dd> <dl></span></span>

<span data-ttu-id="66c33-141">La prima volta che il processo di stampa deve essere avviato.</span><span class="sxs-lookup"><span data-stu-id="66c33-141">The earliest time when the print job should be started.</span></span>

<dt>

<span data-ttu-id="66c33-142">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="66c33-142">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="66c33-143">Tipo di dati di scripting: **date**</span><span class="sxs-lookup"><span data-stu-id="66c33-143">Scripting data type: **DATE**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_StartTime(
  [out] DATE* pdateStartTime
);
HRESULT put_StartTime(
  [in] DATE dateStartTime
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="66c33-144">**TimeSubmitted**</span><span class="sxs-lookup"><span data-stu-id="66c33-144">**TimeSubmitted**</span></span>
<span data-ttu-id="66c33-145"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="66c33-145"></dt> <dd> <dl></span></span>

<span data-ttu-id="66c33-146">Ora in cui il processo è stato inviato alla coda.</span><span class="sxs-lookup"><span data-stu-id="66c33-146">The time when the job was submitted to the queue.</span></span>

<dt>

<span data-ttu-id="66c33-147">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="66c33-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="66c33-148">Tipo di dati di scripting: **date**</span><span class="sxs-lookup"><span data-stu-id="66c33-148">Scripting data type: **DATE**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_TimeSubmitted(
  [out] DATE* pdateTimeSubmitted
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="66c33-149">**TotalPages**</span><span class="sxs-lookup"><span data-stu-id="66c33-149">**TotalPages**</span></span>
<span data-ttu-id="66c33-150"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="66c33-150"></dt> <dd> <dl></span></span>

<span data-ttu-id="66c33-151">Numero totale di pagine nel processo di stampa.</span><span class="sxs-lookup"><span data-stu-id="66c33-151">The total number of pages in the print job.</span></span>

<dt>

<span data-ttu-id="66c33-152">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="66c33-152">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="66c33-153">Tipo di dati di scripting: **Long**</span><span class="sxs-lookup"><span data-stu-id="66c33-153">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_TotalPages(
  [out] LONG* plTotalPages
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="66c33-154">**UntilTime**</span><span class="sxs-lookup"><span data-stu-id="66c33-154">**UntilTime**</span></span>
<span data-ttu-id="66c33-155"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="66c33-155"></dt> <dd> <dl></span></span>

<span data-ttu-id="66c33-156">Data e ora dell'ultimo avvio del processo di stampa.</span><span class="sxs-lookup"><span data-stu-id="66c33-156">The latest time when the print job should be started.</span></span>

<dt>

<span data-ttu-id="66c33-157">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="66c33-157">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="66c33-158">Tipo di dati di scripting: **date**</span><span class="sxs-lookup"><span data-stu-id="66c33-158">Scripting data type: **DATE**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_UntilTime(
  [out] DATE* pdateUntilTime
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="66c33-159">**Utente**</span><span class="sxs-lookup"><span data-stu-id="66c33-159">**User**</span></span>
<span data-ttu-id="66c33-160"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="66c33-160"></dt> <dd> <dl></span></span>

<span data-ttu-id="66c33-161">Nome dell'utente che ha inviato il processo di stampa.</span><span class="sxs-lookup"><span data-stu-id="66c33-161">The name of user who submitted the print job.</span></span>

<dt>

<span data-ttu-id="66c33-162">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="66c33-162">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="66c33-163">Tipo di dati di scripting: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="66c33-163">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_User(
  [out] BSTR* pbstrUser
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="66c33-164">**UserPath**</span><span class="sxs-lookup"><span data-stu-id="66c33-164">**UserPath**</span></span>
<span data-ttu-id="66c33-165"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="66c33-165"></dt> <dd> <dl></span></span>

<span data-ttu-id="66c33-166">Stringa ADsPath dell'oggetto utente che ha inviato il processo di stampa.</span><span class="sxs-lookup"><span data-stu-id="66c33-166">The ADsPath string of the user object that submitted this print job.</span></span>

<dt>

<span data-ttu-id="66c33-167">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="66c33-167">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="66c33-168">Tipo di dati di scripting: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="66c33-168">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_UserPath(
  [out] BSTR* pbstrUserPath
);
```


</dt> </dl> </dd> </dl>

 

## <a name="examples"></a><span data-ttu-id="66c33-169">Esempio</span><span class="sxs-lookup"><span data-stu-id="66c33-169">Examples</span></span>

<span data-ttu-id="66c33-170">Nell'esempio di codice riportato di seguito viene illustrato come utilizzare le proprietà di un oggetto processo di stampa.</span><span class="sxs-lookup"><span data-stu-id="66c33-170">The following code example shows how to work with properties of a print job object.</span></span>


```VB
Dim pqo As IADsPrintQueueOperations
Dim pj As IADsPrintJob
On Error GoTo Cleanup

Set pqo = GetObject("WinNT://aMachine/aPrinter")
For Each pj In pqo.PrintJobs
    MsgBox "Host Printer: " & pj.HostPrintQueue
    MsgBox "Job description: " & pj.Description
    MsgBox "job requester: " & pj.User 
Next

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set pqo = Nothing
    Set pj = Nothing
```



<span data-ttu-id="66c33-171">Nell'esempio di codice riportato di seguito viene illustrato come utilizzare le proprietà di un oggetto processo di stampa.</span><span class="sxs-lookup"><span data-stu-id="66c33-171">The following code example shows how to work with properties of a print job object.</span></span>


```C++
IADsPrintQueueOperations *pqo = NULL;
IADsPrintJob *pJob = NULL;
HRESULT hr = S_OK;
BSTR bstr = NULL;
VARIANT var;
ULONG lFetch = 0;
IDispatch *pDisp = NULL;
IADsCollection *pColl = NULL;
IUnknown *pUnk = NULL;
LPWSTR adsPath =L"WinNT://aMachine/aPrinter";

VariantInit(&var);

hr = ADsGetObject(adsPath, 
                  IID_IADsPrintQueueOperations, 
                  (void**)&pqo);
if(FAILED(hr)){goto Cleanup;}


hr = pqo->PrintJobs(&pColl);

// Enumerate print jobs. Code omitted.

hr = pColl->get__NewEnum(&pUnk);
if(FAILED(hr)){goto Cleanup;}


IEnumVARIANT *pEnum;
hr = pUnk->QueryInterface(IID_IEnumVARIANT,(void**)&pEnum);
if(FAILED(hr)){goto Cleanup;}


// Now Enumerate.
hr = pEnum->Next(1, &var, &lFetch);
if(FAILED(hr)){goto Cleanup;}

while(hr == S_OK)
{
    if (lFetch == 1)    
    {
        pDisp = V_DISPATCH(&var);
        pDisp->QueryInterface(IID_IADsPrintJob, (void**)&pJob);

        pJob->get_HostPrintQueue(&bstr);
        printf("HostPrintQueue: %S\n",bstr);
        SysFreeString(bstr);

        pJob->get_Description(&bstr);
        printf("Print job name: %S\n",bstr);
        SysFreeString(bstr);

        pJob->get_User(&bstr);
        printf("Requester: %S\n",bstr);
        SysFreeString(bstr);

        pJob->Release();
    }
    pDisp->Release();
    VariantClear(&var);
    hr = pEnum->Next(1, &var, &lFetch);
};

Cleanup:
    if(pEnum) pEnum->Release();
    if(pUnk) pUnk->Release();
    if(pColl) pColl->Release();
    if(pqo) pqo->Release();
```



## <a name="requirements"></a><span data-ttu-id="66c33-172">Requisiti</span><span class="sxs-lookup"><span data-stu-id="66c33-172">Requirements</span></span>



| <span data-ttu-id="66c33-173">Requisito</span><span class="sxs-lookup"><span data-stu-id="66c33-173">Requirement</span></span> | <span data-ttu-id="66c33-174">Valore</span><span class="sxs-lookup"><span data-stu-id="66c33-174">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="66c33-175">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="66c33-175">Minimum supported client</span></span><br/> | <span data-ttu-id="66c33-176">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="66c33-176">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="66c33-177">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="66c33-177">Minimum supported server</span></span><br/> | <span data-ttu-id="66c33-178">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="66c33-178">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="66c33-179">Intestazione</span><span class="sxs-lookup"><span data-stu-id="66c33-179">Header</span></span><br/>                   | <dl> <span data-ttu-id="66c33-180"><dt>IADs. h</dt></span><span class="sxs-lookup"><span data-stu-id="66c33-180"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="66c33-181">DLL</span><span class="sxs-lookup"><span data-stu-id="66c33-181">DLL</span></span><br/>                      | <dl> <span data-ttu-id="66c33-182"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="66c33-182"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="66c33-183">IID</span><span class="sxs-lookup"><span data-stu-id="66c33-183">IID</span></span><br/>                      | <span data-ttu-id="66c33-184">IID \_ IADsPrintJob è definito come 32FB6780-1ED0-11CF-a988-00AA006BC149</span><span class="sxs-lookup"><span data-stu-id="66c33-184">IID\_IADsPrintJob is defined as 32FB6780-1ED0-11CF-A988-00AA006BC149</span></span><br/>         |



## <a name="see-also"></a><span data-ttu-id="66c33-185">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="66c33-185">See also</span></span>

<dl> <dt>

[<span data-ttu-id="66c33-186">**IADsPrintJob**</span><span class="sxs-lookup"><span data-stu-id="66c33-186">**IADsPrintJob**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsprintjob)
</dt> <dt>

[<span data-ttu-id="66c33-187">Metodi di proprietà dell'interfaccia</span><span class="sxs-lookup"><span data-stu-id="66c33-187">Interface Property Methods</span></span>](interface-property-methods.md)
</dt> </dl>

 

 






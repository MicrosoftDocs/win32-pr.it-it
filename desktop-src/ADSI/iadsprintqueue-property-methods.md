---
title: Metodi di proprietà IADsPrintQueue (IADs. h)
description: I metodi di proprietà dell'interfaccia IADsPrintQueue ottengono o impostano le proprietà descritte nella tabella seguente. Per altre informazioni, vedere Metodi della proprietà di interfaccia.
ms.assetid: 7f5b4200-65c8-4230-8561-ad4fefb391f3
ms.tgt_platform: multiple
keywords:
- Metodi di proprietà IADsPrintQueue ADSI
topic_type:
- apiref
api_name:
- IADsPrintQueue Property Methods
- IADsPrintQueue.BannerPage
- IADsPrintQueue.get_BannerPage
- IADsPrintQueue.put_BannerPage
- IADsPrintQueue.Datatype
- IADsPrintQueue.get_Datatype
- IADsPrintQueue.put_Datatype
- IADsPrintQueue.DefaultJobPriority
- IADsPrintQueue.get_DefaultJobPriority
- IADsPrintQueue.put_DefaultJobPriority
- IADsPrintQueue.Description
- IADsPrintQueue.get_Description
- IADsPrintQueue.put_Description
- IADsPrintQueue.HostComputer
- IADsPrintQueue.get_HostComputer
- IADsPrintQueue.put_HostComputer
- IADsPrintQueue.Location
- IADsPrintQueue.get_Location
- IADsPrintQueue.put_Location
- IADsPrintQueue.Model
- IADsPrintQueue.get_Model
- IADsPrintQueue.put_Model
- IADsPrintQueue.PrintDevices
- IADsPrintQueue.get_PrintDevices
- IADsPrintQueue.put_PrintDevices
- IADsPrintQueue.PrinterPath
- IADsPrintQueue.get_PrinterPath
- IADsPrintQueue.put_PrinterPath
- IADsPrintQueue.PrintProcessor
- IADsPrintQueue.get_PrintProcessor
- IADsPrintQueue.put_PrintProcessor
- IADsPrintQueue.Priority
- IADsPrintQueue.get_Priority
- IADsPrintQueue.put_Priority
- IADsPrintQueue.StartTime
- IADsPrintQueue.get_StartTime
- IADsPrintQueue.put_StartTime
- IADsPrintQueue.UntilTime
- IADsPrintQueue.get_UntilTime
- IADsPrintQueue.put_UntilTime
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e8b7b2260805dbf5fa144f239111b6e29f5ec78
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104225221"
---
# <a name="iadsprintqueue-property-methods"></a><span data-ttu-id="943e5-105">Metodi di proprietà IADsPrintQueue</span><span class="sxs-lookup"><span data-stu-id="943e5-105">IADsPrintQueue Property Methods</span></span>

<span data-ttu-id="943e5-106">I metodi di proprietà dell'interfaccia [**IADsPrintQueue**](/windows/desktop/api/Iads/nn-iads-iadsprintqueue) ottengono o impostano le proprietà descritte nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="943e5-106">The property methods of the [**IADsPrintQueue**](/windows/desktop/api/Iads/nn-iads-iadsprintqueue) interface get or set the properties described in the following table.</span></span> <span data-ttu-id="943e5-107">Per altre informazioni, vedere [metodi della proprietà di interfaccia](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="943e5-107">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="943e5-108">Proprietà</span><span class="sxs-lookup"><span data-stu-id="943e5-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="943e5-109">**BannerPage**</span><span class="sxs-lookup"><span data-stu-id="943e5-109">**BannerPage**</span></span>
<span data-ttu-id="943e5-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="943e5-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="943e5-111">Percorso file system che punta alla pagina del banner utilizzata per separare i processi di stampa.</span><span class="sxs-lookup"><span data-stu-id="943e5-111">The file system path that points to the banner page used to separate print jobs.</span></span> <span data-ttu-id="943e5-112">Se è **null**, non viene utilizzata alcuna pagina di intestazione.</span><span class="sxs-lookup"><span data-stu-id="943e5-112">If **NULL**, no banner page is used.</span></span>

<dt>

<span data-ttu-id="943e5-113">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="943e5-113">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="943e5-114">Tipo di dati di scripting: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="943e5-114">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_BannerPage(
  [out] BSTR* pbstrBannerPage
);
HRESULT put_BannerPage(
  [in] BSTR bstrBannerPage
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="943e5-115">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="943e5-115">**Datatype**</span></span>
<span data-ttu-id="943e5-116"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="943e5-116"></dt> <dd> <dl></span></span>

<span data-ttu-id="943e5-117">Tipo di dati che può essere elaborato da questa coda.</span><span class="sxs-lookup"><span data-stu-id="943e5-117">The data type that can be processed by this queue.</span></span>

<dt>

<span data-ttu-id="943e5-118">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="943e5-118">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="943e5-119">Tipo di dati di scripting: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="943e5-119">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Datatype(
  [out] BSTR* pbstrDatatype
);
HRESULT put_Datatype(
  [in] BSTR bstrDatatype
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="943e5-120">**DefaultJobPriority**</span><span class="sxs-lookup"><span data-stu-id="943e5-120">**DefaultJobPriority**</span></span>
<span data-ttu-id="943e5-121"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="943e5-121"></dt> <dd> <dl></span></span>

<span data-ttu-id="943e5-122">Priorità predefinita assegnata a ogni processo di stampa.</span><span class="sxs-lookup"><span data-stu-id="943e5-122">The default priority assigned to each print job.</span></span>

<dt>

<span data-ttu-id="943e5-123">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="943e5-123">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="943e5-124">Tipo di dati di scripting: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="943e5-124">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_DefaultJobPriority(
  [out] LONG* plDefaultJobPriority
);
HRESULT put_DefaultJobPriority(
  [in] BSTR lDefaultJobPriority
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="943e5-125">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="943e5-125">**Description**</span></span>
<span data-ttu-id="943e5-126"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="943e5-126"></dt> <dd> <dl></span></span>

<span data-ttu-id="943e5-127">Descrizione testuale della coda di stampa.</span><span class="sxs-lookup"><span data-stu-id="943e5-127">The text description of this print queue.</span></span>

<dt>

<span data-ttu-id="943e5-128">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="943e5-128">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="943e5-129">Tipo di dati di scripting: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="943e5-129">Scripting data type: **BSTR**</span></span>
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

<span data-ttu-id="943e5-130">**HostComputer**</span><span class="sxs-lookup"><span data-stu-id="943e5-130">**HostComputer**</span></span>
<span data-ttu-id="943e5-131"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="943e5-131"></dt> <dd> <dl></span></span>

<span data-ttu-id="943e5-132">Stringa ADsPath che fa riferimento al computer host.</span><span class="sxs-lookup"><span data-stu-id="943e5-132">The ADsPath string that references the host computer.</span></span>

<dt>

<span data-ttu-id="943e5-133">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="943e5-133">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="943e5-134">Tipo di dati di scripting: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="943e5-134">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_HostComputer(
  [out] BSTR* pbstrHostComputer
);
HRESULT put_HostComputer(
  [in] BSTR bstrHostComputer
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="943e5-135">**Posizione**</span><span class="sxs-lookup"><span data-stu-id="943e5-135">**Location**</span></span>
<span data-ttu-id="943e5-136"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="943e5-136"></dt> <dd> <dl></span></span>

<span data-ttu-id="943e5-137">Percorso della coda come descritto da un amministratore.</span><span class="sxs-lookup"><span data-stu-id="943e5-137">The location of the queue as described by an administrator.</span></span>

<dt>

<span data-ttu-id="943e5-138">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="943e5-138">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="943e5-139">Tipo di dati di scripting: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="943e5-139">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Location(
  [out] BSTR* pbstrLocation
);
HRESULT put_Location(
  [in] BSTR bstrLocation
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="943e5-140">**Modello**</span><span class="sxs-lookup"><span data-stu-id="943e5-140">**Model**</span></span>
<span data-ttu-id="943e5-141"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="943e5-141"></dt> <dd> <dl></span></span>

<span data-ttu-id="943e5-142">Nome del driver utilizzato da questa coda di stampa.</span><span class="sxs-lookup"><span data-stu-id="943e5-142">The name of the driver used by this print queue.</span></span>

<dt>

<span data-ttu-id="943e5-143">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="943e5-143">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="943e5-144">Tipo di dati di scripting: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="943e5-144">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Model(
  [out] BSTR* pbstrModel
);
HRESULT put_Model(
  [in] BSTR bstrModel
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="943e5-145">**PrintDevices**</span><span class="sxs-lookup"><span data-stu-id="943e5-145">**PrintDevices**</span></span>
<span data-ttu-id="943e5-146"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="943e5-146"></dt> <dd> <dl></span></span>

<span data-ttu-id="943e5-147">SAFEARRAY di **BSTR** che contiene i nomi dei dispositivi di stampa in cui questa coda di stampa consente di eseguire lo spooling dei processi.</span><span class="sxs-lookup"><span data-stu-id="943e5-147">A SAFEARRAY of **BSTR** that contains the names of the print devices to which this print queue spools jobs.</span></span>

<dt>

<span data-ttu-id="943e5-148">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="943e5-148">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="943e5-149">Tipo di dati di scripting: **Variant**</span><span class="sxs-lookup"><span data-stu-id="943e5-149">Scripting data type: **VARIANT**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_PrintDevices(
  [out] VARIANT* pvPrintDevices
);
HRESULT put_PrintDevices(
  [in] VARIANT vPrintDevices
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="943e5-150">**PrinterPath**</span><span class="sxs-lookup"><span data-stu-id="943e5-150">**PrinterPath**</span></span>
<span data-ttu-id="943e5-151"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="943e5-151"></dt> <dd> <dl></span></span>

<span data-ttu-id="943e5-152">Stringa che fa riferimento al percorso mediante il quale è possibile accedere a una stampante condivisa.</span><span class="sxs-lookup"><span data-stu-id="943e5-152">The string that references the path by which a shared printer can be accessed.</span></span>

<dt>

<span data-ttu-id="943e5-153">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="943e5-153">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="943e5-154">Tipo di dati di scripting: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="943e5-154">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_PrinterPath(
  [out] BSTR* pbstrPrinterPath
);
HRESULT put_PrinterPath(
  [in] BSTR bstrPrinterPath
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="943e5-155">**PrintProcessor**</span><span class="sxs-lookup"><span data-stu-id="943e5-155">**PrintProcessor**</span></span>
<span data-ttu-id="943e5-156"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="943e5-156"></dt> <dd> <dl></span></span>

<span data-ttu-id="943e5-157">Processore di stampa associato a questa coda.</span><span class="sxs-lookup"><span data-stu-id="943e5-157">The print processor associated with this queue.</span></span>

<dt>

<span data-ttu-id="943e5-158">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="943e5-158">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="943e5-159">Tipo di dati di scripting: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="943e5-159">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_PrintProcessor(
  [out] BSTR* pbstrPrintProcessor
);
HRESULT put_PrintProcessor(
  [in] BSTR bstrPrintProcessor
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="943e5-160">**Priorità**</span><span class="sxs-lookup"><span data-stu-id="943e5-160">**Priority**</span></span>
<span data-ttu-id="943e5-161"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="943e5-161"></dt> <dd> <dl></span></span>

<span data-ttu-id="943e5-162">Priorità della coda di processi dell'oggetto Printer per tutti i dispositivi connessi.</span><span class="sxs-lookup"><span data-stu-id="943e5-162">The priority of this printer object job queue for any connected devices.</span></span> <span data-ttu-id="943e5-163">Verranno elaborati per primi tutti i processi con priorità più alta.</span><span class="sxs-lookup"><span data-stu-id="943e5-163">All jobs in higher priority print queue objects will be processed first.</span></span>

<dt>

<span data-ttu-id="943e5-164">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="943e5-164">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="943e5-165">Tipo di dati di scripting: **Long**</span><span class="sxs-lookup"><span data-stu-id="943e5-165">Scripting data type: **LONG**</span></span>
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

<span data-ttu-id="943e5-166">**StartTime**</span><span class="sxs-lookup"><span data-stu-id="943e5-166">**StartTime**</span></span>
<span data-ttu-id="943e5-167"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="943e5-167"></dt> <dd> <dl></span></span>

<span data-ttu-id="943e5-168">Ora di inizio dell'elaborazione dei processi da parte della coda.</span><span class="sxs-lookup"><span data-stu-id="943e5-168">The time when the queue should begin processing jobs.</span></span> <span data-ttu-id="943e5-169">La parte relativa alla data dell'ora viene ignorata.</span><span class="sxs-lookup"><span data-stu-id="943e5-169">The date portion of the time is ignored.</span></span>

<dt>

<span data-ttu-id="943e5-170">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="943e5-170">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="943e5-171">Tipo di dati di scripting: **date**</span><span class="sxs-lookup"><span data-stu-id="943e5-171">Scripting data type: **DATE**</span></span>
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

<span data-ttu-id="943e5-172">**UntilTime**</span><span class="sxs-lookup"><span data-stu-id="943e5-172">**UntilTime**</span></span>
<span data-ttu-id="943e5-173"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="943e5-173"></dt> <dd> <dl></span></span>

<span data-ttu-id="943e5-174">Data e ora in cui la coda deve arrestare l'elaborazione dei processi.</span><span class="sxs-lookup"><span data-stu-id="943e5-174">The time when the queue should stop processing jobs.</span></span>

<dt>

<span data-ttu-id="943e5-175">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="943e5-175">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="943e5-176">Tipo di dati di scripting: **date**</span><span class="sxs-lookup"><span data-stu-id="943e5-176">Scripting data type: **DATE**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_UntilTime(
  [out] DATE* pdateUntilTime
);
HRESULT put_UntilTime(
  [in] DATE dateUntilTime
);
```


</dt> </dl> </dd> </dl>

 

## <a name="examples"></a><span data-ttu-id="943e5-177">Esempio</span><span class="sxs-lookup"><span data-stu-id="943e5-177">Examples</span></span>

<span data-ttu-id="943e5-178">Nell'esempio di codice seguente viene illustrato come determinare se una stampante specificata è online o offline.</span><span class="sxs-lookup"><span data-stu-id="943e5-178">The following code example shows how to determine if a specified printer is online or offline.</span></span>


```VB
Dim pq As IADsPrintQueue
Dim pqo As IADsPrintQueueOperations
On Error GoTo Cleanup
 
Set pq = GetObject("WinNT://aMachine/aPrinter")
Set pqo = pq
If pqo.status = ADS_PRINTER_OFFLINE Then
    MsgBox pq.Model & "@" & pq.Location & is offline."
Else
    MsgBox pq.Model & "@" & pq.Location & is online."
End If

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set pq = Nothing
    Set pqo = Nothing
```



<span data-ttu-id="943e5-179">Nell'esempio di codice seguente viene illustrato come determinare se una stampante specificata è online o offline.</span><span class="sxs-lookup"><span data-stu-id="943e5-179">The following code example shows how to determine if a specified printer is online or offline.</span></span>


```C++
IADsPrintQueue *pq = NULL;
HRESULT hr = S_OK;
IADsPrintQueueOperations *pqo = NULL;
BSTR model = NULL;
BSTR location = NULL;

LPWSTR adsPath = L"WinNT://aMachine/aPrinter";
hr = ADsGetObject(adsPath,
                  IID_IADsPrintQueue,
                  (void**)&pq);
if(FAILED(hr)) {goto Cleanup;}


hr = pq->QueryInterface(IID_IADsPrintQueueOperations,(void**)&pqo);
if(FAILED(hr)) {goto Cleanup;}

long status;
hr = pqo->get_Status(&status);
if(FAILED(hr)) {goto Cleanup;}

hr = pq->get_Model(&model);
if(FAILED(hr)) {goto Cleanup;}

hr =pq->get_Location(&location);
if(FAILED(hr)) {goto Cleanup;}

if(status == ADS_PRINTER_OFFLINE) 
{
    printf("%S @ %S is offline.\n",model,location);
} 
else 
{
    printf("%S @ %S is online.\n",model,location);
}


Cleanup:
    SysFreeString(model);
    SysFreeString(location);
    if(pq) pq->Release();
    if(pqo) pqo->Release();
```



## <a name="requirements"></a><span data-ttu-id="943e5-180">Requisiti</span><span class="sxs-lookup"><span data-stu-id="943e5-180">Requirements</span></span>



| <span data-ttu-id="943e5-181">Requisito</span><span class="sxs-lookup"><span data-stu-id="943e5-181">Requirement</span></span> | <span data-ttu-id="943e5-182">Valore</span><span class="sxs-lookup"><span data-stu-id="943e5-182">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="943e5-183">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="943e5-183">Minimum supported client</span></span><br/> | <span data-ttu-id="943e5-184">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="943e5-184">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="943e5-185">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="943e5-185">Minimum supported server</span></span><br/> | <span data-ttu-id="943e5-186">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="943e5-186">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="943e5-187">Intestazione</span><span class="sxs-lookup"><span data-stu-id="943e5-187">Header</span></span><br/>                   | <dl> <span data-ttu-id="943e5-188"><dt>IADs. h</dt></span><span class="sxs-lookup"><span data-stu-id="943e5-188"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="943e5-189">DLL</span><span class="sxs-lookup"><span data-stu-id="943e5-189">DLL</span></span><br/>                      | <dl> <span data-ttu-id="943e5-190"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="943e5-190"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="943e5-191">IID</span><span class="sxs-lookup"><span data-stu-id="943e5-191">IID</span></span><br/>                      | <span data-ttu-id="943e5-192">IID \_ IADsPrintQueue è definito come B15160D0-1226-11CF-A985-00AA006BC149</span><span class="sxs-lookup"><span data-stu-id="943e5-192">IID\_IADsPrintQueue is defined as B15160D0-1226-11CF-A985-00AA006BC149</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="943e5-193">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="943e5-193">See also</span></span>

<dl> <dt>

[<span data-ttu-id="943e5-194">**IADsPrintQueue**</span><span class="sxs-lookup"><span data-stu-id="943e5-194">**IADsPrintQueue**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsprintqueue)
</dt> <dt>

[<span data-ttu-id="943e5-195">Metodi di proprietà dell'interfaccia</span><span class="sxs-lookup"><span data-stu-id="943e5-195">Interface Property Methods</span></span>](interface-property-methods.md)
</dt> </dl>

 

 






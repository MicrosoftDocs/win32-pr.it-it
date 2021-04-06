---
title: Metodi di proprietà IADsServiceOperations (IADs. h)
description: I metodi di proprietà dell'interfaccia IADsServiceOperations leggono e scrivono le proprietà descritte nell'elenco seguente. Per ulteriori informazioni sui metodi di proprietà, vedere Metodi della proprietà di interfaccia.
ms.assetid: ebddfc42-1d2f-495b-b57c-f57419b54ff8
ms.tgt_platform: multiple
keywords:
- Metodi di proprietà IADsServiceOperations ADSI
topic_type:
- apiref
api_name:
- IADsServiceOperations Property Methods
- IADsServiceOperations.Status
- IADsServiceOperations.get_Status
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 654a92be1052d4e4c70e0274d719a49be965d8cb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873670"
---
# <a name="iadsserviceoperations-property-methods"></a><span data-ttu-id="ad14b-105">Metodi di proprietà IADsServiceOperations</span><span class="sxs-lookup"><span data-stu-id="ad14b-105">IADsServiceOperations Property Methods</span></span>

<span data-ttu-id="ad14b-106">I metodi di proprietà dell'interfaccia [**IADsServiceOperations**](/windows/desktop/api/Iads/nn-iads-iadsserviceoperations) leggono e scrivono le proprietà descritte nell'elenco seguente.</span><span class="sxs-lookup"><span data-stu-id="ad14b-106">The property methods of the [**IADsServiceOperations**](/windows/desktop/api/Iads/nn-iads-iadsserviceoperations) interface read and write the properties described in the following list.</span></span> <span data-ttu-id="ad14b-107">Per ulteriori informazioni sui metodi di proprietà, vedere [metodi della proprietà di interfaccia](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="ad14b-107">For more information about property methods, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="ad14b-108">Proprietà</span><span class="sxs-lookup"><span data-stu-id="ad14b-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="ad14b-109">**Status**</span><span class="sxs-lookup"><span data-stu-id="ad14b-109">**Status**</span></span>
<span data-ttu-id="ad14b-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="ad14b-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="ad14b-111">Stato del servizio.</span><span class="sxs-lookup"><span data-stu-id="ad14b-111">Status of service.</span></span>

<span data-ttu-id="ad14b-112">Di seguito sono riportati i valori possibili.</span><span class="sxs-lookup"><span data-stu-id="ad14b-112">The following are possible values.</span></span>

<dt>

<span id="ADS_SERVICE_STOPPED"></span><span id="ads_service_stopped"></span>

<span data-ttu-id="ad14b-113">**Annunci \_ SERVIZIO \_ interrotto** (0x00000001)</span><span class="sxs-lookup"><span data-stu-id="ad14b-113">**ADS\_SERVICE\_STOPPED** (0x00000001)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_START_PENDING"></span><span id="ads_service_start_pending"></span>

<span data-ttu-id="ad14b-114">**Annunci \_ \_Avvio servizio \_ in sospeso** (0x00000002)</span><span class="sxs-lookup"><span data-stu-id="ad14b-114">**ADS\_SERVICE\_START\_PENDING** (0x00000002)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_STOP_PENDING"></span><span id="ads_service_stop_pending"></span>

<span data-ttu-id="ad14b-115">**Annunci \_ \_Arresto servizio \_ in sospeso** (0x00000003)</span><span class="sxs-lookup"><span data-stu-id="ad14b-115">**ADS\_SERVICE\_STOP\_PENDING** (0x00000003)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_RUNNING"></span><span id="ads_service_running"></span>

<span data-ttu-id="ad14b-116">**Annunci \_ SERVIZIO \_ in esecuzione** (0x00000004)</span><span class="sxs-lookup"><span data-stu-id="ad14b-116">**ADS\_SERVICE\_RUNNING** (0x00000004)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_CONTINUE_PENDING"></span><span id="ads_service_continue_pending"></span>

<span data-ttu-id="ad14b-117">**Annunci \_ \_Continuazione servizio \_ in sospeso** (0x00000005)</span><span class="sxs-lookup"><span data-stu-id="ad14b-117">**ADS\_SERVICE\_CONTINUE\_PENDING** (0x00000005)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_PAUSE_PENDING"></span><span id="ads_service_pause_pending"></span>

<span data-ttu-id="ad14b-118">**Annunci \_ \_Sospensione servizio \_ in sospeso** (0x00000006)</span><span class="sxs-lookup"><span data-stu-id="ad14b-118">**ADS\_SERVICE\_PAUSE\_PENDING** (0x00000006)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_PAUSED"></span><span id="ads_service_paused"></span>

<span data-ttu-id="ad14b-119">**Annunci \_ SERVIZIO \_ sospeso** (0x00000007)</span><span class="sxs-lookup"><span data-stu-id="ad14b-119">**ADS\_SERVICE\_PAUSED** (0x00000007)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_ERROR"></span><span id="ads_service_error"></span>

<span data-ttu-id="ad14b-120">**Annunci \_ \_Errore del servizio** (0x00000008)</span><span class="sxs-lookup"><span data-stu-id="ad14b-120">**ADS\_SERVICE\_ERROR** (0x00000008)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_OWN_PROCESS"></span><span id="ads_service_own_process"></span>

<span data-ttu-id="ad14b-121">**Annunci \_ \_ \_ Processo del servizio personalizzato** (0x00000010)</span><span class="sxs-lookup"><span data-stu-id="ad14b-121">**ADS\_SERVICE\_OWN\_PROCESS** (0x00000010)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_SHARE_PROCESS"></span><span id="ads_service_share_process"></span>

<span data-ttu-id="ad14b-122">**Annunci \_ \_ \_ Processo di condivisione del servizio** (0x00000020)</span><span class="sxs-lookup"><span data-stu-id="ad14b-122">**ADS\_SERVICE\_SHARE\_PROCESS** (0x00000020)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_KERNEL_DRIVER"></span><span id="ads_service_kernel_driver"></span>

<span data-ttu-id="ad14b-123">**Annunci \_ \_ \_ Driver del kernel del servizio** (0x00000001)</span><span class="sxs-lookup"><span data-stu-id="ad14b-123">**ADS\_SERVICE\_KERNEL\_DRIVER** (0x00000001)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_FILE_SYSTEM_DRIVER"></span><span id="ads_service_file_system_driver"></span>

<span data-ttu-id="ad14b-124">**Annunci \_ \_ \_ \_ Driver del file System di servizio** (0x00000002)</span><span class="sxs-lookup"><span data-stu-id="ad14b-124">**ADS\_SERVICE\_FILE\_SYSTEM\_DRIVER** (0x00000002)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_BOOT_START"></span><span id="ads_service_boot_start"></span>

<span data-ttu-id="ad14b-125">**Annunci \_ avvio \_ avvio \_ del servizio** (avvio avvio del servizio \_ \_ )</span><span class="sxs-lookup"><span data-stu-id="ad14b-125">**ADS\_SERVICE\_BOOT\_START** (SERVICE\_BOOT\_START)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_SYSTEM_START"></span><span id="ads_service_system_start"></span>

<span data-ttu-id="ad14b-126">**Annunci \_ \_ \_ avvio del sistema del servizio** (avvio del sistema del servizio \_ \_ )</span><span class="sxs-lookup"><span data-stu-id="ad14b-126">**ADS\_SERVICE\_SYSTEM\_START** (SERVICE\_SYSTEM\_START)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_AUTO_START"></span><span id="ads_service_auto_start"></span>

<span data-ttu-id="ad14b-127">**Annunci \_ \_ \_ avvio automatico servizio** ( \_ avvio automatico servizio \_ )</span><span class="sxs-lookup"><span data-stu-id="ad14b-127">**ADS\_SERVICE\_AUTO\_START** (SERVICE\_AUTO\_START)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_DEMAND_START"></span><span id="ads_service_demand_start"></span>

<span data-ttu-id="ad14b-128">**Annunci \_ \_ \_ avvio richiesta di servizio** ( \_ avvio richiesta servizio \_ )</span><span class="sxs-lookup"><span data-stu-id="ad14b-128">**ADS\_SERVICE\_DEMAND\_START** (SERVICE\_DEMAND\_START)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_DISABLED"></span><span id="ads_service_disabled"></span>

<span data-ttu-id="ad14b-129">**Annunci \_ SERVIZIO \_ disabilitato** (servizio \_ disabilitato)</span><span class="sxs-lookup"><span data-stu-id="ad14b-129">**ADS\_SERVICE\_DISABLED** (SERVICE\_DISABLED)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_ERROR_IGNORE"></span><span id="ads_service_error_ignore"></span>

<span data-ttu-id="ad14b-130">**Annunci \_ Errore del servizio \_ \_ ignorato** (0)</span><span class="sxs-lookup"><span data-stu-id="ad14b-130">**ADS\_SERVICE\_ERROR\_IGNORE** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_ERROR_NORMAL"></span><span id="ads_service_error_normal"></span>

<span data-ttu-id="ad14b-131">**Annunci \_ Errore del servizio \_ \_ normale** (1)</span><span class="sxs-lookup"><span data-stu-id="ad14b-131">**ADS\_SERVICE\_ERROR\_NORMAL** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_ERROR_SEVERE"></span><span id="ads_service_error_severe"></span>

<span data-ttu-id="ad14b-132">**Annunci \_ Errore del servizio \_ \_ grave** (2)</span><span class="sxs-lookup"><span data-stu-id="ad14b-132">**ADS\_SERVICE\_ERROR\_SEVERE** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_ERROR_CRITICAL"></span><span id="ads_service_error_critical"></span>

<span data-ttu-id="ad14b-133">**Annunci \_ Errore del servizio \_ \_ critico** (3)</span><span class="sxs-lookup"><span data-stu-id="ad14b-133">**ADS\_SERVICE\_ERROR\_CRITICAL** (3)</span></span>


</dt> <dd></dd> </dl> <dt>

<span data-ttu-id="ad14b-134">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ad14b-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ad14b-135">Tipo di dati di scripting: **Long**</span><span class="sxs-lookup"><span data-stu-id="ad14b-135">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Status(
  [out] LONG* pstatus
);
```


</dt> </dl> </dd> </dl>

 

## <a name="examples"></a><span data-ttu-id="ad14b-136">Esempio</span><span class="sxs-lookup"><span data-stu-id="ad14b-136">Examples</span></span>

<span data-ttu-id="ad14b-137">Nell'esempio di codice riportato di seguito viene illustrato come verificare lo stato di un servizio fax Microsoft in esecuzione in Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="ad14b-137">The following code example shows how to verify the status of a Microsoft Fax Service running on Windows 2000.</span></span>


```VB
Dim cp As IADsComputer
Dim sr As IADsService
Dim so As IADsServiceOperations
On Error GoTo Cleanup

Set cp = GetObject("WinNT://myMachine,computer")
Set sr = cp.GetObject("Service", "Fax")
Set so = sr

Select Case so.Status
    Case ADS_SERVICE_STOPPED
        MsgBox "Microsoft Fax Service has stopped."
    Case ADS_SERVICE_RUNNING
        MsgBox "Microsoft Fax Service is running."
    Case ADS_SERVICE_PAUSED
        MsgBox "Microsoft Fax Service has paused."
    Case ADS_SERVICE_ERROR
        MsgBox "Microsoft Fax Service has errors."
End Select

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set cp = Nothing
    Set sr = Nothing
    Set so = Nothing
```



<span data-ttu-id="ad14b-138">Nell'esempio di codice seguente viene verificato lo stato di un servizio fax Microsoft in esecuzione in Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="ad14b-138">The following code example verifies the status of a Microsoft Fax Service running on Windows 2000.</span></span>


```C++
IADsContainer *pCont = NULL;
IADsServiceOperations *pSrvOp = NULL;
LPWSTR adsPath = L"WinNT://myMachine,computer";
IDispatch *pDisp = NULL;
long status = 0;

HRESULT hr = S_OK;

hr = ADsGetObject(adsPath,IID_IADsContainer,(void**)&pCont);
if(FAILED(hr)) {goto Cleanup;}

hr = pCont->GetObject(CComBSTR("Service"), CComBSTR("Fax"), &pDisp);
if(FAILED(hr)) {goto Cleanup;}

hr = pDisp->QueryInterface(IID_IADsServiceOperations,(void**)&pSrvOp);
if(FAILED(hr)) {goto Cleanup;}

hr = pSrvOp->get_Status(&status);
switch (status) 
{
    case ADS_SERVICE_STOPPED:
        printf("The service has stopped.\n");
        break;
    case ADS_SERVICE_RUNNING:
        printf("The service is running.\n");
        break;
    case ADS_SERVICE_PAUSED:
        printf("The service has paused.\n");
        break;
    case ADS_SERVICE_ERROR:
        printf("The service has errors.\n");
        break;
}

Cleanup:
    if(pDisp) pDisp->Release();
    if(pCont) pCont->Release();
    if(pSrvOp) pSrvOp->Release();
```



## <a name="requirements"></a><span data-ttu-id="ad14b-139">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ad14b-139">Requirements</span></span>



| <span data-ttu-id="ad14b-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="ad14b-140">Requirement</span></span> | <span data-ttu-id="ad14b-141">Valore</span><span class="sxs-lookup"><span data-stu-id="ad14b-141">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="ad14b-142">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ad14b-142">Minimum supported client</span></span><br/> | <span data-ttu-id="ad14b-143">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ad14b-143">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="ad14b-144">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ad14b-144">Minimum supported server</span></span><br/> | <span data-ttu-id="ad14b-145">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ad14b-145">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="ad14b-146">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ad14b-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="ad14b-147"><dt>IADs. h</dt></span><span class="sxs-lookup"><span data-stu-id="ad14b-147"><dt>Iads.h</dt></span></span> </dl>        |
| <span data-ttu-id="ad14b-148">DLL</span><span class="sxs-lookup"><span data-stu-id="ad14b-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ad14b-149"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ad14b-149"><dt>Activeds.dll</dt></span></span> </dl>  |
| <span data-ttu-id="ad14b-150">IID</span><span class="sxs-lookup"><span data-stu-id="ad14b-150">IID</span></span><br/>                      | <span data-ttu-id="ad14b-151">IID \_ IADsServiceOperations è definito come 5D7B33F0-31CA-11CF-A98A-00AA006BC149</span><span class="sxs-lookup"><span data-stu-id="ad14b-151">IID\_IADsServiceOperations is defined as 5D7B33F0-31CA-11CF-A98A-00AA006BC149</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ad14b-152">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ad14b-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ad14b-153">**IADsFileService**</span><span class="sxs-lookup"><span data-stu-id="ad14b-153">**IADsFileService**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsfileservice)
</dt> <dt>

[<span data-ttu-id="ad14b-154">**IADsFileServiceOperations**</span><span class="sxs-lookup"><span data-stu-id="ad14b-154">**IADsFileServiceOperations**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsfileserviceoperations)
</dt> <dt>

[<span data-ttu-id="ad14b-155">**IADsService**</span><span class="sxs-lookup"><span data-stu-id="ad14b-155">**IADsService**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsservice)
</dt> <dt>

[<span data-ttu-id="ad14b-156">**IADsServiceOperations**</span><span class="sxs-lookup"><span data-stu-id="ad14b-156">**IADsServiceOperations**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsserviceoperations)
</dt> </dl>

 

 






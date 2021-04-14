---
title: Metodi di proprietà IADsFileService (IADs. h)
description: I metodi di proprietà dell'interfaccia IADsFileService ottengono o impostano le proprietà descritte nella tabella seguente. Per altre informazioni, vedere Metodi della proprietà di interfaccia.
ms.assetid: 1455df61-9218-450b-b956-1cf127364f24
ms.tgt_platform: multiple
keywords:
- Metodi di proprietà IADsFileService ADSI
topic_type:
- apiref
api_name:
- IADsFileService Property Methods
- IADsFileService.Description
- IADsFileService.get_Description
- IADsFileService.put_Description
- IADsFileService.MaxUserCount
- IADsFileService.get_MaxUserCount
- IADsFileService.put_MaxUserCount
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e1f3a46b37522bbdce6e99b969811e2909c8ecc9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518460"
---
# <a name="iadsfileservice-property-methods"></a><span data-ttu-id="3fffc-105">Metodi di proprietà IADsFileService</span><span class="sxs-lookup"><span data-stu-id="3fffc-105">IADsFileService Property Methods</span></span>

<span data-ttu-id="3fffc-106">I metodi di proprietà dell'interfaccia [**IADsFileService**](/windows/desktop/api/Iads/nn-iads-iadsfileservice) ottengono o impostano le proprietà descritte nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="3fffc-106">The property methods of the [**IADsFileService**](/windows/desktop/api/Iads/nn-iads-iadsfileservice) interface get or set the properties described in the following table.</span></span> <span data-ttu-id="3fffc-107">Per altre informazioni, vedere [metodi della proprietà di interfaccia](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="3fffc-107">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="3fffc-108">Proprietà</span><span class="sxs-lookup"><span data-stu-id="3fffc-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="3fffc-109">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="3fffc-109">**Description**</span></span>
<span data-ttu-id="3fffc-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="3fffc-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="3fffc-111">Descrizione del servizio file.</span><span class="sxs-lookup"><span data-stu-id="3fffc-111">The description of the file service.</span></span>

<dt>

<span data-ttu-id="3fffc-112">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="3fffc-112">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="3fffc-113">Tipo di dati di scripting: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="3fffc-113">Scripting data type: **BSTR**</span></span>
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

<span data-ttu-id="3fffc-114">**MaxUserCount**</span><span class="sxs-lookup"><span data-stu-id="3fffc-114">**MaxUserCount**</span></span>
<span data-ttu-id="3fffc-115"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="3fffc-115"></dt> <dd> <dl></span></span>

<span data-ttu-id="3fffc-116">Numero massimo di utenti consentiti per il servizio in qualsiasi momento.</span><span class="sxs-lookup"><span data-stu-id="3fffc-116">The maximum number of users allowed on the service at any time.</span></span>

<dt>

<span data-ttu-id="3fffc-117">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="3fffc-117">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="3fffc-118">Tipo di dati di scripting: **Long**</span><span class="sxs-lookup"><span data-stu-id="3fffc-118">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_MaxUserCount(
  [out] LONG* plMaxUserCount
);
HRESULT put_MaxUserCount(
  [in] LONG lMaxUserCount
);
```


</dt> </dl> </dd> </dl>

 

## <a name="remarks"></a><span data-ttu-id="3fffc-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="3fffc-119">Remarks</span></span>

<span data-ttu-id="3fffc-120">È necessario eseguire il servizio file per accedere a condivisioni file, sessioni e risorse in un computer.</span><span class="sxs-lookup"><span data-stu-id="3fffc-120">You must go through the file service to access file shares, sessions, and resources on a computer.</span></span>

## <a name="examples"></a><span data-ttu-id="3fffc-121">Esempio</span><span class="sxs-lookup"><span data-stu-id="3fffc-121">Examples</span></span>

<span data-ttu-id="3fffc-122">Nell'esempio di codice seguente viene scritta una descrizione per e viene verificato il limite utente del servizio file.</span><span class="sxs-lookup"><span data-stu-id="3fffc-122">The following code example writes a description for and check the user limit of the file service.</span></span>


```VB
Dim fs As IADsFileService
On Error GoTo Cleanup

' Bind to a file service object on "myComputer" in the local domain.
Set fs = GetObject("WinNT://myComputer/LanmanServer")

fs.Description = "WinNT file service."
n = fs.MaxUserCount
If n = -1 Then
   MsgBox "No limit has been imposed on number of users allowed."
Else
   MsgBox n & " users are allowed."
End If

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set fs = Nothing
```



<span data-ttu-id="3fffc-123">Nell'esempio di codice seguente viene scritta una descrizione per e viene verificato il limite utente per un oggetto servizio file.</span><span class="sxs-lookup"><span data-stu-id="3fffc-123">The following code example writes a description for and check the user limit on a file service object.</span></span>


```C++
HRESULT CheckFileService()
{
    IADsFileService *pFs = NULL;
    LPWSTR adsPath = L"WinNT://myComputer/LanmanServer";
    HRESULT hr = S_OK;
    long count = 0;

    hr = ADsGetObject(adsPath, IID_IADsFileService, (void**)&pFs)
    if(FAILED(hr)) {goto Cleanup;}

    hr = pFs->put_Description(CComBSTR("WinNT File Service"));
    if(FAILED(hr)) {goto Cleanup;}

    hr = pFs->SetInfo();
    if(FAILED(hr)) {goto Cleanup;}

    hr = pFs->get_MaxUserCount(&count);
    if(FAILED(hr)) {goto Cleanup;}

    if(count == -1) {
        printf("No limit has been imposed on the number of users.\n");
    } 
    else {
        printf("Number of allowed users are %d\n",count);
    }

Cleanup:
    if(pFs) pFs->Release();
    return S_OK;
}
```



## <a name="requirements"></a><span data-ttu-id="3fffc-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3fffc-124">Requirements</span></span>



| <span data-ttu-id="3fffc-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="3fffc-125">Requirement</span></span> | <span data-ttu-id="3fffc-126">Valore</span><span class="sxs-lookup"><span data-stu-id="3fffc-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3fffc-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3fffc-127">Minimum supported client</span></span><br/> | <span data-ttu-id="3fffc-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3fffc-128">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="3fffc-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3fffc-129">Minimum supported server</span></span><br/> | <span data-ttu-id="3fffc-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3fffc-130">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="3fffc-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3fffc-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="3fffc-132"><dt>IADs. h</dt></span><span class="sxs-lookup"><span data-stu-id="3fffc-132"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="3fffc-133">DLL</span><span class="sxs-lookup"><span data-stu-id="3fffc-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3fffc-134"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3fffc-134"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="3fffc-135">IID</span><span class="sxs-lookup"><span data-stu-id="3fffc-135">IID</span></span><br/>                      | <span data-ttu-id="3fffc-136">IID \_ IADsFileService è definito come A89D1900-31CA-11CF-A98A-00AA006BC149</span><span class="sxs-lookup"><span data-stu-id="3fffc-136">IID\_IADsFileService is defined as A89D1900-31CA-11CF-A98A-00AA006BC149</span></span><br/>      |



## <a name="see-also"></a><span data-ttu-id="3fffc-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3fffc-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3fffc-138">**IADsService**</span><span class="sxs-lookup"><span data-stu-id="3fffc-138">**IADsService**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsservice)
</dt> <dt>

[<span data-ttu-id="3fffc-139">**IADsFileService**</span><span class="sxs-lookup"><span data-stu-id="3fffc-139">**IADsFileService**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsfileservice)
</dt> <dt>

[<span data-ttu-id="3fffc-140">**IADsFileServiceOperations**</span><span class="sxs-lookup"><span data-stu-id="3fffc-140">**IADsFileServiceOperations**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsfileserviceoperations)
</dt> <dt>

[<span data-ttu-id="3fffc-141">**IADsServiceOperations**</span><span class="sxs-lookup"><span data-stu-id="3fffc-141">**IADsServiceOperations**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsserviceoperations)
</dt> <dt>

[<span data-ttu-id="3fffc-142">Metodi di proprietà dell'interfaccia</span><span class="sxs-lookup"><span data-stu-id="3fffc-142">Interface Property Methods</span></span>](interface-property-methods.md)
</dt> </dl>

 

 






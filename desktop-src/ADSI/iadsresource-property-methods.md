---
title: Metodi di proprietà IADsResource (IADs. h)
description: I metodi di proprietà dell'interfaccia IADsResource ottengono o impostano le proprietà descritte nella tabella seguente. Per informazioni generali sui metodi di proprietà, vedere Metodi della proprietà di interfaccia.
ms.assetid: a2d6ed76-88e9-468f-928a-a038b73fb362
ms.tgt_platform: multiple
keywords:
- Metodi di proprietà IADsResource ADSI
topic_type:
- apiref
api_name:
- IADsResource Property Methods
- IADsResource.LockCount
- IADsResource.get_LockCount
- IADsResource.Path
- IADsResource.get_Path
- IADsResource.User
- IADsResource.get_User
- IADsResource.UserPath
- IADsResource.get_UserPath
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f0f2ab2642dd8d03062a26d096190cf7615977a1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301479"
---
# <a name="iadsresource-property-methods"></a><span data-ttu-id="bda6d-105">Metodi di proprietà IADsResource</span><span class="sxs-lookup"><span data-stu-id="bda6d-105">IADsResource Property Methods</span></span>

<span data-ttu-id="bda6d-106">I metodi di proprietà dell'interfaccia [**IADsResource**](/windows/desktop/api/Iads/nn-iads-iadsresource) ottengono o impostano le proprietà descritte nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="bda6d-106">The property methods of the [**IADsResource**](/windows/desktop/api/Iads/nn-iads-iadsresource) interface get or set the properties described in the following table.</span></span> <span data-ttu-id="bda6d-107">Per informazioni generali sui metodi di proprietà, vedere [metodi della proprietà di interfaccia](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="bda6d-107">For a general discussion of property methods, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="bda6d-108">Proprietà</span><span class="sxs-lookup"><span data-stu-id="bda6d-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="bda6d-109">**LockCount**</span><span class="sxs-lookup"><span data-stu-id="bda6d-109">**LockCount**</span></span>
<span data-ttu-id="bda6d-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="bda6d-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="bda6d-111">Numero di blocchi sulla risorsa.</span><span class="sxs-lookup"><span data-stu-id="bda6d-111">Number of locks on the resource.</span></span>

<dt>

<span data-ttu-id="bda6d-112">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bda6d-112">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bda6d-113">Tipo di dati di scripting: **Long**</span><span class="sxs-lookup"><span data-stu-id="bda6d-113">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_LockCount(
  [out] LONG* plLockCount
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="bda6d-114">**Percorso**</span><span class="sxs-lookup"><span data-stu-id="bda6d-114">**Path**</span></span>
<span data-ttu-id="bda6d-115"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="bda6d-115"></dt> <dd> <dl></span></span>

<span data-ttu-id="bda6d-116">Percorso file system della risorsa aperta.</span><span class="sxs-lookup"><span data-stu-id="bda6d-116">The file system path of the opened resource.</span></span>

<dt>

<span data-ttu-id="bda6d-117">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bda6d-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bda6d-118">Tipo di dati di scripting: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="bda6d-118">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Path(
  [out] BSTR* pbstrPath
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="bda6d-119">**Utente**</span><span class="sxs-lookup"><span data-stu-id="bda6d-119">**User**</span></span>
<span data-ttu-id="bda6d-120"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="bda6d-120"></dt> <dd> <dl></span></span>

<span data-ttu-id="bda6d-121">Nome dell'utente che ha aperto la risorsa.</span><span class="sxs-lookup"><span data-stu-id="bda6d-121">The name of the user who opened the resource.</span></span>

<dt>

<span data-ttu-id="bda6d-122">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bda6d-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bda6d-123">Tipo di dati di scripting: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="bda6d-123">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_User(
  [out] BSTR* pbstrUser
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="bda6d-124">**UserPath**</span><span class="sxs-lookup"><span data-stu-id="bda6d-124">**UserPath**</span></span>
<span data-ttu-id="bda6d-125"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="bda6d-125"></dt> <dd> <dl></span></span>

<span data-ttu-id="bda6d-126">ADsPath dell'oggetto utente per l'utente che ha aperto la risorsa.</span><span class="sxs-lookup"><span data-stu-id="bda6d-126">The ADsPath of the user object for the user who opened the resource.</span></span>

<dt>

<span data-ttu-id="bda6d-127">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bda6d-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bda6d-128">Tipo di dati di scripting: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="bda6d-128">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_UserPath(
  [out] BSTR* pbstrUserPath
);
```


</dt> </dl> </dd> </dl>

 

## <a name="examples"></a><span data-ttu-id="bda6d-129">Esempio</span><span class="sxs-lookup"><span data-stu-id="bda6d-129">Examples</span></span>

<span data-ttu-id="bda6d-130">Nell'esempio di codice seguente viene illustrato come esaminare le risorse aperte di un servizio file.</span><span class="sxs-lookup"><span data-stu-id="bda6d-130">The following code example shows how to examine open resources of a file service.</span></span>


```VB
Dim fso As IADsFileServiceOperations
' Bind to a file service operations object on "myComputer" in the local domain.
Set fso = GetObject("WinNT://myComputer/LanmanServer")

' Enumerate resources.
If (IsEmpty(fso) = False) Then
    For Each resource In fso.resources
        MsgBox "Resource name: " & resource.name
        MsgBox "Resource path: " & resource.path
    Next resource
End If

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set fso = Nothing
```



<span data-ttu-id="bda6d-131">Nell'esempio di codice seguente viene enumerata una raccolta di risorse.</span><span class="sxs-lookup"><span data-stu-id="bda6d-131">The following code example enumerates a collection of resources.</span></span>


```C++
IADsFileServiceOperations *pFso = NULL;
IADsResource *pRes = NULL;
IADsCollection *pColl = NULL;
IUnknown *pUnk = NULL;
IEnumVARIANT *pEnum = NULL;
BSTR bstr = NULL;
VARIANT var;
ULONG lFetch = 0;
IDispatch *pDisp = NULL;
HRESULT hr = S_OK;

LPWSTR adsPath =L"WinNT://aMachine/LanmanServer";
hr = ADsGetObject(adsPath, IID_IADsFileServiceOperations,(void**)&pFso);
if(FAILED(hr)) {goto Cleanup;}

hr = pFso->Resources(&pColl);
if(FAILED(hr)) {goto Cleanup;}


// Enumerate print jobs. Code omitted.
hr = pColl->get__NewEnum(&pUnk);
if(FAILED(hr)) {goto Cleanup;}

hr = pUnk->QueryInterface(IID_IEnumVARIANT,(void**)&pEnum);
if(FAILED(hr)) {goto Cleanup;}

// Enumerate.
VariantInit(&var);
hr = pEnum->Next(1, &var, &lFetch);
while(hr == S_OK)
{
    if (lFetch == 1)    
    {
        pDisp = V_DISPATCH(&var);
        pDisp->QueryInterface(IID_IADsResource, (void**)&pRes);
        pRes->get_Name(&bstr);
        printf("Resource name: %S\n",bstr);
        SysFreeString(bstr);
        pRes->get_Path(&bstr);
        printf("Resource path: %S\n",bstr);
        SysFreeString(bstr);
        pRes->Release();
    }
    pDisp->Release();
    VariantClear(&var);
    hr = pEnum->Next(1, &var, &lFetch);
};

Cleanup:
    if(pRes) pRes->Release();
    if(pDisp) pDisp->Release();
    if(pEnum) pEnum->Release();
    if(pUnk) pUnk->Release();
    if(pColl) pColl->Release();
    if(pFso) pFso->Release();
```



## <a name="requirements"></a><span data-ttu-id="bda6d-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bda6d-132">Requirements</span></span>



| <span data-ttu-id="bda6d-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="bda6d-133">Requirement</span></span> | <span data-ttu-id="bda6d-134">Valore</span><span class="sxs-lookup"><span data-stu-id="bda6d-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bda6d-135">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bda6d-135">Minimum supported client</span></span><br/> | <span data-ttu-id="bda6d-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="bda6d-136">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="bda6d-137">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bda6d-137">Minimum supported server</span></span><br/> | <span data-ttu-id="bda6d-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bda6d-138">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="bda6d-139">Intestazione</span><span class="sxs-lookup"><span data-stu-id="bda6d-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="bda6d-140"><dt>IADs. h</dt></span><span class="sxs-lookup"><span data-stu-id="bda6d-140"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="bda6d-141">DLL</span><span class="sxs-lookup"><span data-stu-id="bda6d-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bda6d-142"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bda6d-142"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="bda6d-143">IID</span><span class="sxs-lookup"><span data-stu-id="bda6d-143">IID</span></span><br/>                      | <span data-ttu-id="bda6d-144">IID \_ IADsResource è definito come 34A05B20-4aab-11CF-AE2C-00AA006EBFB9</span><span class="sxs-lookup"><span data-stu-id="bda6d-144">IID\_IADsResource is defined as 34A05B20-4AAB-11CF-AE2C-00AA006EBFB9</span></span><br/>         |



## <a name="see-also"></a><span data-ttu-id="bda6d-145">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bda6d-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bda6d-146">**IADsResource**</span><span class="sxs-lookup"><span data-stu-id="bda6d-146">**IADsResource**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsresource)
</dt> <dt>

[<span data-ttu-id="bda6d-147">**IADsFileServiceOperations:: Resources**</span><span class="sxs-lookup"><span data-stu-id="bda6d-147">**IADsFileServiceOperations::Resources**</span></span>](/windows/desktop/api/Iads/nf-iads-iadsfileserviceoperations-resources)
</dt> </dl>

 

 






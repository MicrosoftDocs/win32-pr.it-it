---
title: Metodi di proprietà IADsContainer (IADs. h)
description: I metodi di proprietà dell'interfaccia IADsContainer ottengono o impostano le proprietà descritte nella tabella seguente. Per ulteriori informazioni e per una discussione generale sui metodi di proprietà, vedere Metodi della proprietà di interfaccia.
ms.assetid: 74d348bf-7b7f-4971-ba03-f77940600674
ms.tgt_platform: multiple
keywords:
- Metodi di proprietà IADsContainer ADSI
topic_type:
- apiref
api_name:
- IADsContainer Property Methods
- IADsContainer.Count
- IADsContainer.get_Count
- IADsContainer.Filter
- IADsContainer.get_Filter
- IADsContainer.put_Filter
- IADsContainer.Hints
- IADsContainer.get_Hints
- IADsContainer.put_Hints
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c5196addda0d9ff89f8a4976f3197bbeeae07044
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120751"
---
# <a name="iadscontainer-property-methods"></a><span data-ttu-id="4bcd0-105">Metodi di proprietà IADsContainer</span><span class="sxs-lookup"><span data-stu-id="4bcd0-105">IADsContainer Property Methods</span></span>

<span data-ttu-id="4bcd0-106">I metodi di proprietà dell'interfaccia [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer) ottengono o impostano le proprietà descritte nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="4bcd0-106">The property methods of the [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer) interface get or set the properties described in the following table.</span></span> <span data-ttu-id="4bcd0-107">Per ulteriori informazioni e per una discussione generale sui metodi di proprietà, vedere [metodi della proprietà di interfaccia](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="4bcd0-107">For more information, and a general discussion about property methods, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="4bcd0-108">Proprietà</span><span class="sxs-lookup"><span data-stu-id="4bcd0-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="4bcd0-109">**Count**</span><span class="sxs-lookup"><span data-stu-id="4bcd0-109">**Count**</span></span>
<span data-ttu-id="4bcd0-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="4bcd0-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="4bcd0-111">Recupera il numero di elementi nel contenitore.</span><span class="sxs-lookup"><span data-stu-id="4bcd0-111">Retrieves the number of items in the container.</span></span> <span data-ttu-id="4bcd0-112">Quando è impostato il **filtro** , **count** restituisce solo il numero di elementi filtrati.</span><span class="sxs-lookup"><span data-stu-id="4bcd0-112">When **Filter** is set, **Count** returns only the number of filtered items.</span></span>

<dt>

<span data-ttu-id="4bcd0-113">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4bcd0-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4bcd0-114">Tipo di dati di scripting: **Long**</span><span class="sxs-lookup"><span data-stu-id="4bcd0-114">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Count(
  [out] LONG* plCount
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="4bcd0-115">**Filter**</span><span class="sxs-lookup"><span data-stu-id="4bcd0-115">**Filter**</span></span>
<span data-ttu-id="4bcd0-116"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="4bcd0-116"></dt> <dd> <dl></span></span>

<span data-ttu-id="4bcd0-117">Recupera o imposta il filtro utilizzato per selezionare le classi di oggetti in un'enumerazione specificata.</span><span class="sxs-lookup"><span data-stu-id="4bcd0-117">Retrieves or sets the filter used to select object classes in a given enumeration.</span></span> <span data-ttu-id="4bcd0-118">Si tratta di una matrice Variant, ogni elemento di cui è il nome di una classe dello schema.</span><span class="sxs-lookup"><span data-stu-id="4bcd0-118">This is a variant array, each element of which is the name of a schema class.</span></span> <span data-ttu-id="4bcd0-119">Se **Filter** non è impostato o è impostato su Empty, tutti gli oggetti di tutte le classi vengono recuperati dall'enumeratore.</span><span class="sxs-lookup"><span data-stu-id="4bcd0-119">If **Filter** is not set or set to empty, all objects of all classes are retrieved by the enumerator.</span></span>

<dt>

<span data-ttu-id="4bcd0-120">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="4bcd0-120">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="4bcd0-121">Tipo di dati di scripting: **Variant**</span><span class="sxs-lookup"><span data-stu-id="4bcd0-121">Scripting data type: **VARIANT**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Filter(
  [out] VARIANT* pvFilter
);
HRESULT put_Filter(
  [in] VARIANT vFilter
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="4bcd0-122">**Hint**</span><span class="sxs-lookup"><span data-stu-id="4bcd0-122">**Hints**</span></span>
<span data-ttu-id="4bcd0-123"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="4bcd0-123"></dt> <dd> <dl></span></span>

<span data-ttu-id="4bcd0-124">Matrice Variant di stringhe **BSTR** .</span><span class="sxs-lookup"><span data-stu-id="4bcd0-124">A variant array of **BSTR** strings.</span></span> <span data-ttu-id="4bcd0-125">Ogni elemento identifica il nome di una proprietà presente nella definizione dello schema.</span><span class="sxs-lookup"><span data-stu-id="4bcd0-125">Each element identifies the name of a property found in the schema definition.</span></span> <span data-ttu-id="4bcd0-126">Il parametro *vHints* consente al client di indicare gli attributi da caricare per ogni oggetto enumerato.</span><span class="sxs-lookup"><span data-stu-id="4bcd0-126">The *vHints* parameter enables the client to indicate which attributes to load for each enumerated object.</span></span> <span data-ttu-id="4bcd0-127">Tali dati possono essere utilizzati per ottimizzare l'accesso alla rete.</span><span class="sxs-lookup"><span data-stu-id="4bcd0-127">Such data may be used to optimize network access.</span></span> <span data-ttu-id="4bcd0-128">L'implementazione esatta, tuttavia, è specifica del provider e non è attualmente utilizzata dal provider WinNT.</span><span class="sxs-lookup"><span data-stu-id="4bcd0-128">The exact implementation, however, is provider-specific, and is currently not used by the WinNT provider.</span></span>

<dt>

<span data-ttu-id="4bcd0-129">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="4bcd0-129">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="4bcd0-130">Tipo di dati di scripting: **Variant**</span><span class="sxs-lookup"><span data-stu-id="4bcd0-130">Scripting data type: **VARIANT**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Hints(
  [out] VARIANT* pvHints
);
HRESULT put_Hints(
  [in] VARIANT vHints
);
```


</dt> </dl> </dd> </dl>

 

## <a name="remarks"></a><span data-ttu-id="4bcd0-131">Commenti</span><span class="sxs-lookup"><span data-stu-id="4bcd0-131">Remarks</span></span>

<span data-ttu-id="4bcd0-132">I processi di enumerazione in [**IADsContainer:: Get \_ \_ NewEnum**](/windows/desktop/api/Iads/nf-iads-iadscontainer-get__newenum) e **IADsContainer:: Get \_ count** vengono eseguiti sugli oggetti contenuti nella cache.</span><span class="sxs-lookup"><span data-stu-id="4bcd0-132">The enumeration processes under [**IADsContainer::get\_\_NewEnum**](/windows/desktop/api/Iads/nf-iads-iadscontainer-get__newenum) and **IADsContainer::get\_Count** are performed against the contained objects in the cache.</span></span> <span data-ttu-id="4bcd0-133">Quando un contenitore contiene un numero elevato di oggetti, le prestazioni potrebbero essere influenzate.</span><span class="sxs-lookup"><span data-stu-id="4bcd0-133">When a container contains a large number of objects, the performance may be affected.</span></span> <span data-ttu-id="4bcd0-134">Per migliorare le prestazioni, disattivare la cache, impostare una dimensione di pagina appropriata e usare l'interfaccia [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) .</span><span class="sxs-lookup"><span data-stu-id="4bcd0-134">To enhance performance, turn off the cache, set up an appropriate page size, and use the [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) interface.</span></span> <span data-ttu-id="4bcd0-135">Per questo motivo, la proprietà **Ottieni \_ conteggio** non è supportata nel provider Microsoft LDAP.</span><span class="sxs-lookup"><span data-stu-id="4bcd0-135">For this reason, the **get\_Count** property is not supported in the Microsoft LDAP provider.</span></span>

## <a name="examples"></a><span data-ttu-id="4bcd0-136">Esempio</span><span class="sxs-lookup"><span data-stu-id="4bcd0-136">Examples</span></span>

<span data-ttu-id="4bcd0-137">Nell'esempio di codice Visual Basic riportato di seguito viene illustrato come utilizzare i metodi di proprietà di [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer) .</span><span class="sxs-lookup"><span data-stu-id="4bcd0-137">The following Visual Basic code example shows how property methods of [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer) can be used.</span></span>


```VB
Dim cont As IADsContainer
Dim usr As IADsUser

On Error GoTo Cleanup
 
Set cont = GetObject("LDAP://OU=Sales, DC=Fabrikam, DC=COM")
cont.Hints = Array("adminDescription") ' Load this attribute. Optional.
Debug.Print cont.Get("adminDescription")

' Filter users.
cont.Filter = Array("user")

For Each usr In cont
  Debug.Print usr.Name
Next

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set cont = Nothing
    Set usr = Nothing
```



<span data-ttu-id="4bcd0-138">Nell'esempio di codice C++ riportato di seguito viene illustrato come è possibile utilizzare i metodi di proprietà di [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer) .</span><span class="sxs-lookup"><span data-stu-id="4bcd0-138">The following C++ code example shows how the property methods of [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer) can be used.</span></span> <span data-ttu-id="4bcd0-139">Per brevità, il controllo degli errori viene omesso.</span><span class="sxs-lookup"><span data-stu-id="4bcd0-139">For brevity, error checking is omitted.</span></span>


```C++
IADsContainer *pCont;
IADs *pChild;
IADs *pADs;
 
HRESULT hr = ADsGetObject(L"LDAP://OU=Sales,DC=Fabrikam,DC=COM",
                          IID_IADsContainer, 
                          (void**)&pCont);

if(FAILED(hr)){goto Cleanup;}

LPWSTR pszArray[] = { L"adminDescription" };
DWORD dwNumber = sizeof(pszArray)/sizeof(LPWSTR);
hr = ADsBuildVarArrayStr( pszArray, dwNumber, &var);
if(FAILED(hr)){goto Cleanup;}

hr = pCont->put_Hints( var );
if(FAILED(hr)){goto Cleanup;}

VariantClear(&var);
 
hr = pCont->QueryInterface(IID_IADs, (void**)pADs);
if(FAILED(hr)){goto Cleanup;}
 
hr = pADs->Get(CComBSTR("adminDescription"), var);
 
LPWSTR pszUsers = {L"user"};
dwNumber = sizeof(pszUsers)/sizeof(LPWSTR);
hr = ADsBuildVarArrayStr(pszUsers, dwNumber, &var);
hr = pCont->put_Filter( var );
VariantClear(&var);
 
// Enumerate user objects in the container.
IEnumVARIANT *pEnum = NULL;
hr = ADsBuildEnumerator(pCont, &pEnum);
pCont->Release();    // Not required when users are enumerated.
 
ULONG lFetch;
VariantClear(&var);
while (SUCCEEDED(ADsEnumerateNext(pEnum, 1, &var, &lFetch)) && 
                      lFetch==1) {
    hr = V_DISPATCH(&var)->QueryInterface(IID_IADs, (void**)&pChild)
    if(SUCCEEDED(hr)) {
        BSTR bstrName;
        pChild->get_Name(&bstrName);
        printf("  %S\n", bstrName);
        SysFreeString(bstrName);
        pChild->Release();
    }
    VariantClear(&var);
}
Cleanup:
    if(pADs)
        pADs->Release();

    if(pCont)
        pCont->Release();

    if(pChild)
        pChild->Release();

    VariantClear(&var);
```



## <a name="requirements"></a><span data-ttu-id="4bcd0-140">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4bcd0-140">Requirements</span></span>



| <span data-ttu-id="4bcd0-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="4bcd0-141">Requirement</span></span> | <span data-ttu-id="4bcd0-142">Valore</span><span class="sxs-lookup"><span data-stu-id="4bcd0-142">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4bcd0-143">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4bcd0-143">Minimum supported client</span></span><br/> | <span data-ttu-id="4bcd0-144">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4bcd0-144">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="4bcd0-145">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4bcd0-145">Minimum supported server</span></span><br/> | <span data-ttu-id="4bcd0-146">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4bcd0-146">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="4bcd0-147">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4bcd0-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="4bcd0-148"><dt>IADs. h</dt></span><span class="sxs-lookup"><span data-stu-id="4bcd0-148"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="4bcd0-149">DLL</span><span class="sxs-lookup"><span data-stu-id="4bcd0-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4bcd0-150"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4bcd0-150"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="4bcd0-151">IID</span><span class="sxs-lookup"><span data-stu-id="4bcd0-151">IID</span></span><br/>                      | <span data-ttu-id="4bcd0-152">IID \_ IADsContainer è definito come 001677D0-FD16-11CE-ABC4-02608C9E7553</span><span class="sxs-lookup"><span data-stu-id="4bcd0-152">IID\_IADsContainer is defined as 001677D0-FD16-11CE-ABC4-02608C9E7553</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="4bcd0-153">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4bcd0-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4bcd0-154">**IADsContainer**</span><span class="sxs-lookup"><span data-stu-id="4bcd0-154">**IADsContainer**</span></span>](/windows/desktop/api/Iads/nn-iads-iadscontainer)
</dt> <dt>

[<span data-ttu-id="4bcd0-155">**IDirectorySearch**</span><span class="sxs-lookup"><span data-stu-id="4bcd0-155">**IDirectorySearch**</span></span>](/windows/desktop/api/Iads/nn-iads-idirectorysearch)
</dt> </dl>

 

 






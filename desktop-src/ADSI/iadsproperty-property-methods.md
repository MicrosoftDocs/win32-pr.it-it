---
title: Metodi di proprietà IADsProperty (IADs. h)
description: Leggere e scrivere le proprietà descritte nella tabella seguente.
ms.assetid: dd348a3c-0386-4fa2-984d-cdea6f09bd72
ms.tgt_platform: multiple
keywords:
- Metodi di proprietà IADsProperty ADSI
topic_type:
- apiref
api_name:
- IADsProperty Property Methods
- IADsProperty.OID
- IADsProperty.get_OID
- IADsProperty.put_OID
- IADsProperty.Syntax
- IADsProperty.get_Syntax
- IADsProperty.put_Syntax
- IADsProperty.MaxRange
- IADsProperty.get_MaxRange
- IADsProperty.put_MaxRange
- IADsProperty.MinRange
- IADsProperty.get_MinRange
- IADsProperty.put_MinRange
- IADsProperty.MultiValued
- IADsProperty.get_MultiValued
- IADsProperty.put_MultiValued
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 233bd5411e1c82956ef745255418a1b176af5900
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301086"
---
# <a name="iadsproperty-property-methods"></a><span data-ttu-id="ec2f6-104">Metodi di proprietà IADsProperty</span><span class="sxs-lookup"><span data-stu-id="ec2f6-104">IADsProperty Property Methods</span></span>

<span data-ttu-id="ec2f6-105">I metodi di proprietà dell'interfaccia [**IADsProperty**](/windows/desktop/api/Iads/nn-iads-iadsproperty) leggono e scrivono le proprietà descritte nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="ec2f6-105">The property methods of the [**IADsProperty**](/windows/desktop/api/Iads/nn-iads-iadsproperty) interface read and write the properties described in the following table.</span></span> <span data-ttu-id="ec2f6-106">Per ulteriori informazioni sui metodi di proprietà, vedere [metodi della proprietà di interfaccia](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="ec2f6-106">For more information about property methods, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="ec2f6-107">Proprietà</span><span class="sxs-lookup"><span data-stu-id="ec2f6-107">Properties</span></span>

<dl> <dt>

<span data-ttu-id="ec2f6-108">**MaxRange**</span><span class="sxs-lookup"><span data-stu-id="ec2f6-108">**MaxRange**</span></span>
<span data-ttu-id="ec2f6-109"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="ec2f6-109"></dt> <dd> <dl></span></span>

<span data-ttu-id="ec2f6-110">Limite massimo di valori.</span><span class="sxs-lookup"><span data-stu-id="ec2f6-110">Upper limit of values.</span></span>

<dt>

<span data-ttu-id="ec2f6-111">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ec2f6-111">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="ec2f6-112">Tipo di dati di scripting: **Long**</span><span class="sxs-lookup"><span data-stu-id="ec2f6-112">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_MaxRange(
  [out] LONG* lnMaxRange
);
HRESULT put_MaxRange(
  [in] LONG lnMaxRange
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="ec2f6-113">**MinRange**</span><span class="sxs-lookup"><span data-stu-id="ec2f6-113">**MinRange**</span></span>
<span data-ttu-id="ec2f6-114"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="ec2f6-114"></dt> <dd> <dl></span></span>

<span data-ttu-id="ec2f6-115">Limite inferiore dei valori.</span><span class="sxs-lookup"><span data-stu-id="ec2f6-115">Lower limit of values.</span></span>

<dt>

<span data-ttu-id="ec2f6-116">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ec2f6-116">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="ec2f6-117">Tipo di dati di scripting: **Long**</span><span class="sxs-lookup"><span data-stu-id="ec2f6-117">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_MinRange(
  [out] LONG* lnMinRange
);
HRESULT put_MinRange(
  [in] LONG lnMinRange
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="ec2f6-118">**Multivalore**</span><span class="sxs-lookup"><span data-stu-id="ec2f6-118">**MultiValued**</span></span>
<span data-ttu-id="ec2f6-119"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="ec2f6-119"></dt> <dd> <dl></span></span>

<span data-ttu-id="ec2f6-120">Indica se la proprietà supporta uno o più valori.</span><span class="sxs-lookup"><span data-stu-id="ec2f6-120">Whether property supports single or multiple values.</span></span>

<dt>

<span data-ttu-id="ec2f6-121">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ec2f6-121">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="ec2f6-122">Tipo di dati di scripting: **\_ bool Variant**</span><span class="sxs-lookup"><span data-stu-id="ec2f6-122">Scripting data type: **VARIANT\_BOOL**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_MultiValued(
  [out] VARIANT_BOOL* fMultivalued
);
HRESULT put_MultiValued(
  [in] VARIANT_BOOL fMultivalued
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="ec2f6-123">**OID**</span><span class="sxs-lookup"><span data-stu-id="ec2f6-123">**OID**</span></span>
<span data-ttu-id="ec2f6-124"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="ec2f6-124"></dt> <dd> <dl></span></span>

<span data-ttu-id="ec2f6-125">Identificatore di oggetto specifico della directory.</span><span class="sxs-lookup"><span data-stu-id="ec2f6-125">Directory-specific object identifier.</span></span>

<dt>

<span data-ttu-id="ec2f6-126">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ec2f6-126">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="ec2f6-127">Tipo di dati di scripting: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="ec2f6-127">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_OID(
  [out] BSTR* bstrOID
);
HRESULT put_OID(
  [out] BSTR* bstrOID
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="ec2f6-128">**Sintassi**</span><span class="sxs-lookup"><span data-stu-id="ec2f6-128">**Syntax**</span></span>
<span data-ttu-id="ec2f6-129"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="ec2f6-129"></dt> <dd> <dl></span></span>

<span data-ttu-id="ec2f6-130">Percorso relativo dell'oggetto sintassi.</span><span class="sxs-lookup"><span data-stu-id="ec2f6-130">Relative path of syntax object.</span></span>

<dt>

<span data-ttu-id="ec2f6-131">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ec2f6-131">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="ec2f6-132">Tipo di dati di scripting: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="ec2f6-132">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Syntax(
  [out] BSTR* bstrSyntax
);
HRESULT put_Syntax(
  [in] BSTR* bstrSyntax
);
```


</dt> </dl> </dd> </dl>

 

## <a name="examples"></a><span data-ttu-id="ec2f6-133">Esempio</span><span class="sxs-lookup"><span data-stu-id="ec2f6-133">Examples</span></span>

<span data-ttu-id="ec2f6-134">Nell'esempio di codice seguente viene esaminato l'attributo **OperatingSystem** di un computer in una rete tramite il provider WinNT.</span><span class="sxs-lookup"><span data-stu-id="ec2f6-134">The following code example examines the **OperatingSystem** attribute of a computer on a network through the WinNT provider.</span></span>


```VB
Dim obj As IADs
Dim cl As IADsClass
Dim pr As IADsProperty
Dim sc As IADsContainer

On Error GoTo Cleanup
 
Set obj = GetObject("WinNT://myMachine,computer")
Set cl = GetObject(obj.Schema)
Set sc = GetObject(cl.Parent)
Set pr = sc.GetObject("Property","OperatingSystem")
 
MsgBox "Attribute:  " & pr.Name
MsgBox "Syntax:     " & pr.Syntax
MsgBox "MaxRange:   " & pr.MaxRange
MsgBox "MinRange:   " & pr.MinRange
MsgBox "Multivalued:" & pr.Multivalued

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set obj = Nothing
    Set cl = Nothing
    Set pr = Nothing
    Set sc = Nothing
```



<span data-ttu-id="ec2f6-135">Nell'esempio di codice seguente viene esaminato l'attributo **OperatingSystem** di un computer in una rete tramite il provider WinNT.</span><span class="sxs-lookup"><span data-stu-id="ec2f6-135">The following code example examines the **OperatingSystem** attribute of a computer on a network through the WinNT provider.</span></span> <span data-ttu-id="ec2f6-136">Per brevità, il controllo degli errori viene omesso.</span><span class="sxs-lookup"><span data-stu-id="ec2f6-136">For brevity, error checking is omitted.</span></span>


```C++
IADs *pADs = NULL;
IADsClass *pCls = NULL;
IADsProperty* pProp = NULL;
IADsContainer *pCont = NULL;
long lval;
short bval;
HRESULT hr = CoInitialize(NULL);
 
hr = ADsGetObject(L"WinNT://myMachine,computer",
                  IID_IADs, (void**)&pADs);
if(FAILED(hr))
    goto Cleanup;

BSTR bstr;
hr = pADs->get_Schema(&bstr);
if(FAILED(hr))
    goto Cleanup;

hr = ADsGetObject(bstr, IID_IADsClass, (void**)&pCls);
hr = pCls->get_Parent(&bstr);
if(FAILED(hr))
    goto Cleanup;

hr = ADsGetObject(bstr, IID_IADsContainer, (void**)&pCont);
if(FAILED(hr))
    goto Cleanup;
SysFreeString(bstr);

hr = pCont->GetObject(CComBSTR("Property"), CComBSTR("OperatingSystem"), (IDispatch**)&pProp);
if(FAILED(hr))
    goto Cleanup;

hr = pProp->get_Name(&bstr);
if(FAILED(hr))
    goto Cleanup;
printf(" Name : %S\n",bstr);
SysFreeString(bstr);

hr = pProp->get_Syntax(&bstr);
if(FAILED(hr))
    goto Cleanup;
printf(" Syntax : %S\n",bstr);
SysFreeString(bstr);

hr = pProp->get_MaxRange(&lval);
if(FAILED(hr))
    goto Cleanup;
printf(" MaxRange : %d\n",lval);
SysFreeString(bstr);

hr = pProp->get_MinRange(&lval);
if(FAILED(hr))
    goto Cleanup;
printf(" MinRange : %d\n", lval);
SysFreeString(bstr);

hr = pProp->get_Multivalued(&bval);
if(FAILED(hr))
    goto Cleanup;
printf(" MultiValued : %b\n",bval);
SysFreeString(bstr);

Cleanup:
    if(pADs)
        pADs->Release();

    if(pCls)
        pCls->Release();

    if(pCont)
        pCont->Release();

    if(pProp)
        pProp->Release(); 
 
CoUninitialize();
```



## <a name="requirements"></a><span data-ttu-id="ec2f6-137">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ec2f6-137">Requirements</span></span>



| <span data-ttu-id="ec2f6-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="ec2f6-138">Requirement</span></span> | <span data-ttu-id="ec2f6-139">Valore</span><span class="sxs-lookup"><span data-stu-id="ec2f6-139">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ec2f6-140">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ec2f6-140">Minimum supported client</span></span><br/> | <span data-ttu-id="ec2f6-141">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ec2f6-141">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="ec2f6-142">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ec2f6-142">Minimum supported server</span></span><br/> | <span data-ttu-id="ec2f6-143">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ec2f6-143">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ec2f6-144">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ec2f6-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="ec2f6-145"><dt>IADs. h</dt></span><span class="sxs-lookup"><span data-stu-id="ec2f6-145"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="ec2f6-146">DLL</span><span class="sxs-lookup"><span data-stu-id="ec2f6-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ec2f6-147"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ec2f6-147"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="ec2f6-148">IID</span><span class="sxs-lookup"><span data-stu-id="ec2f6-148">IID</span></span><br/>                      | <span data-ttu-id="ec2f6-149">IID \_ IADsProperty è definito come C8F93DD3-4AE0-11CF-9E73-00AA004A5691</span><span class="sxs-lookup"><span data-stu-id="ec2f6-149">IID\_IADsProperty is defined as C8F93DD3-4AE0-11CF-9E73-00AA004A5691</span></span><br/>         |



## <a name="see-also"></a><span data-ttu-id="ec2f6-150">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ec2f6-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ec2f6-151">**IADsClass**</span><span class="sxs-lookup"><span data-stu-id="ec2f6-151">**IADsClass**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsclass)
</dt> <dt>

[<span data-ttu-id="ec2f6-152">**IADsProperty**</span><span class="sxs-lookup"><span data-stu-id="ec2f6-152">**IADsProperty**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsproperty)
</dt> <dt>

[<span data-ttu-id="ec2f6-153">**IADsSyntax**</span><span class="sxs-lookup"><span data-stu-id="ec2f6-153">**IADsSyntax**</span></span>](/windows/desktop/api/Iads/nn-iads-iadssyntax)
</dt> </dl>

 

 






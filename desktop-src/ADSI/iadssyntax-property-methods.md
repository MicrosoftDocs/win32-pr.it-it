---
title: Metodi di proprietà IADsSyntax (IADs. h)
description: I metodi di proprietà dell'interfaccia IADsSyntax ottengono o impostano le proprietà elencate nella tabella seguente. Per ulteriori informazioni sui metodi di proprietà, vedere Metodi della proprietà di interfaccia.
ms.assetid: a216a55d-63eb-4fdf-a67f-8d4b5eb74262
ms.tgt_platform: multiple
keywords:
- Metodi di proprietà IADsSyntax ADSI
topic_type:
- apiref
api_name:
- IADsSyntax Property Methods
- IADsSyntax.OleAutoDataType
- IADsSyntax.get_OleAutoDataType
- IADsSyntax.put_OleAutoDataType
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7a41c84efb4f48171913156823e18a301236290
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517656"
---
# <a name="iadssyntax-property-methods"></a><span data-ttu-id="8f531-105">Metodi di proprietà IADsSyntax</span><span class="sxs-lookup"><span data-stu-id="8f531-105">IADsSyntax Property Methods</span></span>

<span data-ttu-id="8f531-106">I metodi di proprietà dell'interfaccia [**IADsSyntax**](/windows/desktop/api/Iads/nn-iads-iadssyntax) ottengono o impostano le proprietà elencate nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="8f531-106">The property methods of the [**IADsSyntax**](/windows/desktop/api/Iads/nn-iads-iadssyntax) interface get or set the properties listed in the following table.</span></span> <span data-ttu-id="8f531-107">Per ulteriori informazioni sui metodi di proprietà, vedere [metodi della proprietà di interfaccia](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="8f531-107">For more information about property methods, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="8f531-108">Proprietà</span><span class="sxs-lookup"><span data-stu-id="8f531-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="8f531-109">**OleAutoDataType**</span><span class="sxs-lookup"><span data-stu-id="8f531-109">**OleAutoDataType**</span></span>
<span data-ttu-id="8f531-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="8f531-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="8f531-111">Recupera e imposta un oggetto **Long** che contiene il valore della costante **VT \_ xxx** per il tipo di dati di automazione che rappresenta questa sintassi.</span><span class="sxs-lookup"><span data-stu-id="8f531-111">Retrieves and sets a **LONG** that contains the value of the **VT\_xxx** constant for the Automation data type that represents this syntax.</span></span>

<span data-ttu-id="8f531-112">Active Directory supporta le seguenti costanti **VT \_ xxx** per il tipo di dati di automazione che rappresenta questa sintassi:</span><span class="sxs-lookup"><span data-stu-id="8f531-112">Active Directory supports the following **VT\_xxx** constants for the Automation data type that represents this syntax:</span></span>

-   <span data-ttu-id="8f531-113">**VT \_ bool bool**</span><span class="sxs-lookup"><span data-stu-id="8f531-113">**VT\_BOOL** BOOL</span></span>
-   <span data-ttu-id="8f531-114">**VT \_** BSTR BSTR</span><span class="sxs-lookup"><span data-stu-id="8f531-114">**VT\_BSTR** BSTR</span></span>
-   <span data-ttu-id="8f531-115">**VT \_ bstrt bstrt**</span><span class="sxs-lookup"><span data-stu-id="8f531-115">**VT\_BSTRT** BSTRT</span></span>
-   <span data-ttu-id="8f531-116">**VT \_ valuta CY**</span><span class="sxs-lookup"><span data-stu-id="8f531-116">**VT\_CY** CURRENCY</span></span>
-   <span data-ttu-id="8f531-117">**VT \_ Data data**</span><span class="sxs-lookup"><span data-stu-id="8f531-117">**VT\_DATE** Date</span></span>
-   <span data-ttu-id="8f531-118">**VT \_** **null** vuoto</span><span class="sxs-lookup"><span data-stu-id="8f531-118">**VT\_EMPTY** **NULL**</span></span>
-   <span data-ttu-id="8f531-119">**VT \_ ERRORE** non valido</span><span class="sxs-lookup"><span data-stu-id="8f531-119">**VT\_ERROR** Not valid</span></span>
-   <span data-ttu-id="8f531-120">**VT \_ I2** Short</span><span class="sxs-lookup"><span data-stu-id="8f531-120">**VT\_I2** short</span></span>
-   <span data-ttu-id="8f531-121">**VT \_ I4** Long</span><span class="sxs-lookup"><span data-stu-id="8f531-121">**VT\_I4** long</span></span>
-   <span data-ttu-id="8f531-122">**VT \_ R4** Real</span><span class="sxs-lookup"><span data-stu-id="8f531-122">**VT\_R4** real</span></span>
-   <span data-ttu-id="8f531-123">**VT \_ Doppio R8**</span><span class="sxs-lookup"><span data-stu-id="8f531-123">**VT\_R8** double</span></span>
-   <span data-ttu-id="8f531-124">**VT \_ BYTE UI1**</span><span class="sxs-lookup"><span data-stu-id="8f531-124">**VT\_UI1** BYTE</span></span>

<dt>

<span data-ttu-id="8f531-125">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="8f531-125">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="8f531-126">Tipo di dati di scripting: **Long**</span><span class="sxs-lookup"><span data-stu-id="8f531-126">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_OleAutoDataType(
  [out] LONG* plAutoDataType
);
HRESULT put_OleAutoDataType(
  [in] LONG lAutoDataType
);
```


</dt> </dl> </dd> </dl>

 

## <a name="remarks"></a><span data-ttu-id="8f531-127">Commenti</span><span class="sxs-lookup"><span data-stu-id="8f531-127">Remarks</span></span>

<span data-ttu-id="8f531-128">Una matrice di byte senza segno, la **\_** \| **\_ matrice VT** Ui1 VT potrebbe significare che il provider ha eseguito il mapping di una sintassi di cui non è possibile eseguire il mapping a un tipo virtuale di automazione.</span><span class="sxs-lookup"><span data-stu-id="8f531-128">An array of unsigned bytes, **VT\_UI1**\|**VT\_ARRAY** could mean that the provider has mapped a syntax that cannot be mapped to an Automation virtual type.</span></span>

## <a name="examples"></a><span data-ttu-id="8f531-129">Esempio</span><span class="sxs-lookup"><span data-stu-id="8f531-129">Examples</span></span>

<span data-ttu-id="8f531-130">Nell'esempio di codice seguente viene esaminata la sintassi dell'attributo **OperatingSystemVersion** di un computer in una rete tramite il provider WinNT.</span><span class="sxs-lookup"><span data-stu-id="8f531-130">The following code example examines the syntax of the **OperatingSystemVersion** attribute of a computer on a network through the WinNT provider.</span></span> <span data-ttu-id="8f531-131">La sintassi del risultato è una stringa.</span><span class="sxs-lookup"><span data-stu-id="8f531-131">The result syntax is a string.</span></span>


```VB
Dim obj As IADs
Dim cl As IADsClass
Dim pr As IADsProperty
Dim sy As IADsSyntax
Dim sc As IADsContainer
On Error GoTo Cleanup

Set obj = GetObject("WinNT://myMachine,computer")
Set cl = GetObject(obj.Schema)
Set sc = GetObject(cl.Parent)
Set pr = sc.GetObject("Property","OperatingSystemVersion")
Set sy = GetObject(sc.ADsPath & "/" & pr.Syntax)
 
MsgBox "Automation data types: " & sy.OleAutoDataType

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set obj = Nothing
    Set cl = Nothing
    Set pr = Nothing
    Set sy = Nothing
    Set sc = Nothing
```



<span data-ttu-id="8f531-132">Nell'esempio di codice seguente viene esaminata la sintassi dell'attributo **OperatingSystemVersion** di un computer in una rete tramite il provider WinNT.</span><span class="sxs-lookup"><span data-stu-id="8f531-132">The following code example examines the syntax of the **OperatingSystemVersion** attribute of a computer on a network through the WinNT provider.</span></span> <span data-ttu-id="8f531-133">La sintassi del risultato è una stringa.</span><span class="sxs-lookup"><span data-stu-id="8f531-133">The result syntax is a string.</span></span> <span data-ttu-id="8f531-134">Per brevità, il controllo degli errori viene omesso.</span><span class="sxs-lookup"><span data-stu-id="8f531-134">For brevity, error checking is omitted.</span></span>


```C++
#include <stdio.h>
#include <activeds.h>
#include <atlbase.h>
 
IADs *pObj = NULL;
IADsClass *pCls = NULL;
IADsProperty *pProp = NULL;
IADsSyntax *pSyn = NULL;
IADsContainer *pCont = NULL;
 
HRESULT hr = ADsGetObject(L"WinNT://myMachine,computer",
                          IID_IADs,
                          (void**)&pObj);
if(FAILED(hr)){goto Cleanup;}
VARIANT var;
VariantInit(&var);
CComBSTR sbstr;
 
pObj->get_Schema(&sbstr);
printf("Object schema: %S\n",sbstr);
 
hr = ADsGetObject(sbstr, IID_IADsClass,(void**)&pCls);
if(FAILED(hr)){goto Cleanup;}

pCls->get_Parent(&sbstr);
printf("Object class's container:  %S\n", sbstr);
 
hr = ADsGetObject(sbstr, IID_IADsContainer, (void**)&pCont);
if(FAILED(hr)){goto Cleanup;}
pCont->QueryInterface(IID_IADs,(void**)&pObj);
pObj->get_ADsPath(&sbstr);
printf("Container's AdsPath:  %S\n",sbstr);
 
IDispatch *pDisp;
hr = pCont->GetObject(CComBSTR("Property"),
                      CComBSTR("OperatingSystemVersion"),
                      (IDispatch**)&pDisp);
if(FAILED(hr)){goto Cleanup;}
 
hr = pDisp->QueryInterface(IID_IADsProperty, (void**)&pProp);
if(FAILED(hr)){goto Cleanup;}
 
hr = pProp->get_Syntax(&sbstr);
if(FAILED(hr)){goto Cleanup;}
printf("Property Syntax:  %S\n",sbstr);
 
printf("ADsPath of the syntax object %S\n",sbstr);
 
hr = ADsGetObject(sbstr, IID_IADsSyntax, (void**)&pSyn);
if(FAILED(hr)){goto Cleanup;}

long lType;
pSyn->get_OleAutoDataType(&lType);
printf("Property syntax's OleAutoDataType: %d\n", lType);

Cleanup:
    if(pObj)
        pObj->Release();

    if(pProp)
        pProp->Release();

    if(pCls)
        pCls->Release();

    if(pSyn)
        pSyn->Release();

    if(pCont)
        pCont->Release();
```



## <a name="requirements"></a><span data-ttu-id="8f531-135">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8f531-135">Requirements</span></span>



| <span data-ttu-id="8f531-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="8f531-136">Requirement</span></span> | <span data-ttu-id="8f531-137">Valore</span><span class="sxs-lookup"><span data-stu-id="8f531-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8f531-138">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8f531-138">Minimum supported client</span></span><br/> | <span data-ttu-id="8f531-139">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8f531-139">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="8f531-140">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8f531-140">Minimum supported server</span></span><br/> | <span data-ttu-id="8f531-141">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8f531-141">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="8f531-142">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8f531-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="8f531-143"><dt>IADs. h</dt></span><span class="sxs-lookup"><span data-stu-id="8f531-143"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="8f531-144">DLL</span><span class="sxs-lookup"><span data-stu-id="8f531-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8f531-145"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8f531-145"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="8f531-146">IID</span><span class="sxs-lookup"><span data-stu-id="8f531-146">IID</span></span><br/>                      | <span data-ttu-id="8f531-147">IID \_ IADsSyntax è definito come C8F93DD2-4AE0-11CF-9E73-00AA004A5691</span><span class="sxs-lookup"><span data-stu-id="8f531-147">IID\_IADsSyntax is defined as C8F93DD2-4AE0-11CF-9E73-00AA004A5691</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="8f531-148">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8f531-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8f531-149">**IADsClass**</span><span class="sxs-lookup"><span data-stu-id="8f531-149">**IADsClass**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsclass)
</dt> <dt>

[<span data-ttu-id="8f531-150">**IADsProperty**</span><span class="sxs-lookup"><span data-stu-id="8f531-150">**IADsProperty**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsproperty)
</dt> <dt>

[<span data-ttu-id="8f531-151">**IADsSyntax**</span><span class="sxs-lookup"><span data-stu-id="8f531-151">**IADsSyntax**</span></span>](/windows/desktop/api/Iads/nn-iads-iadssyntax)
</dt> </dl>

 

 






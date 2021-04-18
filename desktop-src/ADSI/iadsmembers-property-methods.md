---
title: Metodi di proprietà IADsMembers (IADs. h)
description: I metodi dell'interfaccia IADsMembers leggono e scrivono le proprietà descritte in questo argomento. Per altre informazioni, vedere Metodi della proprietà di interfaccia.
ms.assetid: ed4e98e5-053c-4d3b-bcd0-3add96bbe120
ms.tgt_platform: multiple
keywords:
- Metodi di proprietà IADsMembers ADSI
topic_type:
- apiref
api_name:
- IADsMembers Property Methods
- IADsMembers.Count
- IADsMembers.get_Count
- IADsMembers.Filter
- IADsMembers.get_Filter
- IADsMembers.put_Filter
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af047d6fe52fdd7d808b1d7e5dbfb35303d3ff59
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302140"
---
# <a name="iadsmembers-property-methods"></a><span data-ttu-id="dfbf7-105">Metodi di proprietà IADsMembers</span><span class="sxs-lookup"><span data-stu-id="dfbf7-105">IADsMembers Property Methods</span></span>

<span data-ttu-id="dfbf7-106">I metodi dell'interfaccia [**IADsMembers**](/windows/desktop/api/Iads/nn-iads-iadsmembers) leggono e scrivono le proprietà descritte in questo argomento.</span><span class="sxs-lookup"><span data-stu-id="dfbf7-106">The methods of the [**IADsMembers**](/windows/desktop/api/Iads/nn-iads-iadsmembers) interface read and write the properties described in this topic.</span></span> <span data-ttu-id="dfbf7-107">Per altre informazioni, vedere [metodi della proprietà di interfaccia](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="dfbf7-107">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="dfbf7-108">Proprietà</span><span class="sxs-lookup"><span data-stu-id="dfbf7-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="dfbf7-109">**Count**</span><span class="sxs-lookup"><span data-stu-id="dfbf7-109">**Count**</span></span>
<span data-ttu-id="dfbf7-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="dfbf7-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="dfbf7-111">Indica il numero di elementi nel contenitore.</span><span class="sxs-lookup"><span data-stu-id="dfbf7-111">Indicates the number of items in the container.</span></span> <span data-ttu-id="dfbf7-112">Se il filtro è impostato, Count restituisce solo il numero di elementi che soddisfano la descrizione del filtro.</span><span class="sxs-lookup"><span data-stu-id="dfbf7-112">If the filter is set then count returns only the number of items that fit the filter description.</span></span>

<dt>

<span data-ttu-id="dfbf7-113">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="dfbf7-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dfbf7-114">Tipo di dati di scripting: **Long**</span><span class="sxs-lookup"><span data-stu-id="dfbf7-114">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Count(
  [out] LONG* plCountr
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="dfbf7-115">**Filter**</span><span class="sxs-lookup"><span data-stu-id="dfbf7-115">**Filter**</span></span>
<span data-ttu-id="dfbf7-116"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="dfbf7-116"></dt> <dd> <dl></span></span>

<span data-ttu-id="dfbf7-117">Indica il filtro.</span><span class="sxs-lookup"><span data-stu-id="dfbf7-117">Indicates the filter.</span></span> <span data-ttu-id="dfbf7-118">La sintassi delle voci nella matrice di filtri è identica a quella del filtro usato nell'interfaccia [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer) .</span><span class="sxs-lookup"><span data-stu-id="dfbf7-118">The syntax of the entries in the filter array is the same as the Filter used on the [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer) interface.</span></span>

<dt>

<span data-ttu-id="dfbf7-119">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="dfbf7-119">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="dfbf7-120">Tipo di dati di scripting: **Variant**</span><span class="sxs-lookup"><span data-stu-id="dfbf7-120">Scripting data type: **VARIANT**</span></span>
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


</dt> </dl> </dd> </dl>

 

## <a name="remarks"></a><span data-ttu-id="dfbf7-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="dfbf7-121">Remarks</span></span>

<span data-ttu-id="dfbf7-122">I provider di sistema ADSI non supportano il metodo della proprietà **IADsMembers:: Get \_ count** .</span><span class="sxs-lookup"><span data-stu-id="dfbf7-122">The ADSI system providers do not support the **IADsMembers::get\_Count** property method.</span></span>

## <a name="examples"></a><span data-ttu-id="dfbf7-123">Esempio</span><span class="sxs-lookup"><span data-stu-id="dfbf7-123">Examples</span></span>

<span data-ttu-id="dfbf7-124">Nell'esempio di codice riportato di seguito viene illustrato come utilizzare i metodi di proprietà di questa interfaccia.</span><span class="sxs-lookup"><span data-stu-id="dfbf7-124">The following code example shows how to use the property methods of this interface.</span></span>


```VB
Dim grp As IADsGroup
On Error GoTo Cleanup

Set grp = GetObject("WinNT://myComputer/someGroup")
grp.members.filter = Array("user")
For Each usr In grp.Members
    MsgBox usr.Name & "," & usr.Class & "," & usr.AdsPath
Next

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set grp = Nothing
```



<span data-ttu-id="dfbf7-125">Nell'esempio di codice seguente viene usato il metodo **IADsMembers::p UT \_ Filter** per preparare un'enumerazione della raccolta di membri di un gruppo.</span><span class="sxs-lookup"><span data-stu-id="dfbf7-125">The following code example uses the **IADsMembers::put\_Filter** method to prepare for an enumeration of the collection of members of a group.</span></span>


```C++
IADsGroup *pGroup;
HRESULT hr = S_OK;

LPWSTR grpPath = L"WinNT://myComputer/someGroup";
hr = ADsGetObject(grpPath,IID_IADsGroup,(void**)&pGroup);
if(FAILED(hr)){goto Cleanup;}

IADsMembers *pMembers;
hr = pGroup->Members(&pMembers);
if(FAILED(hr)){goto Cleanup;}

hr = pGroup->Release();

SAFEARRAY *sa = CreateSafeArray(L"user");
hr = pMembers->put_Filter(sa);
if(FAILED(hr)){goto Cleanup;}

hr = EnumMembers(pMembers);    // For more information, and a 
                               // code example, see 
                               // IADsMembers::get__NewEnum.
if(FAILED(hr)){goto Cleanup;}

Cleanup:
    if(pGroup) pGroup->Release();
    if(pMembers) pMembers->Release();
    return hr;
```



## <a name="requirements"></a><span data-ttu-id="dfbf7-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="dfbf7-126">Requirements</span></span>



| <span data-ttu-id="dfbf7-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="dfbf7-127">Requirement</span></span> | <span data-ttu-id="dfbf7-128">Valore</span><span class="sxs-lookup"><span data-stu-id="dfbf7-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="dfbf7-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="dfbf7-129">Minimum supported client</span></span><br/> | <span data-ttu-id="dfbf7-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="dfbf7-130">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="dfbf7-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="dfbf7-131">Minimum supported server</span></span><br/> | <span data-ttu-id="dfbf7-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="dfbf7-132">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="dfbf7-133">Intestazione</span><span class="sxs-lookup"><span data-stu-id="dfbf7-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="dfbf7-134"><dt>IADs. h</dt></span><span class="sxs-lookup"><span data-stu-id="dfbf7-134"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="dfbf7-135">DLL</span><span class="sxs-lookup"><span data-stu-id="dfbf7-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dfbf7-136"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dfbf7-136"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="dfbf7-137">IID</span><span class="sxs-lookup"><span data-stu-id="dfbf7-137">IID</span></span><br/>                      | <span data-ttu-id="dfbf7-138">IID \_ IADsMembers è definito come 451A0030-72EC-11CF-B03B-00AA006E0975</span><span class="sxs-lookup"><span data-stu-id="dfbf7-138">IID\_IADsMembers is defined as 451A0030-72EC-11CF-B03B-00AA006E0975</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="dfbf7-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="dfbf7-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dfbf7-140">**IADsContainer**</span><span class="sxs-lookup"><span data-stu-id="dfbf7-140">**IADsContainer**</span></span>](/windows/desktop/api/Iads/nn-iads-iadscontainer)
</dt> <dt>

[<span data-ttu-id="dfbf7-141">**IADsMembers:: Get \_ \_ NewEnum**</span><span class="sxs-lookup"><span data-stu-id="dfbf7-141">**IADsMembers::get\_\_NewEnum**</span></span>](/windows/desktop/api/Iads/nf-iads-iadsmembers-get__newenum)
</dt> <dt>

[<span data-ttu-id="dfbf7-142">**IADsMembers**</span><span class="sxs-lookup"><span data-stu-id="dfbf7-142">**IADsMembers**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsmembers)
</dt> <dt>

[<span data-ttu-id="dfbf7-143">Metodi di proprietà dell'interfaccia</span><span class="sxs-lookup"><span data-stu-id="dfbf7-143">Interface Property Methods</span></span>](interface-property-methods.md)
</dt> </dl>

 

 






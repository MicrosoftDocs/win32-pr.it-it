---
title: Metodi di proprietà IADsGroup (IADs. h)
description: Metodi di proprietà dell'interfaccia IADsGroup.
ms.assetid: a8aa88d4-4695-47bc-bf7f-a17236a5671c
ms.tgt_platform: multiple
keywords:
- Metodi di proprietà IADsGroup ADSI
topic_type:
- apiref
api_name:
- IADsGroup Property Methods
- IADsGroup.Description
- IADsGroup.get_Description
- IADsGroup.put_Description
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 665cb91a55298012e4e906c2972da5371e3960be
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302142"
---
# <a name="iadsgroup-property-methods"></a><span data-ttu-id="38756-104">Metodi di proprietà IADsGroup</span><span class="sxs-lookup"><span data-stu-id="38756-104">IADsGroup Property Methods</span></span>

<span data-ttu-id="38756-105">I metodi di proprietà dell'interfaccia [**IADsGroup**](/windows/desktop/api/Iads/nn-iads-iadsgroup) leggono e scrivono le proprietà seguenti.</span><span class="sxs-lookup"><span data-stu-id="38756-105">The property methods of the [**IADsGroup**](/windows/desktop/api/Iads/nn-iads-iadsgroup) interface read and write the following properties.</span></span> <span data-ttu-id="38756-106">Per altre informazioni, vedere [metodi della proprietà di interfaccia](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="38756-106">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="38756-107">Proprietà</span><span class="sxs-lookup"><span data-stu-id="38756-107">Properties</span></span>

<dl> <dt>

<span data-ttu-id="38756-108">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="38756-108">**Description**</span></span>
<span data-ttu-id="38756-109"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="38756-109"></dt> <dd> <dl></span></span>

<span data-ttu-id="38756-110">Indica la descrizione testuale dell'appartenenza al gruppo.</span><span class="sxs-lookup"><span data-stu-id="38756-110">Indicates the textual description of the group membership.</span></span>

<dt>

<span data-ttu-id="38756-111">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="38756-111">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="38756-112">Tipo di dati di scripting: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="38756-112">Scripting data type: **BSTR**</span></span>
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


</dt> </dl> </dd> </dl>

 

## <a name="remarks"></a><span data-ttu-id="38756-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="38756-113">Remarks</span></span>

### <a name="using-iadsgroup-to-retrieve-descriptions-of-built-in-groups"></a><span data-ttu-id="38756-114">Uso di IADsGroup per recuperare le descrizioni dei gruppi predefiniti</span><span class="sxs-lookup"><span data-stu-id="38756-114">Using IADsGroup to Retrieve Descriptions of Built-in Groups</span></span>

<span data-ttu-id="38756-115">Negli esempi seguenti viene illustrato come recuperare informazioni sugli oggetti gruppo di Windows in base al nome.</span><span class="sxs-lookup"><span data-stu-id="38756-115">The following examples show how to retrieve information about Windows group objects by name.</span></span> <span data-ttu-id="38756-116">In un ambiente multilingue, i gruppi predefiniti sono a volte noti da nomi localizzati diversi, il che significa che non possono essere recuperati direttamente usando identificatori di stringa, ad esempio "WinNT://Microsoft/Administrators".</span><span class="sxs-lookup"><span data-stu-id="38756-116">In a multilingual environment, built-in groups are sometimes known by different localized names, which means that they cannot be retrieved directly by using string identifiers such as "WinNT://Microsoft/Administrators".</span></span> <span data-ttu-id="38756-117">In tal caso, l'utente può eseguire l'associazione all'oggetto SID noto per il gruppo, recuperare il nome del gruppo localizzato e fornire tale nome al metodo GetObject.</span><span class="sxs-lookup"><span data-stu-id="38756-117">In that case, the user can bind to the well-known SID object for the group, retrieve the localized group name, and supply that to the GetObject method.</span></span> <span data-ttu-id="38756-118">Per ulteriori informazioni, vedere [SID noti](/windows/desktop/SecAuthZ/well-known-sids).</span><span class="sxs-lookup"><span data-stu-id="38756-118">For more information, see [Well-known SIDs](/windows/desktop/SecAuthZ/well-known-sids).</span></span>

## <a name="examples"></a><span data-ttu-id="38756-119">Esempio</span><span class="sxs-lookup"><span data-stu-id="38756-119">Examples</span></span>

<span data-ttu-id="38756-120">Nell'esempio di Visual Basic seguente viene illustrato come eseguire l'associazione a un oggetto gruppo e visualizzare la descrizione del gruppo.</span><span class="sxs-lookup"><span data-stu-id="38756-120">The following Visual Basic example shows how to bind to a group object and display the description of the group.</span></span>


```VB
Dim grp As IADsGroup
On Error GoTo Cleanup

Set grp = GetObject("WinNT://Microsoft/Administrators")
Debug.Print grp.Description

Cleanup
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set grp = Nothing
```



<span data-ttu-id="38756-121">Nell'esempio C++ riportato di seguito viene illustrato come eseguire l'associazione a un oggetto gruppo e visualizzare la descrizione del gruppo.</span><span class="sxs-lookup"><span data-stu-id="38756-121">The following C++ example shows how to bind to a group object and display the description of the group.</span></span>


```C++
IADsGroup *pGroup = NULL;
HRESULT hr = S_OK;
LPWSTR adsPath = L"WinNT://localHost/Administrators";
BSTR bstr;

hr = ADsGetObject(adsPath,IID_IADsGroup,(void**)&pGroup);

if(FAILED(hr)) {goto Cleanup;}

hr = pGroup->get_Description(&bstr);
if(FAILED(hr)) {goto Cleanup;}

printf("Description: %S\n",bstr);

Cleanup:
    SysFreeString(bstr);
    if(pGroup) 
        pGroup->Release();

    return hr;
```



## <a name="requirements"></a><span data-ttu-id="38756-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="38756-122">Requirements</span></span>



| <span data-ttu-id="38756-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="38756-123">Requirement</span></span> | <span data-ttu-id="38756-124">Valore</span><span class="sxs-lookup"><span data-stu-id="38756-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="38756-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="38756-125">Minimum supported client</span></span><br/> | <span data-ttu-id="38756-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="38756-126">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="38756-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="38756-127">Minimum supported server</span></span><br/> | <span data-ttu-id="38756-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="38756-128">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="38756-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="38756-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="38756-130"><dt>IADs. h</dt></span><span class="sxs-lookup"><span data-stu-id="38756-130"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="38756-131">DLL</span><span class="sxs-lookup"><span data-stu-id="38756-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="38756-132"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="38756-132"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="38756-133">IID</span><span class="sxs-lookup"><span data-stu-id="38756-133">IID</span></span><br/>                      | <span data-ttu-id="38756-134">IID \_ IADsGroup è definito come 27636B00-410f-11CF-B1FF-02608C9E7553</span><span class="sxs-lookup"><span data-stu-id="38756-134">IID\_IADsGroup is defined as 27636B00-410F-11CF-B1FF-02608C9E7553</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="38756-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="38756-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="38756-136">**IADs**</span><span class="sxs-lookup"><span data-stu-id="38756-136">**IADs**</span></span>](/windows/desktop/api/Iads/nn-iads-iads)
</dt> <dt>

[<span data-ttu-id="38756-137">**IADsGroup**</span><span class="sxs-lookup"><span data-stu-id="38756-137">**IADsGroup**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsgroup)
</dt> <dt>

[<span data-ttu-id="38756-138">Metodi di proprietà dell'interfaccia</span><span class="sxs-lookup"><span data-stu-id="38756-138">Interface Property Methods</span></span>](interface-property-methods.md)
</dt> </dl>

 


---
title: Metodi di proprietà IADsOU (IADs. h)
description: I metodi di proprietà dell'interfaccia IADsOU ottengono o impostano le proprietà elencate nella tabella seguente. Per altre informazioni, vedere Metodi della proprietà di interfaccia.
ms.assetid: 8cb84972-733b-47ca-8647-1b7a85c97021
ms.tgt_platform: multiple
keywords:
- Metodi di proprietà IADsOU ADSI
topic_type:
- apiref
api_name:
- IADsOU Property Methods
- IADsOU.BusinessCategory
- IADsOU.get_BusinessCategory
- IADsOU.put_BusinessCategory
- IADsOU.Description
- IADsOU.get_Description
- IADsOU.put_Description
- IADsOU.FaxNumber
- IADsOU.get_FaxNumber
- IADsOU.put_FaxNumber
- IADsOU.LocalityName
- IADsOU.get_LocalityName
- IADsOU.put_LocalityName
- IADsOU.PostalAddress
- IADsOU.get_PostalAddress
- IADsOU.put_PostalAddress
- IADsOU.TelephoneNumber
- IADsOU.get_TelephoneNumber
- IADsOU.put_TelephoneNumber
- IADsOU.SeeAlso
- IADsOU.get_SeeAlso
- IADsOU.put_SeeAlso
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a0ce30fad6a690a26a8e16b817b77b129dee25f1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302137"
---
# <a name="iadsou-property-methods"></a><span data-ttu-id="a8144-105">Metodi di proprietà IADsOU</span><span class="sxs-lookup"><span data-stu-id="a8144-105">IADsOU Property Methods</span></span>

<span data-ttu-id="a8144-106">I metodi di proprietà dell'interfaccia [**IADsOU**](/windows/desktop/api/Iads/nn-iads-iadsou) ottengono o impostano le proprietà elencate nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="a8144-106">The property methods of the [**IADsOU**](/windows/desktop/api/Iads/nn-iads-iadsou) interface get or set the properties listed in the following table.</span></span> <span data-ttu-id="a8144-107">Per altre informazioni, vedere [metodi della proprietà di interfaccia](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="a8144-107">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="a8144-108">Proprietà</span><span class="sxs-lookup"><span data-stu-id="a8144-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="a8144-109">**BusinessCategory**</span><span class="sxs-lookup"><span data-stu-id="a8144-109">**BusinessCategory**</span></span>
<span data-ttu-id="a8144-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="a8144-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="a8144-111">Stringa che contiene la funzione o le funzioni aziendali generali eseguite dall'unità organizzativa, ad esempio "contabilità".</span><span class="sxs-lookup"><span data-stu-id="a8144-111">A string that contains the general business function or functions performed by the organizational unit, for example "Accounting".</span></span>

<dt>

<span data-ttu-id="a8144-112">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="a8144-112">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="a8144-113">Tipo di dati di scripting: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="a8144-113">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_BusinessCategory(
  [out] BSTR* pbstrBusinessCategory
);
HRESULT put_BusinessCategory(
  [in] BSTR bstrBusinessCategory
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8144-114">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="a8144-114">**Description**</span></span>
<span data-ttu-id="a8144-115"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="a8144-115"></dt> <dd> <dl></span></span>

<span data-ttu-id="a8144-116">Stringa che contiene una descrizione testuale dell'unità organizzativa.</span><span class="sxs-lookup"><span data-stu-id="a8144-116">A string that contains a textual description of the organizational unit.</span></span>

<dt>

<span data-ttu-id="a8144-117">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="a8144-117">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="a8144-118">Tipo di dati di scripting: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="a8144-118">Scripting data type: **BSTR**</span></span>
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

<span data-ttu-id="a8144-119">**NumeroFax**</span><span class="sxs-lookup"><span data-stu-id="a8144-119">**FaxNumber**</span></span>
<span data-ttu-id="a8144-120"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="a8144-120"></dt> <dd> <dl></span></span>

<span data-ttu-id="a8144-121">Stringa che contiene il numero di fax dell'unità organizzativa.</span><span class="sxs-lookup"><span data-stu-id="a8144-121">A string that contains the facsimile number of the organizational unit.</span></span>

<dt>

<span data-ttu-id="a8144-122">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="a8144-122">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="a8144-123">Tipo di dati di scripting: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="a8144-123">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_FaxNumber(
  [out] BSTR* pbstrFaxNumber
);
HRESULT put_FaxNumber(
  [in] BSTR bstrFaxNumber
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8144-124">**LocalityName**</span><span class="sxs-lookup"><span data-stu-id="a8144-124">**LocalityName**</span></span>
<span data-ttu-id="a8144-125"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="a8144-125"></dt> <dd> <dl></span></span>

<span data-ttu-id="a8144-126">Stringa che contiene il nome dell'area geografica dell'unità organizzativa.</span><span class="sxs-lookup"><span data-stu-id="a8144-126">A string that contains the name of the geographic region of the organizational unit.</span></span>

<dt>

<span data-ttu-id="a8144-127">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="a8144-127">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="a8144-128">Tipo di dati di scripting: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="a8144-128">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_LocalityName(
  [out] BSTR* pbstrLocalityName
);
HRESULT put_LocalityName(
  [in] BSTR bstrLocalityName
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8144-129">**PostalAddress**</span><span class="sxs-lookup"><span data-stu-id="a8144-129">**PostalAddress**</span></span>
<span data-ttu-id="a8144-130"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="a8144-130"></dt> <dd> <dl></span></span>

<span data-ttu-id="a8144-131">Stringa che contiene l'indirizzo postale dell'unità organizzativa.</span><span class="sxs-lookup"><span data-stu-id="a8144-131">A string that contains the postal address of the organizational unit.</span></span>

<dt>

<span data-ttu-id="a8144-132">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="a8144-132">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="a8144-133">Tipo di dati di scripting: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="a8144-133">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_PostalAddress(
  [out] BSTR* pbstrPostalAddress
);
HRESULT put_PostalAddress(
  [in] BSTR bstrPostalAddress
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8144-134">**SeeAlso**</span><span class="sxs-lookup"><span data-stu-id="a8144-134">**SeeAlso**</span></span>
<span data-ttu-id="a8144-135"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="a8144-135"></dt> <dd> <dl></span></span>

<span data-ttu-id="a8144-136">Matrice di stringhe che contiene i nomi distinti di altri oggetti directory che possono essere rilevanti per questo oggetto.</span><span class="sxs-lookup"><span data-stu-id="a8144-136">An array of strings that contains the distinguished names of other directory objects which may be relevant to this object.</span></span>

<dt>

<span data-ttu-id="a8144-137">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="a8144-137">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="a8144-138">Tipo di dati di scripting: **Variant**</span><span class="sxs-lookup"><span data-stu-id="a8144-138">Scripting data type: **VARIANT**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_SeeAlso(
  [out] VARIANT* pvSeeAlso
);
HRESULT put_SeeAlso(
  [in] VARIANT vSeeAlso
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8144-139">**TelephoneNumber**</span><span class="sxs-lookup"><span data-stu-id="a8144-139">**TelephoneNumber**</span></span>
<span data-ttu-id="a8144-140"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="a8144-140"></dt> <dd> <dl></span></span>

<span data-ttu-id="a8144-141">Stringa che contiene il numero di telefono dell'unità organizzativa.</span><span class="sxs-lookup"><span data-stu-id="a8144-141">A string that contains the telephone number of the organizational unit.</span></span>

<dt>

<span data-ttu-id="a8144-142">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="a8144-142">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="a8144-143">Tipo di dati di scripting: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="a8144-143">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_TelephoneNumber(
  [out] BSTR* pbstrTelephoneNumber
);
HRESULT put_TelephoneNumber(
  [in] BSTR bstrTelephoneNumber
);
```


</dt> </dl> </dd> </dl>

 

## <a name="examples"></a><span data-ttu-id="a8144-144">Esempio</span><span class="sxs-lookup"><span data-stu-id="a8144-144">Examples</span></span>

<span data-ttu-id="a8144-145">L'esempio di codice seguente Visualizza il **BusinessCategory** e la **Descrizione** di tutte le unità organizzative in un contenitore.</span><span class="sxs-lookup"><span data-stu-id="a8144-145">The following code example displays the **BusinessCategory** and **Description** of all organization units in a container.</span></span> <span data-ttu-id="a8144-146">Si presuppone che il servizio directory sottostante supporti il raggruppamento di oggetti directory per unità organizzativa.</span><span class="sxs-lookup"><span data-stu-id="a8144-146">It assumes that the underlying directory service supports grouping of directory objects by organization unit.</span></span>


```VB
Dim dom As IADsContainer
Dim ou As IADsOU

' Bind to the container.
Set dom = GetObject("LDAP://server1/domain1")

' Filter out all objects that are not of class "organizationalUnit".
dom.filter = Array("organizationalUnit")

' Enumerate the organizational units in the container and display  
' the BusinessCategory and Description properties of each OU.
For Each ou In dom
    MsgBox ou.BusinessCategory & ": " & ou.Description
Next
```



## <a name="requirements"></a><span data-ttu-id="a8144-147">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a8144-147">Requirements</span></span>



| <span data-ttu-id="a8144-148">Requisito</span><span class="sxs-lookup"><span data-stu-id="a8144-148">Requirement</span></span> | <span data-ttu-id="a8144-149">Valore</span><span class="sxs-lookup"><span data-stu-id="a8144-149">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a8144-150">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a8144-150">Minimum supported client</span></span><br/> | <span data-ttu-id="a8144-151">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a8144-151">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a8144-152">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a8144-152">Minimum supported server</span></span><br/> | <span data-ttu-id="a8144-153">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a8144-153">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a8144-154">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a8144-154">Header</span></span><br/>                   | <dl> <span data-ttu-id="a8144-155"><dt>IADs. h</dt></span><span class="sxs-lookup"><span data-stu-id="a8144-155"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="a8144-156">DLL</span><span class="sxs-lookup"><span data-stu-id="a8144-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a8144-157"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a8144-157"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="a8144-158">IID</span><span class="sxs-lookup"><span data-stu-id="a8144-158">IID</span></span><br/>                      | <span data-ttu-id="a8144-159">IID \_ IADsOU è definito come A2F733B8-Effe-11CF-8ABC-00C04FD8D503</span><span class="sxs-lookup"><span data-stu-id="a8144-159">IID\_IADsOU is defined as A2F733B8-EFFE-11CF-8ABC-00C04FD8D503</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="a8144-160">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a8144-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8144-161">**IADsOU**</span><span class="sxs-lookup"><span data-stu-id="a8144-161">**IADsOU**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsou)
</dt> <dt>

[<span data-ttu-id="a8144-162">Metodi di proprietà dell'interfaccia</span><span class="sxs-lookup"><span data-stu-id="a8144-162">Interface Property Methods</span></span>](interface-property-methods.md)
</dt> </dl>

 

 






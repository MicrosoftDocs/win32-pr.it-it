---
title: Metodi di proprietà IADsLocality (IADs. h)
description: I metodi dell'interfaccia IADsLocality leggono e scrivono le proprietà descritte in questo argomento. Per altre informazioni, vedere Metodi della proprietà di interfaccia.
ms.assetid: 5d1cea40-62fb-49d4-857f-4563e9db7f51
ms.tgt_platform: multiple
keywords:
- Metodi di proprietà IADsLocality ADSI
topic_type:
- apiref
api_name:
- IADsLocality Property Methods
- IADsLocality.Description
- IADsLocality.get_Description
- IADsLocality.put_Description
- IADsLocality.LocalityName
- IADsLocality.get_LocalityName
- IADsLocality.put_LocalityName
- IADsLocality.PostalAddress
- IADsLocality.get_PostalAddress
- IADsLocality.put_PostalAddress
- IADsLocality.SeeAlso
- IADsLocality.get_SeeAlso
- IADsLocality.put_SeeAlso
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 34023f0af5365deb4f023d53a843dcf688c40afd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964661"
---
# <a name="iadslocality-property-methods"></a><span data-ttu-id="dd2d5-105">Metodi di proprietà IADsLocality</span><span class="sxs-lookup"><span data-stu-id="dd2d5-105">IADsLocality Property Methods</span></span>

<span data-ttu-id="dd2d5-106">I metodi dell'interfaccia [**IADsLocality**](/windows/desktop/api/Iads/nn-iads-iadslocality) leggono e scrivono le proprietà descritte in questo argomento.</span><span class="sxs-lookup"><span data-stu-id="dd2d5-106">The methods of the [**IADsLocality**](/windows/desktop/api/Iads/nn-iads-iadslocality) interface read and write the properties described in this topic.</span></span> <span data-ttu-id="dd2d5-107">Per altre informazioni, vedere [metodi della proprietà di interfaccia](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="dd2d5-107">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="dd2d5-108">Proprietà</span><span class="sxs-lookup"><span data-stu-id="dd2d5-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="dd2d5-109">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="dd2d5-109">**Description**</span></span>
<span data-ttu-id="dd2d5-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="dd2d5-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="dd2d5-111">Indica il testo che descrive la località.</span><span class="sxs-lookup"><span data-stu-id="dd2d5-111">Indicates the text that describes the locality.</span></span>

<dt>

<span data-ttu-id="dd2d5-112">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="dd2d5-112">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="dd2d5-113">Tipo di dati di scripting: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="dd2d5-113">Scripting data type: **BSTR**</span></span>
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

<span data-ttu-id="dd2d5-114">**LocalityName**</span><span class="sxs-lookup"><span data-stu-id="dd2d5-114">**LocalityName**</span></span>
<span data-ttu-id="dd2d5-115"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="dd2d5-115"></dt> <dd> <dl></span></span>

<span data-ttu-id="dd2d5-116">Indica il nome dell'area geografica come rappresentata da questo oggetto di località.</span><span class="sxs-lookup"><span data-stu-id="dd2d5-116">Indicates the name of the geographical region as represented by this locality object.</span></span>

<dt>

<span data-ttu-id="dd2d5-117">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="dd2d5-117">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="dd2d5-118">Tipo di dati di scripting: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="dd2d5-118">Scripting data type: **BSTR**</span></span>
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

<span data-ttu-id="dd2d5-119">**PostalAddress**</span><span class="sxs-lookup"><span data-stu-id="dd2d5-119">**PostalAddress**</span></span>
<span data-ttu-id="dd2d5-120"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="dd2d5-120"></dt> <dd> <dl></span></span>

<span data-ttu-id="dd2d5-121">Indica l'indirizzo postale principale della località.</span><span class="sxs-lookup"><span data-stu-id="dd2d5-121">Indicates the main postal address of the locality.</span></span>

<dt>

<span data-ttu-id="dd2d5-122">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="dd2d5-122">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="dd2d5-123">Tipo di dati di scripting: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="dd2d5-123">Scripting data type: **BSTR**</span></span>
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

<span data-ttu-id="dd2d5-124">**SeeAlso**</span><span class="sxs-lookup"><span data-stu-id="dd2d5-124">**SeeAlso**</span></span>
<span data-ttu-id="dd2d5-125"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="dd2d5-125"></dt> <dd> <dl></span></span>

<span data-ttu-id="dd2d5-126">Indica una matrice di nomi di ADsPath di oggetti directory rilevanti per questo oggetto.</span><span class="sxs-lookup"><span data-stu-id="dd2d5-126">Indicates an array of ADsPath names of directory objects relevant to this object.</span></span>

<dt>

<span data-ttu-id="dd2d5-127">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="dd2d5-127">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="dd2d5-128">Tipo di dati di scripting: **Variant**</span><span class="sxs-lookup"><span data-stu-id="dd2d5-128">Scripting data type: **VARIANT**</span></span>
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


</dt> </dl> </dd> </dl>

 

## <a name="examples"></a><span data-ttu-id="dd2d5-129">Esempio</span><span class="sxs-lookup"><span data-stu-id="dd2d5-129">Examples</span></span>

<span data-ttu-id="dd2d5-130">Nell'esempio di codice seguente vengono visualizzati i dati di località di un oggetto contenitore.</span><span class="sxs-lookup"><span data-stu-id="dd2d5-130">The following code example displays the locality data of a container object.</span></span> <span data-ttu-id="dd2d5-131">Si presuppone che sia stato creato un oggetto di località, denominato "setlocale", per l'oggetto contenitore e che le proprietà siano state impostate.</span><span class="sxs-lookup"><span data-stu-id="dd2d5-131">It assumes that a locality object, named "myLocality", has been created for the container object and the properties have been set.</span></span>


```VB
Dim dom As IADsContainer
Dim loc As IADsLocality
On Error GoTo Cleanup
 
Set dom = getObject("LDAP://adsrv1/dc=Fabrikam, dc=Com")
Set loc = dom.GetObject("locality","L=myLocality")
Debug.Print loc.Name
Debug.Print loc.LocalityName
Debug.Print loc.Description
Debug.Print loc.PostalAddress
Debug.Print loc.SeeAlso

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set dom = Nothing
    Set loc = Nothing
```



## <a name="requirements"></a><span data-ttu-id="dd2d5-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="dd2d5-132">Requirements</span></span>



| <span data-ttu-id="dd2d5-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="dd2d5-133">Requirement</span></span> | <span data-ttu-id="dd2d5-134">Valore</span><span class="sxs-lookup"><span data-stu-id="dd2d5-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="dd2d5-135">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="dd2d5-135">Minimum supported client</span></span><br/> | <span data-ttu-id="dd2d5-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="dd2d5-136">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="dd2d5-137">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="dd2d5-137">Minimum supported server</span></span><br/> | <span data-ttu-id="dd2d5-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="dd2d5-138">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="dd2d5-139">Intestazione</span><span class="sxs-lookup"><span data-stu-id="dd2d5-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="dd2d5-140"><dt>IADs. h</dt></span><span class="sxs-lookup"><span data-stu-id="dd2d5-140"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="dd2d5-141">DLL</span><span class="sxs-lookup"><span data-stu-id="dd2d5-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dd2d5-142"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dd2d5-142"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="dd2d5-143">IID</span><span class="sxs-lookup"><span data-stu-id="dd2d5-143">IID</span></span><br/>                      | <span data-ttu-id="dd2d5-144">IID \_ IADsLocality è definito come A05E03A2-Effe-11CF-8ABC-00C04FD8D503</span><span class="sxs-lookup"><span data-stu-id="dd2d5-144">IID\_IADsLocality is defined as A05E03A2-EFFE-11CF-8ABC-00C04FD8D503</span></span><br/>         |



## <a name="see-also"></a><span data-ttu-id="dd2d5-145">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="dd2d5-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dd2d5-146">**IADs**</span><span class="sxs-lookup"><span data-stu-id="dd2d5-146">**IADs**</span></span>](/windows/desktop/api/Iads/nn-iads-iads)
</dt> <dt>

[<span data-ttu-id="dd2d5-147">**IADsLocality**</span><span class="sxs-lookup"><span data-stu-id="dd2d5-147">**IADsLocality**</span></span>](/windows/desktop/api/Iads/nn-iads-iadslocality)
</dt> <dt>

[<span data-ttu-id="dd2d5-148">Metodi di proprietà dell'interfaccia</span><span class="sxs-lookup"><span data-stu-id="dd2d5-148">Interface Property Methods</span></span>](interface-property-methods.md)
</dt> </dl>

 

 






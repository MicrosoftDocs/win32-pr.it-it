---
title: Metodi di proprietà IADsPropertyValue (IADs. h)
description: I metodi di proprietà dell'interfaccia IADsPropertyValue forniscono accesso alle proprietà descritte nella tabella seguente. Per altre informazioni, vedere Metodi della proprietà di interfaccia.
ms.assetid: 1039d4a9-bef8-457d-9a32-3743c14adef1
ms.tgt_platform: multiple
keywords:
- Metodi di proprietà IADsPropertyValue ADSI
topic_type:
- apiref
api_name:
- IADsPropertyValue Property Methods
- IADsPropertyValue.ADsType
- IADsPropertyValue.get_ADsType
- IADsPropertyValue.put_ADsType
- IADsPropertyValue.DNString
- IADsPropertyValue.get_DNString
- IADsPropertyValue.put_DNString
- IADsPropertyValue.CaseExactString
- IADsPropertyValue.get_CaseExactString
- IADsPropertyValue.put_CaseExactString
- IADsPropertyValue.CaseIgnoreString
- IADsPropertyValue.get_CaseIgnoreString
- IADsPropertyValue.put_CaseIgnoreString
- IADsPropertyValue.PrintableString
- IADsPropertyValue.get_PrintableString
- IADsPropertyValue.put_PrintableString
- IADsPropertyValue.NumericString
- IADsPropertyValue.get_NumericString
- IADsPropertyValue.put_NumericString
- IADsPropertyValue.Boolean
- IADsPropertyValue.get_Boolean
- IADsPropertyValue.put_Boolean
- IADsPropertyValue.Integer
- IADsPropertyValue.get_Integer
- IADsPropertyValue.put_Integer
- IADsPropertyValue.OctetString
- IADsPropertyValue.get_OctetString
- IADsPropertyValue.put_OctetString
- IADsPropertyValue.SecurityDescriptor
- IADsPropertyValue.get_SecurityDescriptor
- IADsPropertyValue.put_SecurityDescriptor
- IADsPropertyValue.LargeInteger
- IADsPropertyValue.get_LargeInteger
- IADsPropertyValue.put_LargeInteger
- IADsPropertyValue.UTCTime
- IADsPropertyValue.get_UTCTime
- IADsPropertyValue.put_UTCTime
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 196e8097e5beaa5350738971be29de89b43c17a8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476354"
---
# <a name="iadspropertyvalue-property-methods"></a><span data-ttu-id="d3835-105">Metodi di proprietà IADsPropertyValue</span><span class="sxs-lookup"><span data-stu-id="d3835-105">IADsPropertyValue Property Methods</span></span>

<span data-ttu-id="d3835-106">I metodi di proprietà dell'interfaccia [**IADsPropertyValue**](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue) forniscono accesso alle proprietà descritte nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="d3835-106">The property methods of the [**IADsPropertyValue**](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue) interface provide access to the properties described in the following table.</span></span> <span data-ttu-id="d3835-107">Per altre informazioni, vedere [metodi della proprietà di interfaccia](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="d3835-107">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="d3835-108">Proprietà</span><span class="sxs-lookup"><span data-stu-id="d3835-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="d3835-109">**ADsType**</span><span class="sxs-lookup"><span data-stu-id="d3835-109">**ADsType**</span></span>
<span data-ttu-id="d3835-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="d3835-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="d3835-111">Tipo di dati del valore della proprietà, tratto dall'enumerazione [**ADSTYPEENUM**](/windows/win32/api/iads/ne-iads-adstypeenum) , della proprietà Value.</span><span class="sxs-lookup"><span data-stu-id="d3835-111">The data type of the value of the property, taken from the [**ADSTYPEENUM**](/windows/win32/api/iads/ne-iads-adstypeenum) enumeration, of the value property.</span></span>

<dt>

<span data-ttu-id="d3835-112">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="d3835-112">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="d3835-113">Tipo di dati di scripting: **Long**</span><span class="sxs-lookup"><span data-stu-id="d3835-113">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_ADsType(
  [out] LONG* ADsType
);
HRESULT put_ADsType(
  [in] LONG ADsType
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="d3835-114">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="d3835-114">**Boolean**</span></span>
<span data-ttu-id="d3835-115"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="d3835-115"></dt> <dd> <dl></span></span>

<span data-ttu-id="d3835-116">.</span><span class="sxs-lookup"><span data-stu-id="d3835-116">Boolean value.</span></span>

<dt>

<span data-ttu-id="d3835-117">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="d3835-117">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="d3835-118">Tipo di dati di scripting: **Long**</span><span class="sxs-lookup"><span data-stu-id="d3835-118">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Boolean(
  [out] LONG* lnBoolean
);
HRESULT put_Boolean(
  [in] LONG lnBoolean
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="d3835-119">**CaseExactString**</span><span class="sxs-lookup"><span data-stu-id="d3835-119">**CaseExactString**</span></span>
<span data-ttu-id="d3835-120"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="d3835-120"></dt> <dd> <dl></span></span>

<span data-ttu-id="d3835-121">Stringa da interpretare.</span><span class="sxs-lookup"><span data-stu-id="d3835-121">String to be interpreted.</span></span> <span data-ttu-id="d3835-122">Distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="d3835-122">Case-sensitive.</span></span>

<dt>

<span data-ttu-id="d3835-123">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="d3835-123">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="d3835-124">Tipo di dati di scripting: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="d3835-124">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_CaseExactString(
  [out] BSTR* bstrCaseExactString
);
HRESULT put_CaseExactString(
  [in] BSTR bstrCaseExactString
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="d3835-125">**CaseIgnoreString**</span><span class="sxs-lookup"><span data-stu-id="d3835-125">**CaseIgnoreString**</span></span>
<span data-ttu-id="d3835-126"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="d3835-126"></dt> <dd> <dl></span></span>

<span data-ttu-id="d3835-127">Stringa da interpretare.</span><span class="sxs-lookup"><span data-stu-id="d3835-127">String to be interpreted.</span></span> <span data-ttu-id="d3835-128">Senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="d3835-128">Case insensitive.</span></span>

<dt>

<span data-ttu-id="d3835-129">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="d3835-129">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="d3835-130">Tipo di dati di scripting: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="d3835-130">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_CaseIgnoreString(
  [out] BSTR* bstrCaseIgnoreString
);
HRESULT put_CaseIgnoreString(
  [in] BSTR bstrCaseIgnoreString
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="d3835-131">**DNString**</span><span class="sxs-lookup"><span data-stu-id="d3835-131">**DNString**</span></span>
<span data-ttu-id="d3835-132"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="d3835-132"></dt> <dd> <dl></span></span>

<span data-ttu-id="d3835-133">Stringa che identifica il nome distinto (percorso) di un oggetto valore del servizio directory.</span><span class="sxs-lookup"><span data-stu-id="d3835-133">String that identifies the distinguished name (path) of a directory service value object.</span></span>

<dt>

<span data-ttu-id="d3835-134">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="d3835-134">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="d3835-135">Tipo di dati di scripting: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="d3835-135">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_DNString(
  [out] BSTR* bstrDNString
);
HRESULT put_DNString(
  [in] BSTR bstrDNString
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="d3835-136">**Integer**</span><span class="sxs-lookup"><span data-stu-id="d3835-136">**Integer**</span></span>
<span data-ttu-id="d3835-137"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="d3835-137"></dt> <dd> <dl></span></span>

<span data-ttu-id="d3835-138">Valore intero.</span><span class="sxs-lookup"><span data-stu-id="d3835-138">Integer value.</span></span>

<dt>

<span data-ttu-id="d3835-139">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="d3835-139">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="d3835-140">Tipo di dati di scripting: **Long**</span><span class="sxs-lookup"><span data-stu-id="d3835-140">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Integer(
  [out] LONG* lnInteger
);
HRESULT put_Integer(
  [in] LONG lnInteger
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="d3835-141">**LargeInteger**</span><span class="sxs-lookup"><span data-stu-id="d3835-141">**LargeInteger**</span></span>
<span data-ttu-id="d3835-142"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="d3835-142"></dt> <dd> <dl></span></span>

<span data-ttu-id="d3835-143">Puntatore all'interfaccia [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) dell'oggetto che implementa [**IADsLargeInteger**](/windows/desktop/api/Iads/nn-iads-iadslargeinteger) per questo valore.</span><span class="sxs-lookup"><span data-stu-id="d3835-143">Pointer to the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface of the object implementing [**IADsLargeInteger**](/windows/desktop/api/Iads/nn-iads-iadslargeinteger) for this value.</span></span>

<dt>

<span data-ttu-id="d3835-144">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="d3835-144">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="d3835-145">Tipo di dati di scripting: **IDispatch**</span><span class="sxs-lookup"><span data-stu-id="d3835-145">Scripting data type: **IDispatch**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_LargeInteger(
  [out] IDispatch** ppLargeInteger
);
HRESULT put_LargeInteger(
  [in] IDispatch* pLargeInteger
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="d3835-146">**NumericString**</span><span class="sxs-lookup"><span data-stu-id="d3835-146">**NumericString**</span></span>
<span data-ttu-id="d3835-147"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="d3835-147"></dt> <dd> <dl></span></span>

<span data-ttu-id="d3835-148">Testo da interpretare.</span><span class="sxs-lookup"><span data-stu-id="d3835-148">Text to be interpreted.</span></span> <span data-ttu-id="d3835-149">Tipo numerico.</span><span class="sxs-lookup"><span data-stu-id="d3835-149">Numeric type.</span></span>

<dt>

<span data-ttu-id="d3835-150">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="d3835-150">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="d3835-151">Tipo di dati di scripting: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="d3835-151">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_NumericString(
  [out] BSTR* bstrNumericString
);
HRESULT put_NumericString(
  [in] BSTR bstrNumericString
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="d3835-152">**OctetString**</span><span class="sxs-lookup"><span data-stu-id="d3835-152">**OctetString**</span></span>
<span data-ttu-id="d3835-153"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="d3835-153"></dt> <dd> <dl></span></span>

<span data-ttu-id="d3835-154">Matrice Variant di caratteri a un byte.</span><span class="sxs-lookup"><span data-stu-id="d3835-154">Variant array of one-byte characters.</span></span>

<dt>

<span data-ttu-id="d3835-155">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="d3835-155">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="d3835-156">Tipo di dati di scripting: **Variant**</span><span class="sxs-lookup"><span data-stu-id="d3835-156">Scripting data type: **VARIANT**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_OctetString(
  [in] VARIANT* vOctetString
);
HRESULT put_OctetString(
  [in] VARIANT* vOctetString
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="d3835-157">**PrintableString**</span><span class="sxs-lookup"><span data-stu-id="d3835-157">**PrintableString**</span></span>
<span data-ttu-id="d3835-158"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="d3835-158"></dt> <dd> <dl></span></span>

<span data-ttu-id="d3835-159">Visualizzazione o stringa di stampa.</span><span class="sxs-lookup"><span data-stu-id="d3835-159">Display or print string.</span></span>

<dt>

<span data-ttu-id="d3835-160">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="d3835-160">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="d3835-161">Tipo di dati di scripting: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="d3835-161">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_PrintableString(
  [out] BSTR* bstrPrintableString
);
HRESULT put_PrintableString(
  [in] BSTR bstrPrintableString
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="d3835-162">**SecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="d3835-162">**SecurityDescriptor**</span></span>
<span data-ttu-id="d3835-163"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="d3835-163"></dt> <dd> <dl></span></span>

<span data-ttu-id="d3835-164">Puntatore all'interfaccia [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) dell'oggetto che implementa [**IADsSecurityDescriptor**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor) per questo valore.</span><span class="sxs-lookup"><span data-stu-id="d3835-164">Pointer to the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface of the object implementing [**IADsSecurityDescriptor**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor) for this value.</span></span>

<dt>

<span data-ttu-id="d3835-165">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="d3835-165">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="d3835-166">Tipo di dati di scripting: **IDispatch**</span><span class="sxs-lookup"><span data-stu-id="d3835-166">Scripting data type: **IDispatch**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_SecurityDescriptor(
  [out] IDispatch** ppSecurityDescriptor
);
HRESULT put_SecurityDescriptor(
  [in] IDispatch* pSecurityDescriptor
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="d3835-167">**UTCTime**</span><span class="sxs-lookup"><span data-stu-id="d3835-167">**UTCTime**</span></span>
<span data-ttu-id="d3835-168"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="d3835-168"></dt> <dd> <dl></span></span>

<span data-ttu-id="d3835-169">Data del tipo di **\_ Data VT** espresso nel formato UTC (Coordinated Universal Time).</span><span class="sxs-lookup"><span data-stu-id="d3835-169">A date of the **VT\_DATE** type expressed in Coordinated Universal Time (UTC) format.</span></span>

<dt>

<span data-ttu-id="d3835-170">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="d3835-170">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="d3835-171">Tipo di dati di scripting: **date**</span><span class="sxs-lookup"><span data-stu-id="d3835-171">Scripting data type: **DATE**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_UTCTime(
  [out] DATE* daUTCTime
);
HRESULT put_UTCTime(
  [in] DATE daUTCTime
);
```


</dt> </dl> </dd> </dl>

 

## <a name="remarks"></a><span data-ttu-id="d3835-172">Commenti</span><span class="sxs-lookup"><span data-stu-id="d3835-172">Remarks</span></span>

<span data-ttu-id="d3835-173">Con le proprietà [**IADsPropertyValue**](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue) viene impostato o recuperato solo un valore della proprietà del tipo specificato.</span><span class="sxs-lookup"><span data-stu-id="d3835-173">The [**IADsPropertyValue**](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue) properties will only set or retrieve a property value of the specified type.</span></span> <span data-ttu-id="d3835-174">Ad esempio, la proprietà **CaseIgnoreString** su un attributo di tipo **\_ \_ stringa DN ADSTYPE**, come l'attributo **Distinguishname** , comporterà un errore.</span><span class="sxs-lookup"><span data-stu-id="d3835-174">For example, the **CaseIgnoreString** property on an attribute of type **ADSTYPE\_DN\_STRING**, like the **distinguishedName** attribute, will result in an error.</span></span> <span data-ttu-id="d3835-175">La proprietà **CaseIgnoreString** funzionerà solo sugli attributi di tipo **Ads \_ case \_ Ignore \_ String**.</span><span class="sxs-lookup"><span data-stu-id="d3835-175">The **CaseIgnoreString** property will only work on attributes of type **ADS\_CASE\_IGNORE\_STRING**.</span></span> <span data-ttu-id="d3835-176">Nella tabella seguente viene eseguito il mapping del valore [**ADSTYPEENUM**](/windows/win32/api/iads/ne-iads-adstypeenum) alla proprietà **IADsPropertyValue** corrispondente che può essere utilizzata per accedere al tipo di attributo.</span><span class="sxs-lookup"><span data-stu-id="d3835-176">The following table maps the [**ADSTYPEENUM**](/windows/win32/api/iads/ne-iads-adstypeenum) value to the corresponding **IADsPropertyValue** property that can be used to access that attribute type.</span></span> <span data-ttu-id="d3835-177">Se un valore **ADSTYPEENUM** non è elencato in questa tabella, non è disponibile dall'interfaccia **IADsPropertyValue** .</span><span class="sxs-lookup"><span data-stu-id="d3835-177">If an **ADSTYPEENUM** value is not listed in this table, it is not available from the **IADsPropertyValue** interface.</span></span> <span data-ttu-id="d3835-178">L'interfaccia [**IADsPropertyValue2**](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue2) deve essere utilizzata per ottenere i dati negli altri formati.</span><span class="sxs-lookup"><span data-stu-id="d3835-178">The [**IADsPropertyValue2**](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue2) interface should be used to obtain data in the other formats.</span></span>



| <span data-ttu-id="d3835-179">Valore [**ADSTYPEENUM**](/windows/win32/api/iads/ne-iads-adstypeenum)</span><span class="sxs-lookup"><span data-stu-id="d3835-179">[**ADSTYPEENUM**](/windows/win32/api/iads/ne-iads-adstypeenum) value</span></span> | <span data-ttu-id="d3835-180">Proprietà [**IADsPropertyValue**](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue)</span><span class="sxs-lookup"><span data-stu-id="d3835-180">[**IADsPropertyValue**](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue) property</span></span> |
|------------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="d3835-181">**\_stringa DN \_ ADSTYPE**</span><span class="sxs-lookup"><span data-stu-id="d3835-181">**ADSTYPE\_DN\_STRING**</span></span>                  | <span data-ttu-id="d3835-182">**DNString**</span><span class="sxs-lookup"><span data-stu-id="d3835-182">**DNString**</span></span>                                            |
| <span data-ttu-id="d3835-183">**\_ \_ stringa esatta del case ADSTYPE \_**</span><span class="sxs-lookup"><span data-stu-id="d3835-183">**ADSTYPE\_CASE\_EXACT\_STRING**</span></span>         | <span data-ttu-id="d3835-184">**CaseExactString**</span><span class="sxs-lookup"><span data-stu-id="d3835-184">**CaseExactString**</span></span>                                     |
| <span data-ttu-id="d3835-185">**ADSTYPE \_ case \_ Ignora \_ stringa**</span><span class="sxs-lookup"><span data-stu-id="d3835-185">**ADSTYPE\_CASE\_IGNORE\_STRING**</span></span>        | <span data-ttu-id="d3835-186">**CaseIgnoreString**</span><span class="sxs-lookup"><span data-stu-id="d3835-186">**CaseIgnoreString**</span></span>                                    |
| <span data-ttu-id="d3835-187">**\_stringa stampabile \_ ADSTYPE**</span><span class="sxs-lookup"><span data-stu-id="d3835-187">**ADSTYPE\_PRINTABLE\_STRING**</span></span>           | <span data-ttu-id="d3835-188">**PrintableString**</span><span class="sxs-lookup"><span data-stu-id="d3835-188">**PrintableString**</span></span>                                     |
| <span data-ttu-id="d3835-189">**\_stringa numerica ADSTYPE \_**</span><span class="sxs-lookup"><span data-stu-id="d3835-189">**ADSTYPE\_NUMERIC\_STRING**</span></span>             | <span data-ttu-id="d3835-190">**NumericString**</span><span class="sxs-lookup"><span data-stu-id="d3835-190">**NumericString**</span></span>                                       |
| <span data-ttu-id="d3835-191">**ADSTYPE ( \_ booleano)**</span><span class="sxs-lookup"><span data-stu-id="d3835-191">**ADSTYPE\_BOOLEAN**</span></span>                     | <span data-ttu-id="d3835-192">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="d3835-192">**Boolean**</span></span>                                             |
| <span data-ttu-id="d3835-193">**ADSTYPE \_ Integer**</span><span class="sxs-lookup"><span data-stu-id="d3835-193">**ADSTYPE\_INTEGER**</span></span>                     | <span data-ttu-id="d3835-194">**Integer**</span><span class="sxs-lookup"><span data-stu-id="d3835-194">**Integer**</span></span>                                             |
| <span data-ttu-id="d3835-195">**\_stringa ottetto \_ ADSTYPE**</span><span class="sxs-lookup"><span data-stu-id="d3835-195">**ADSTYPE\_OCTET\_STRING**</span></span>               | <span data-ttu-id="d3835-196">**OctetString**</span><span class="sxs-lookup"><span data-stu-id="d3835-196">**OctetString**</span></span>                                         |
| <span data-ttu-id="d3835-197">**ADSTYPE \_ \_ ora UTC**</span><span class="sxs-lookup"><span data-stu-id="d3835-197">**ADSTYPE\_UTC\_TIME**</span></span>                   | <span data-ttu-id="d3835-198">**UTCTime**</span><span class="sxs-lookup"><span data-stu-id="d3835-198">**UTCTime**</span></span>                                             |
| <span data-ttu-id="d3835-199">**ADSTYPE \_ \_ Integer grande**</span><span class="sxs-lookup"><span data-stu-id="d3835-199">**ADSTYPE\_LARGE\_INTEGER**</span></span>              | <span data-ttu-id="d3835-200">**LargeInteger**</span><span class="sxs-lookup"><span data-stu-id="d3835-200">**LargeInteger**</span></span>                                        |
| <span data-ttu-id="d3835-201">**\_descrittore di sicurezza NT ADSTYPE \_ \_**</span><span class="sxs-lookup"><span data-stu-id="d3835-201">**ADSTYPE\_NT\_SECURITY\_DESCRIPTOR**</span></span>    | <span data-ttu-id="d3835-202">**SecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="d3835-202">**SecurityDescriptor**</span></span>                                  |



 

## <a name="examples"></a><span data-ttu-id="d3835-203">Esempio</span><span class="sxs-lookup"><span data-stu-id="d3835-203">Examples</span></span>

<span data-ttu-id="d3835-204">Nell'esempio di codice seguente viene illustrato come recuperare una proprietà dall'elenco delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="d3835-204">The following code example shows how to retrieve a property from the property list.</span></span>


```VB
Dim propList As IADsPropertyList
Dim propEntry As IADsPropertyEntry
Dim propVal As IADsPropertyValue

On Error GoTo Cleanup
 
' Retrieve the property list.
Set propList = GetObject("LDAP://dc01/DC=Fabrikam,DC=com")
propList.GetInfo
 
' Retrieve a property entry. If you are certain of the property type,
' replace ADSTYPE_UNKNOWN with the actual property type.
Set propEntry = propList.GetPropertyItem("description", ADSTYPE_UNKNOWN)
 
' Print the property entry values.
For Each v In propEntry.Values
    Set propVal = v
    Select Case propVal.ADsType
        Case ADSTYPE_CASE_EXACT_STRING
            Debug.Print propVal.CaseExactString
        Case ADSTYPE_CASE_IGNORE_STRING
            Debug.Print propVal.CaseIgnoreString
        Case Else
            Debug.Print "Unable to handle a property of type: " & propVal.ADsType
    End Select
    
Next

Cleanup:
    If (Err.Number<>0) Then
       Debug.Print "An error has occurred. " & Err.Number
    End If
    Set propList = Nothing
    Set propEntry = Nothing
    Set propVal = Nothing
```



<span data-ttu-id="d3835-205">Il codice seguente illustra come usare **IADsPropertyValue:: Get \_ CaseIgnoreString** per recuperare il valore della proprietà Description da un elenco di proprietà.</span><span class="sxs-lookup"><span data-stu-id="d3835-205">The following code shows how to use **IADsPropertyValue::get\_CaseIgnoreString** to retrieve the value of the description property from a property list.</span></span>


```C++
#include <activeds.h>
#include <stdio.h>
 
IADsPropertyList *pList = NULL;
IADsPropertyEntry *pEntry = NULL;
IADsPropertyValue *pVal = NULL;
IADs *pObj = NULL;
VARIANT var, varItem;
BSTR valStr;
IEnumVARIANT *pEnum = NULL;
LONG lstart = 0;
LONG lend = 0;
LONG lADsType = ADSTYPE_UNKNOWN;
 
VariantInit(&var);
VariantInit(&varItem);
 
// Bind to the directory object.
HRESULT hr = ADsGetObject(L"LDAP://dc01/DC=Fabrikam,DC=com",
                          IID_IADsPropertyList,
                          (void**)&pList);

if(FAILED(hr)){goto Cleanup;}

// Initialize the property cache.
hr = pList->QueryInterface(IID_IADs,(void**)&pObj);
if(FAILED(hr)){goto Cleanup;}

pObj->GetInfo();
pObj->Release();
 
// Retrieve the property entry.
hr = pList->GetPropertyItem(CComBSTR("description"), ADSTYPE_CASE_IGNORE_STRING, &var);
pList->Release();
if(FAILED(hr)){goto Cleanup;}

hr = V_DISPATCH(&var)->QueryInterface(IID_IADsPropertyEntry,
                                      (void**)&pEntry);
VariantClear(&var);
if(FAILED(hr)){goto Cleanup;}
 
// Retrieve the value array of the property entry.
hr = pEntry->get_Values(&var);
if(FAILED(hr)){goto Cleanup;}

SAFEARRAY *sa = V_ARRAY( &var );
 
// Retrieve the lower and upper bound. Iterate and print the values.
hr = SafeArrayGetLBound( sa, 1, &lstart );
hr = SafeArrayGetUBound( sa, 1, &lend );
printf(" Property value(s) = ");
for ( long idx=lstart; idx < lend+1; idx++ )    {
    hr = SafeArrayGetElement( sa, &idx, &varItem );
    hr = V_DISPATCH(&varItem)->QueryInterface(IID_IADsPropertyValue,
                                              (void**)&pVal);
    if(FAILED(hr)){goto Cleanup;}

    pVal->get_ADsType(&lADsType);

    switch(lADsType)
    {
        case ADSTYPE_CASE_IGNORE_STRING:
        {
            hr = pVal->get_CaseIgnoreString(&valStr);
            break;
        }
        case ADSTYPE_CASE_EXACT_STRING:
        {
            hr = pVal->get_CaseExactString(&valStr);
            break;
        }
        default:
        {
            valStr = SysAllocString(L"Unable to handle a property of this type");
            break;
        }
    }

    if(FAILED(hr)){goto Cleanup;}
    printf(" %S ", valStr);
    SysFreeString(valStr);
    VariantClear(&varItem);
}
printf("\n");

Cleanup:
    if(pList)
        pList = NULL;

    if(pEntry)
        pEntry = NULL;

    if(pVal)
        pVal = NULL;

    if(pObj)
        pObj = NULL;

    if(pEnum)
        pEnum = NULL;

    SysFreeString(valStr);
    VariantClear(&varItem);
    VariantClear(&var);
```



## <a name="requirements"></a><span data-ttu-id="d3835-206">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d3835-206">Requirements</span></span>



| <span data-ttu-id="d3835-207">Requisito</span><span class="sxs-lookup"><span data-stu-id="d3835-207">Requirement</span></span> | <span data-ttu-id="d3835-208">Valore</span><span class="sxs-lookup"><span data-stu-id="d3835-208">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d3835-209">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d3835-209">Minimum supported client</span></span><br/> | <span data-ttu-id="d3835-210">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d3835-210">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d3835-211">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d3835-211">Minimum supported server</span></span><br/> | <span data-ttu-id="d3835-212">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d3835-212">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d3835-213">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d3835-213">Header</span></span><br/>                   | <dl> <span data-ttu-id="d3835-214"><dt>IADs. h</dt></span><span class="sxs-lookup"><span data-stu-id="d3835-214"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="d3835-215">DLL</span><span class="sxs-lookup"><span data-stu-id="d3835-215">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d3835-216"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d3835-216"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="d3835-217">IID</span><span class="sxs-lookup"><span data-stu-id="d3835-217">IID</span></span><br/>                      | <span data-ttu-id="d3835-218">IID \_ IADsPropertyValue è definito come 79FA9AD0-A97C-11D0-8534-00C04FD8D503</span><span class="sxs-lookup"><span data-stu-id="d3835-218">IID\_IADsPropertyValue is defined as 79FA9AD0-A97C-11D0-8534-00C04FD8D503</span></span><br/>    |



## <a name="see-also"></a><span data-ttu-id="d3835-219">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d3835-219">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d3835-220">**IADsPropertyValue**</span><span class="sxs-lookup"><span data-stu-id="d3835-220">**IADsPropertyValue**</span></span>](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue)
</dt> <dt>

[<span data-ttu-id="d3835-221">**ADSTYPEENUM**</span><span class="sxs-lookup"><span data-stu-id="d3835-221">**ADSTYPEENUM**</span></span>](/windows/win32/api/iads/ne-iads-adstypeenum)
</dt> <dt>

[<span data-ttu-id="d3835-222">**IADsPropertyEntry**</span><span class="sxs-lookup"><span data-stu-id="d3835-222">**IADsPropertyEntry**</span></span>](/windows/desktop/api/Iads/nn-iads-iadspropertyentry)
</dt> <dt>

[<span data-ttu-id="d3835-223">**IADsPropertyList**</span><span class="sxs-lookup"><span data-stu-id="d3835-223">**IADsPropertyList**</span></span>](/windows/desktop/api/Iads/nn-iads-iadspropertylist)
</dt> <dt>

[<span data-ttu-id="d3835-224">**IADsPropertyValue2**</span><span class="sxs-lookup"><span data-stu-id="d3835-224">**IADsPropertyValue2**</span></span>](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue2)
</dt> <dt>

[<span data-ttu-id="d3835-225">**IADsSecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="d3835-225">**IADsSecurityDescriptor**</span></span>](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor)
</dt> <dt>

[<span data-ttu-id="d3835-226">**IDispatch**</span><span class="sxs-lookup"><span data-stu-id="d3835-226">**IDispatch**</span></span>](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> </dl>

 


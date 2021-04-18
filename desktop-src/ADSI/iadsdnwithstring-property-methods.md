---
title: Metodi di proprietà IADsDNWithString (IADs. h)
description: Il metodo Property dell'interfaccia IADsDNWithString imposta la proprietà descritta nella tabella seguente. Per altre informazioni, vedere Metodi della proprietà di interfaccia.
ms.assetid: d3fb67b6-9f7d-4de5-bf01-f9c5b9e4f086
ms.tgt_platform: multiple
keywords:
- Metodi di proprietà IADsDNWithString ADSI
topic_type:
- apiref
api_name:
- IADsDNWithString Property Methods
- IADsDNWithString.StringValue
- IADsDNWithString.get_StringValue
- IADsDNWithString.put_StringValue
- IADsDNWithString.DNString
- IADsDNWithString.get_DNString
- IADsDNWithString.put_DNString
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4fa63a933a6a41eec9e6e55906a940cee650c87b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302147"
---
# <a name="iadsdnwithstring-property-methods"></a><span data-ttu-id="5b2a0-105">Metodi di proprietà IADsDNWithString</span><span class="sxs-lookup"><span data-stu-id="5b2a0-105">IADsDNWithString Property Methods</span></span>

<span data-ttu-id="5b2a0-106">Il metodo Property dell'interfaccia [**IADsDNWithString**](/windows/desktop/api/Iads/nn-iads-iadsdnwithstring) imposta la proprietà descritta nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="5b2a0-106">The property method of the [**IADsDNWithString**](/windows/desktop/api/Iads/nn-iads-iadsdnwithstring) interface sets the property described in the following table.</span></span> <span data-ttu-id="5b2a0-107">Per altre informazioni, vedere [metodi della proprietà di interfaccia](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="5b2a0-107">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="5b2a0-108">Proprietà</span><span class="sxs-lookup"><span data-stu-id="5b2a0-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="5b2a0-109">**DNString**</span><span class="sxs-lookup"><span data-stu-id="5b2a0-109">**DNString**</span></span>
<span data-ttu-id="5b2a0-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="5b2a0-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="5b2a0-111">Stringa DN associata a un valore stringa.</span><span class="sxs-lookup"><span data-stu-id="5b2a0-111">The DN string associated with a string value.</span></span>

<dt>

<span data-ttu-id="5b2a0-112">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5b2a0-112">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="5b2a0-113">Tipo di dati di scripting: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="5b2a0-113">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_DNString(
  [out] BSTR* retval
);
HRESULT put_DNString(
  [in] BSTR bstrDN
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="5b2a0-114">**StringValue**</span><span class="sxs-lookup"><span data-stu-id="5b2a0-114">**StringValue**</span></span>
<span data-ttu-id="5b2a0-115"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="5b2a0-115"></dt> <dd> <dl></span></span>

<span data-ttu-id="5b2a0-116">Valore stringa associato a un DN di un oggetto.</span><span class="sxs-lookup"><span data-stu-id="5b2a0-116">The string value associated with a DN of an object.</span></span>

<dt>

<span data-ttu-id="5b2a0-117">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5b2a0-117">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="5b2a0-118">Tipo di dati di scripting: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="5b2a0-118">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_StringValue(
  [out] BSTR* retVal
);
HRESULT put_StringValue(
  [in] BSTR varBV
);
```


</dt> </dl> </dd> </dl>

 

## <a name="requirements"></a><span data-ttu-id="5b2a0-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5b2a0-119">Requirements</span></span>



| <span data-ttu-id="5b2a0-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="5b2a0-120">Requirement</span></span> | <span data-ttu-id="5b2a0-121">Valore</span><span class="sxs-lookup"><span data-stu-id="5b2a0-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5b2a0-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5b2a0-122">Minimum supported client</span></span><br/> | <span data-ttu-id="5b2a0-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5b2a0-123">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="5b2a0-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5b2a0-124">Minimum supported server</span></span><br/> | <span data-ttu-id="5b2a0-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5b2a0-125">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="5b2a0-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5b2a0-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="5b2a0-127"><dt>IADs. h</dt></span><span class="sxs-lookup"><span data-stu-id="5b2a0-127"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="5b2a0-128">DLL</span><span class="sxs-lookup"><span data-stu-id="5b2a0-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5b2a0-129"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5b2a0-129"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="5b2a0-130">IID</span><span class="sxs-lookup"><span data-stu-id="5b2a0-130">IID</span></span><br/>                      | <span data-ttu-id="5b2a0-131">IID \_ IADsDNWithString è definito come 370DF02E-F934-11D2-BA96-00C04FB6D0D1</span><span class="sxs-lookup"><span data-stu-id="5b2a0-131">IID\_IADsDNWithString is defined as 370DF02E-F934-11D2-BA96-00C04FB6D0D1</span></span><br/>     |



## <a name="see-also"></a><span data-ttu-id="5b2a0-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5b2a0-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5b2a0-133">**IADsDNWithString**</span><span class="sxs-lookup"><span data-stu-id="5b2a0-133">**IADsDNWithString**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsdnwithstring)
</dt> <dt>

[<span data-ttu-id="5b2a0-134">**\_DN Ads \_ con \_ stringa**</span><span class="sxs-lookup"><span data-stu-id="5b2a0-134">**ADS\_DN\_WITH\_STRING**</span></span>](/windows/win32/api/iads/ns-iads-ads_dn_with_string)
</dt> </dl>

 

 






---
title: Metodi di proprietà IADsDNWithBinary (IADs. h)
description: Il metodo Property dell'interfaccia IADsDNWithBinary imposta la proprietà descritta nella tabella seguente. Per altre informazioni, vedere Metodi della proprietà di interfaccia.
ms.assetid: 3e9ceabb-7a38-4a63-ab62-240ff521e373
ms.tgt_platform: multiple
keywords:
- Metodi di proprietà IADsDNWithBinary ADSI
topic_type:
- apiref
api_name:
- IADsDNWithBinary Property Methods
- IADsDNWithBinary.BinaryValue
- IADsDNWithBinary.get_BinaryValue
- IADsDNWithBinary.put_BinaryValue
- IADsDNWithBinary.DNString
- IADsDNWithBinary.get_DNString
- IADsDNWithBinary.put_DNString
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: adf0398a141596de677d7d1739e84ff7525da9a2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120750"
---
# <a name="iadsdnwithbinary-property-methods"></a><span data-ttu-id="4ceb5-105">Metodi di proprietà IADsDNWithBinary</span><span class="sxs-lookup"><span data-stu-id="4ceb5-105">IADsDNWithBinary Property Methods</span></span>

<span data-ttu-id="4ceb5-106">Il metodo Property dell'interfaccia [**IADsDNWithBinary**](/windows/desktop/api/Iads/nn-iads-iadsdnwithbinary) imposta la proprietà descritta nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="4ceb5-106">The property method of the [**IADsDNWithBinary**](/windows/desktop/api/Iads/nn-iads-iadsdnwithbinary) interface sets the property described in the following table.</span></span> <span data-ttu-id="4ceb5-107">Per altre informazioni, vedere [metodi della proprietà di interfaccia](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="4ceb5-107">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="4ceb5-108">Proprietà</span><span class="sxs-lookup"><span data-stu-id="4ceb5-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="4ceb5-109">**BinaryValue**</span><span class="sxs-lookup"><span data-stu-id="4ceb5-109">**BinaryValue**</span></span>
<span data-ttu-id="4ceb5-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="4ceb5-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="4ceb5-111">GUID di un oggetto associato a un DN.</span><span class="sxs-lookup"><span data-stu-id="4ceb5-111">The GUID of an object associated with a DN.</span></span>

<dt>

<span data-ttu-id="4ceb5-112">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="4ceb5-112">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="4ceb5-113">Tipo di dati di scripting: **Variant**</span><span class="sxs-lookup"><span data-stu-id="4ceb5-113">Scripting data type: **VARIANT**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_BinaryValue(
  [out] VARIANT* retVal
);
HRESULT put_BinaryValue(
  [in] VARIANT varBV
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="4ceb5-114">**DNString**</span><span class="sxs-lookup"><span data-stu-id="4ceb5-114">**DNString**</span></span>
<span data-ttu-id="4ceb5-115"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="4ceb5-115"></dt> <dd> <dl></span></span>

<span data-ttu-id="4ceb5-116">Stringa DN associata al GUID di un oggetto.</span><span class="sxs-lookup"><span data-stu-id="4ceb5-116">The DN string associated with the GUID of an object.</span></span>

<dt>

<span data-ttu-id="4ceb5-117">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="4ceb5-117">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="4ceb5-118">Tipo di dati di scripting: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="4ceb5-118">Scripting data type: **BSTR**</span></span>
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


</dt> </dl> </dd> </dl>

 

## <a name="requirements"></a><span data-ttu-id="4ceb5-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4ceb5-119">Requirements</span></span>



| <span data-ttu-id="4ceb5-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="4ceb5-120">Requirement</span></span> | <span data-ttu-id="4ceb5-121">Valore</span><span class="sxs-lookup"><span data-stu-id="4ceb5-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4ceb5-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4ceb5-122">Minimum supported client</span></span><br/> | <span data-ttu-id="4ceb5-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4ceb5-123">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="4ceb5-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4ceb5-124">Minimum supported server</span></span><br/> | <span data-ttu-id="4ceb5-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4ceb5-125">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="4ceb5-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4ceb5-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="4ceb5-127"><dt>IADs. h</dt></span><span class="sxs-lookup"><span data-stu-id="4ceb5-127"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="4ceb5-128">DLL</span><span class="sxs-lookup"><span data-stu-id="4ceb5-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4ceb5-129"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4ceb5-129"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="4ceb5-130">IID</span><span class="sxs-lookup"><span data-stu-id="4ceb5-130">IID</span></span><br/>                      | <span data-ttu-id="4ceb5-131">IID \_ IADsDNWithBinary è definito come 7E99C0A2-F935-11D2-BA96-00C04FB6D0D1</span><span class="sxs-lookup"><span data-stu-id="4ceb5-131">IID\_IADsDNWithBinary is defined as 7E99C0A2-F935-11D2-BA96-00C04FB6D0D1</span></span><br/>     |



## <a name="see-also"></a><span data-ttu-id="4ceb5-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4ceb5-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4ceb5-133">**IADsDNWithBinary**</span><span class="sxs-lookup"><span data-stu-id="4ceb5-133">**IADsDNWithBinary**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsdnwithbinary)
</dt> <dt>

[<span data-ttu-id="4ceb5-134">**\_DN Ads \_ con \_ binario**</span><span class="sxs-lookup"><span data-stu-id="4ceb5-134">**ADS\_DN\_WITH\_BINARY**</span></span>](/windows/win32/api/iads/ns-iads-ads_dn_with_binary)
</dt> </dl>

 

 






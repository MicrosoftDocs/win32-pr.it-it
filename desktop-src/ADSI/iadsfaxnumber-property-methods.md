---
title: Metodi di proprietà IADsFaxNumber (IADs. h)
description: Il metodo Property dell'interfaccia IADsFaxNumber imposta la proprietà descritta nella tabella seguente. Per altre informazioni, vedere Metodi della proprietà di interfaccia.
ms.assetid: f4d46b9d-8db2-47b3-b489-9ffc363e6ac6
ms.tgt_platform: multiple
keywords:
- Metodi di proprietà IADsFaxNumber ADSI
topic_type:
- apiref
api_name:
- IADsFaxNumber Property Methods
- IADsFaxNumber.TelephoneNumber
- IADsFaxNumber.get_TelephoneNumber
- IADsFaxNumber.put_TelephoneNumber
- IADsFaxNumber.Parameters
- IADsFaxNumber.get_Parameters
- IADsFaxNumber.put_Parameters
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 93e2d982aee794272f80e58385be34098a92a28e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302144"
---
# <a name="iadsfaxnumber-property-methods"></a><span data-ttu-id="5a412-105">Metodi di proprietà IADsFaxNumber</span><span class="sxs-lookup"><span data-stu-id="5a412-105">IADsFaxNumber Property Methods</span></span>

<span data-ttu-id="5a412-106">Il metodo Property dell'interfaccia [**IADsFaxNumber**](/windows/desktop/api/Iads/nn-iads-iadsfaxnumber) imposta la proprietà descritta nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="5a412-106">The property method of the [**IADsFaxNumber**](/windows/desktop/api/Iads/nn-iads-iadsfaxnumber) interface sets the property described in the following table.</span></span> <span data-ttu-id="5a412-107">Per altre informazioni, vedere [metodi della proprietà di interfaccia](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="5a412-107">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="5a412-108">Proprietà</span><span class="sxs-lookup"><span data-stu-id="5a412-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="5a412-109">**Parametri**</span><span class="sxs-lookup"><span data-stu-id="5a412-109">**Parameters**</span></span>
<span data-ttu-id="5a412-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="5a412-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="5a412-111">Parametri per il computer fax.</span><span class="sxs-lookup"><span data-stu-id="5a412-111">The parameters for the fax machine.</span></span>

<dt>

<span data-ttu-id="5a412-112">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5a412-112">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="5a412-113">Tipo di dati di scripting: **Variant**</span><span class="sxs-lookup"><span data-stu-id="5a412-113">Scripting data type: **VARIANT**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Parameters(
  [out] VARIANT* retval
);
HRESULT put_Parameters(
  [in] VARIANT vParameters
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="5a412-114">**TelephoneNumber**</span><span class="sxs-lookup"><span data-stu-id="5a412-114">**TelephoneNumber**</span></span>
<span data-ttu-id="5a412-115"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="5a412-115"></dt> <dd> <dl></span></span>

<span data-ttu-id="5a412-116">Il numero di telefono del computer fax.</span><span class="sxs-lookup"><span data-stu-id="5a412-116">The telephone number of the fax machine.</span></span>

<dt>

<span data-ttu-id="5a412-117">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5a412-117">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="5a412-118">Tipo di dati di scripting: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="5a412-118">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_TelephoneNumber(
  [out] BSTR* retVal
);
HRESULT put_TelephoneNumber(
  [in] BSTR bstrTelephoneNumber
);
```


</dt> </dl> </dd> </dl>

 

## <a name="requirements"></a><span data-ttu-id="5a412-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5a412-119">Requirements</span></span>



| <span data-ttu-id="5a412-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="5a412-120">Requirement</span></span> | <span data-ttu-id="5a412-121">Valore</span><span class="sxs-lookup"><span data-stu-id="5a412-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5a412-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5a412-122">Minimum supported client</span></span><br/> | <span data-ttu-id="5a412-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5a412-123">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="5a412-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5a412-124">Minimum supported server</span></span><br/> | <span data-ttu-id="5a412-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5a412-125">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="5a412-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5a412-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="5a412-127"><dt>IADs. h</dt></span><span class="sxs-lookup"><span data-stu-id="5a412-127"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="5a412-128">DLL</span><span class="sxs-lookup"><span data-stu-id="5a412-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5a412-129"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5a412-129"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="5a412-130">IID</span><span class="sxs-lookup"><span data-stu-id="5a412-130">IID</span></span><br/>                      | <span data-ttu-id="5a412-131">IID \_ IADsFaxNumber è definito come A910DEA9-4680-11D1-0A3B-00C04FB950DC</span><span class="sxs-lookup"><span data-stu-id="5a412-131">IID\_IADsFaxNumber is defined as A910DEA9-4680-11D1-0A3B-00C04FB950DC</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="5a412-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5a412-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a412-133">**IADsFaxNumber**</span><span class="sxs-lookup"><span data-stu-id="5a412-133">**IADsFaxNumber**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsfaxnumber)
</dt> <dt>

[<span data-ttu-id="5a412-134">**\_NUMEROFAX ADS**</span><span class="sxs-lookup"><span data-stu-id="5a412-134">**ADS\_FAXNUMBER**</span></span>](/windows/win32/api/iads/ns-iads-ads_faxnumber)
</dt> </dl>

 

 






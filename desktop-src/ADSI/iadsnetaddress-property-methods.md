---
title: Metodi di proprietà IADsNetAddress (IADs. h)
description: Il metodo Property dell'interfaccia IADsNetAddress imposta la proprietà descritta nella tabella seguente. Per altre informazioni, vedere Metodi della proprietà di interfaccia.
ms.assetid: 1da493d6-5660-4054-8d28-89db0b56f30f
ms.tgt_platform: multiple
keywords:
- Metodi di proprietà IADsNetAddress ADSI
topic_type:
- apiref
api_name:
- IADsNetAddress Property Methods
- IADsNetAddress.AddressType
- IADsNetAddress.get_AddressType
- IADsNetAddress.put_AddressType
- IADsNetAddress.Address
- IADsNetAddress.get_Address
- IADsNetAddress.put_Address
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 073033c703db8eaa55b05058d6d2bbc3d3167f4b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742690"
---
# <a name="iadsnetaddress-property-methods"></a><span data-ttu-id="08aa1-105">Metodi di proprietà IADsNetAddress</span><span class="sxs-lookup"><span data-stu-id="08aa1-105">IADsNetAddress Property Methods</span></span>

<span data-ttu-id="08aa1-106">Il metodo Property dell'interfaccia [**IADsNetAddress**](/windows/desktop/api/Iads/nn-iads-iadsnetaddress) imposta la proprietà descritta nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="08aa1-106">The property method of the [**IADsNetAddress**](/windows/desktop/api/Iads/nn-iads-iadsnetaddress) interface sets the property described in the following table.</span></span> <span data-ttu-id="08aa1-107">Per altre informazioni, vedere [metodi della proprietà di interfaccia](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="08aa1-107">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="08aa1-108">Proprietà</span><span class="sxs-lookup"><span data-stu-id="08aa1-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="08aa1-109">**Indirizzo**</span><span class="sxs-lookup"><span data-stu-id="08aa1-109">**Address**</span></span>
<span data-ttu-id="08aa1-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="08aa1-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="08aa1-111">Un indirizzo di rete.</span><span class="sxs-lookup"><span data-stu-id="08aa1-111">A network address.</span></span>

<dt>

<span data-ttu-id="08aa1-112">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="08aa1-112">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="08aa1-113">Tipo di dati di scripting: **Variant**</span><span class="sxs-lookup"><span data-stu-id="08aa1-113">Scripting data type: **VARIANT**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Address(
  [out] VARIANT* retval
);
HRESULT put_Address(
  [in] VARIANT vAddress
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="08aa1-114">**AddressType**</span><span class="sxs-lookup"><span data-stu-id="08aa1-114">**AddressType**</span></span>
<span data-ttu-id="08aa1-115"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="08aa1-115"></dt> <dd> <dl></span></span>

<span data-ttu-id="08aa1-116">Tipo di protocolli di comunicazione.</span><span class="sxs-lookup"><span data-stu-id="08aa1-116">A type of communication protocols.</span></span>

<dt>

<span data-ttu-id="08aa1-117">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="08aa1-117">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="08aa1-118">Tipo di dati di scripting: **Long**</span><span class="sxs-lookup"><span data-stu-id="08aa1-118">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_AddressType(
  [out] LONG* retVal
);
HRESULT put_AddressType(
  [in] LONG lnAddressType
);
```


</dt> </dl> </dd> </dl>

 

## <a name="requirements"></a><span data-ttu-id="08aa1-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="08aa1-119">Requirements</span></span>



| <span data-ttu-id="08aa1-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="08aa1-120">Requirement</span></span> | <span data-ttu-id="08aa1-121">Valore</span><span class="sxs-lookup"><span data-stu-id="08aa1-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="08aa1-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="08aa1-122">Minimum supported client</span></span><br/> | <span data-ttu-id="08aa1-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="08aa1-123">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="08aa1-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="08aa1-124">Minimum supported server</span></span><br/> | <span data-ttu-id="08aa1-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="08aa1-125">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="08aa1-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="08aa1-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="08aa1-127"><dt>IADs. h</dt></span><span class="sxs-lookup"><span data-stu-id="08aa1-127"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="08aa1-128">DLL</span><span class="sxs-lookup"><span data-stu-id="08aa1-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="08aa1-129"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="08aa1-129"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="08aa1-130">IID</span><span class="sxs-lookup"><span data-stu-id="08aa1-130">IID</span></span><br/>                      | <span data-ttu-id="08aa1-131">IID \_ IADsNetAddress è definito come B21A50A9-4080-11D1-A3AC-00C04FB950DC</span><span class="sxs-lookup"><span data-stu-id="08aa1-131">IID\_IADsNetAddress is defined as B21A50A9-4080-11D1-A3AC-00C04FB950DC</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="08aa1-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="08aa1-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="08aa1-133">**IADsNetAddress**</span><span class="sxs-lookup"><span data-stu-id="08aa1-133">**IADsNetAddress**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsnetaddress)
</dt> <dt>

[<span data-ttu-id="08aa1-134">**\_Netaddress ADS**</span><span class="sxs-lookup"><span data-stu-id="08aa1-134">**ADS\_NETADDRESS**</span></span>](/windows/win32/api/iads/ns-iads-ads_netaddress)
</dt> </dl>

 

 






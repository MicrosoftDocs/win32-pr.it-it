---
title: Metodi di proprietà IADsHold (IADs. h)
description: Il metodo Property dell'interfaccia IADsHold imposta la proprietà descritta nella tabella seguente. Per altre informazioni, vedere Metodi della proprietà di interfaccia.
ms.assetid: 55968bc1-c44a-4db4-acc8-e1b6f1e4ad4c
ms.tgt_platform: multiple
keywords:
- Metodi di proprietà IADsHold ADSI
topic_type:
- apiref
api_name:
- IADsHold Property Methods
- IADsHold.ObjectName
- IADsHold.get_ObjectName
- IADsHold.put_ObjectName
- IADsHold.Amount
- IADsHold.get_Amount
- IADsHold.put_Amount
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cae2499efb461e6c13397fdaef75e515f0a1a21a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120742"
---
# <a name="iadshold-property-methods"></a><span data-ttu-id="cdf34-105">Metodi di proprietà IADsHold</span><span class="sxs-lookup"><span data-stu-id="cdf34-105">IADsHold Property Methods</span></span>

<span data-ttu-id="cdf34-106">Il metodo Property dell'interfaccia [**IADsHold**](/windows/desktop/api/Iads/nn-iads-iadshold) imposta la proprietà descritta nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="cdf34-106">The property method of the [**IADsHold**](/windows/desktop/api/Iads/nn-iads-iadshold) interface sets the property described in the following table.</span></span> <span data-ttu-id="cdf34-107">Per altre informazioni, vedere [metodi della proprietà di interfaccia](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="cdf34-107">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="cdf34-108">Proprietà</span><span class="sxs-lookup"><span data-stu-id="cdf34-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="cdf34-109">**Amount**</span><span class="sxs-lookup"><span data-stu-id="cdf34-109">**Amount**</span></span>
<span data-ttu-id="cdf34-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="cdf34-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="cdf34-111">Importo degli addebiti addebitati all'utente per il periodo di attesa mentre il server verifica il saldo dell'account dell'utente.</span><span class="sxs-lookup"><span data-stu-id="cdf34-111">The amount of charges levied against the user for the period on hold while the server checks the account balance of the user.</span></span>

<dt>

<span data-ttu-id="cdf34-112">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="cdf34-112">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="cdf34-113">Tipo di dati di scripting: **Long**</span><span class="sxs-lookup"><span data-stu-id="cdf34-113">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Amount(
  [out] LONG* retval
);
HRESULT put_Amount(
  [in] LONG lnAmount
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="cdf34-114">**ObjectName**</span><span class="sxs-lookup"><span data-stu-id="cdf34-114">**ObjectName**</span></span>
<span data-ttu-id="cdf34-115"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="cdf34-115"></dt> <dd> <dl></span></span>

<span data-ttu-id="cdf34-116">Nome dell'oggetto che rappresenta un utente in attesa.</span><span class="sxs-lookup"><span data-stu-id="cdf34-116">The name of the object representing a user on hold.</span></span>

<dt>

<span data-ttu-id="cdf34-117">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="cdf34-117">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="cdf34-118">Tipo di dati di scripting: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="cdf34-118">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_ObjectName(
  [out] BSTR* retVal
);
HRESULT put_ObjectName(
  [in] BSTR bstrObjectName
);
```


</dt> </dl> </dd> </dl>

 

## <a name="requirements"></a><span data-ttu-id="cdf34-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cdf34-119">Requirements</span></span>



| <span data-ttu-id="cdf34-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="cdf34-120">Requirement</span></span> | <span data-ttu-id="cdf34-121">Valore</span><span class="sxs-lookup"><span data-stu-id="cdf34-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cdf34-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cdf34-122">Minimum supported client</span></span><br/> | <span data-ttu-id="cdf34-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="cdf34-123">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="cdf34-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cdf34-124">Minimum supported server</span></span><br/> | <span data-ttu-id="cdf34-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="cdf34-125">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="cdf34-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="cdf34-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="cdf34-127"><dt>IADs. h</dt></span><span class="sxs-lookup"><span data-stu-id="cdf34-127"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="cdf34-128">DLL</span><span class="sxs-lookup"><span data-stu-id="cdf34-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cdf34-129"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cdf34-129"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="cdf34-130">IID</span><span class="sxs-lookup"><span data-stu-id="cdf34-130">IID</span></span><br/>                      | <span data-ttu-id="cdf34-131">IID \_ IADsHold è definito come B3EB3B37-4080-11D1-A3AC-00C04FB950DC</span><span class="sxs-lookup"><span data-stu-id="cdf34-131">IID\_IADsHold is defined as B3EB3B37-4080-11D1-A3AC-00C04FB950DC</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="cdf34-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cdf34-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cdf34-133">**IADsHold**</span><span class="sxs-lookup"><span data-stu-id="cdf34-133">**IADsHold**</span></span>](/windows/desktop/api/Iads/nn-iads-iadshold)
</dt> </dl>

 

 






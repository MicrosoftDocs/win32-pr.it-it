---
title: Metodi di proprietà IADsReplicaPointer (IADs. h)
description: Il metodo Property dell'interfaccia IADsReplicaPointer imposta la proprietà descritta nella tabella seguente. Per altre informazioni, vedere Metodi della proprietà di interfaccia.
ms.assetid: fc520ea4-b2c2-44c0-8bec-25f8d4a77074
ms.tgt_platform: multiple
keywords:
- Metodi di proprietà IADsReplicaPointer ADSI
topic_type:
- apiref
api_name:
- IADsReplicaPointer Property Methods
- IADsReplicaPointer.ServerName
- IADsReplicaPointer.get_ServerName
- IADsReplicaPointer.put_ServerName
- IADsReplicaPointer.ReplicaType
- IADsReplicaPointer.get_ReplicaType
- IADsReplicaPointer.put_ReplicaType
- IADsReplicaPointer.ReplicaNumber
- IADsReplicaPointer.get_ReplicaNumber
- IADsReplicaPointer.put_ReplicaNumber
- IADsReplicaPointer.Count
- IADsReplicaPointer.get_Count
- IADsReplicaPointer.put_Count
- IADsReplicaPointer.ReplicaAddressHints
- IADsReplicaPointer.get_ReplicaAddressHints
- IADsReplicaPointer.put_ReplicaAddressHints
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 044d5a5f1b87d42accb7e8e6e6c83eeda69eb5e0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517662"
---
# <a name="iadsreplicapointer-property-methods"></a><span data-ttu-id="65ad8-105">Metodi di proprietà IADsReplicaPointer</span><span class="sxs-lookup"><span data-stu-id="65ad8-105">IADsReplicaPointer Property Methods</span></span>

<span data-ttu-id="65ad8-106">Il metodo Property dell'interfaccia [**IADsReplicaPointer**](/windows/desktop/api/Iads/nn-iads-iadsreplicapointer) imposta la proprietà descritta nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="65ad8-106">The property method of the [**IADsReplicaPointer**](/windows/desktop/api/Iads/nn-iads-iadsreplicapointer) interface sets the property described in the following table.</span></span> <span data-ttu-id="65ad8-107">Per altre informazioni, vedere [metodi della proprietà di interfaccia](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="65ad8-107">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="65ad8-108">Proprietà</span><span class="sxs-lookup"><span data-stu-id="65ad8-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="65ad8-109">**Count**</span><span class="sxs-lookup"><span data-stu-id="65ad8-109">**Count**</span></span>
<span data-ttu-id="65ad8-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="65ad8-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="65ad8-111">Numero di repliche esistenti.</span><span class="sxs-lookup"><span data-stu-id="65ad8-111">The number of existing replicas.</span></span>

<dt>

<span data-ttu-id="65ad8-112">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="65ad8-112">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="65ad8-113">Tipo di dati di scripting: **Long**</span><span class="sxs-lookup"><span data-stu-id="65ad8-113">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Count(
  [out] LONG* retval
);
HRESULT put_Count(
  [in] LONG lnCount
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="65ad8-114">**ReplicaAddressHints**</span><span class="sxs-lookup"><span data-stu-id="65ad8-114">**ReplicaAddressHints**</span></span>
<span data-ttu-id="65ad8-115"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="65ad8-115"></dt> <dd> <dl></span></span>

<span data-ttu-id="65ad8-116">Un indirizzo di rete suggerito come riferimento probabile a un nodo che conduce al server dei nomi.</span><span class="sxs-lookup"><span data-stu-id="65ad8-116">A network address suggested as a likely reference to a node leading to the name server.</span></span>

<dt>

<span data-ttu-id="65ad8-117">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="65ad8-117">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="65ad8-118">Tipo di dati di scripting: **Variant**</span><span class="sxs-lookup"><span data-stu-id="65ad8-118">Scripting data type: **VARIANT**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_ReplicaAddressHints(
  [out] VARIANT* retval
);
HRESULT put_ReplicaAddressHints(
  [in] VARIANT vReplicaAddressHints
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="65ad8-119">**ReplicaNumber**</span><span class="sxs-lookup"><span data-stu-id="65ad8-119">**ReplicaNumber**</span></span>
<span data-ttu-id="65ad8-120"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="65ad8-120"></dt> <dd> <dl></span></span>

<span data-ttu-id="65ad8-121">Numero di identificazione della replica.</span><span class="sxs-lookup"><span data-stu-id="65ad8-121">Identification number of the replica.</span></span>

<dt>

<span data-ttu-id="65ad8-122">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="65ad8-122">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="65ad8-123">Tipo di dati di scripting: **Long**</span><span class="sxs-lookup"><span data-stu-id="65ad8-123">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_ReplicaNumber(
  [out] LONG* retval
);
HRESULT put_ReplicaNumber(
  [in] LONG lnReplicaNumber
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="65ad8-124">**ReplicaType**</span><span class="sxs-lookup"><span data-stu-id="65ad8-124">**ReplicaType**</span></span>
<span data-ttu-id="65ad8-125"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="65ad8-125"></dt> <dd> <dl></span></span>

<span data-ttu-id="65ad8-126">Tipo di replica (Master, secondario o di sola lettura).</span><span class="sxs-lookup"><span data-stu-id="65ad8-126">Type of replica (master, secondary, or read-only.)</span></span>

<dt>

<span data-ttu-id="65ad8-127">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="65ad8-127">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="65ad8-128">Tipo di dati di scripting: **Long**</span><span class="sxs-lookup"><span data-stu-id="65ad8-128">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_ReplicaType(
  [out] LONG* retval
);
HRESULT put_ReplicaType(
  [in] LONG lnType
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="65ad8-129">**ServerName**</span><span class="sxs-lookup"><span data-stu-id="65ad8-129">**ServerName**</span></span>
<span data-ttu-id="65ad8-130"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="65ad8-130"></dt> <dd> <dl></span></span>

<span data-ttu-id="65ad8-131">Nome del server dei nomi che contiene la replica.</span><span class="sxs-lookup"><span data-stu-id="65ad8-131">Name of the name server holding the replica.</span></span>

<dt>

<span data-ttu-id="65ad8-132">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="65ad8-132">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="65ad8-133">Tipo di dati di scripting: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="65ad8-133">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_ServerName(
  [out] BSTR* retVal
);
HRESULT put_ServerName(
  [in] BSTR bstrServerName
);
```


</dt> </dl> </dd> </dl>

 

## <a name="requirements"></a><span data-ttu-id="65ad8-134">Requisiti</span><span class="sxs-lookup"><span data-stu-id="65ad8-134">Requirements</span></span>



| <span data-ttu-id="65ad8-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="65ad8-135">Requirement</span></span> | <span data-ttu-id="65ad8-136">Valore</span><span class="sxs-lookup"><span data-stu-id="65ad8-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="65ad8-137">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="65ad8-137">Minimum supported client</span></span><br/> | <span data-ttu-id="65ad8-138">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="65ad8-138">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="65ad8-139">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="65ad8-139">Minimum supported server</span></span><br/> | <span data-ttu-id="65ad8-140">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="65ad8-140">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="65ad8-141">Intestazione</span><span class="sxs-lookup"><span data-stu-id="65ad8-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="65ad8-142"><dt>IADs. h</dt></span><span class="sxs-lookup"><span data-stu-id="65ad8-142"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="65ad8-143">DLL</span><span class="sxs-lookup"><span data-stu-id="65ad8-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="65ad8-144"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="65ad8-144"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="65ad8-145">IID</span><span class="sxs-lookup"><span data-stu-id="65ad8-145">IID</span></span><br/>                      | <span data-ttu-id="65ad8-146">IID \_ IADsReplicaPointer è definito come F60FB803-4080-11D1-A3AC-00C04FB950DC</span><span class="sxs-lookup"><span data-stu-id="65ad8-146">IID\_IADsReplicaPointer is defined as F60FB803-4080-11D1-A3AC-00C04FB950DC</span></span><br/>   |



## <a name="see-also"></a><span data-ttu-id="65ad8-147">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="65ad8-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="65ad8-148">**IADsReplicaPointer**</span><span class="sxs-lookup"><span data-stu-id="65ad8-148">**IADsReplicaPointer**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsreplicapointer)
</dt> <dt>

[<span data-ttu-id="65ad8-149">**\_REPLICAPOINTER ADS**</span><span class="sxs-lookup"><span data-stu-id="65ad8-149">**ADS\_REPLICAPOINTER**</span></span>](/windows/win32/api/iads/ns-iads-ads_replicapointer)
</dt> </dl>

 

 






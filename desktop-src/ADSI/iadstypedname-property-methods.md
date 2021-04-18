---
title: Metodi di proprietà IADsTypedName (IADs. h)
description: Il metodo Property dell'interfaccia IADsTypedName imposta la proprietà descritta nella tabella seguente. Per altre informazioni, vedere Metodi della proprietà di interfaccia.
ms.assetid: 0097c7c0-91f9-4874-93f2-c24900054a49
ms.tgt_platform: multiple
keywords:
- Metodi di proprietà IADsTypedName ADSI
topic_type:
- apiref
api_name:
- IADsTypedName Property Methods
- IADsTypedName.ObjectName
- IADsTypedName.get_ObjectName
- IADsTypedName.put_ObjectName
- IADsTypedName.Level
- IADsTypedName.get_Level
- IADsTypedName.put_Level
- IADsTypedName.Interval
- IADsTypedName.get_Interval
- IADsTypedName.put_Interval
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a1a90e3c3950fb3912e2fe206048053bec6322be
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301476"
---
# <a name="iadstypedname-property-methods"></a><span data-ttu-id="973e8-105">Metodi di proprietà IADsTypedName</span><span class="sxs-lookup"><span data-stu-id="973e8-105">IADsTypedName Property Methods</span></span>

<span data-ttu-id="973e8-106">Il metodo Property dell'interfaccia [**IADsTypedName**](/windows/desktop/api/Iads/nn-iads-iadstypedname) imposta la proprietà descritta nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="973e8-106">The property method of the [**IADsTypedName**](/windows/desktop/api/Iads/nn-iads-iadstypedname) interface sets the property described in the following table.</span></span> <span data-ttu-id="973e8-107">Per altre informazioni, vedere [metodi della proprietà di interfaccia](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="973e8-107">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="973e8-108">Proprietà</span><span class="sxs-lookup"><span data-stu-id="973e8-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="973e8-109">**Interval**</span><span class="sxs-lookup"><span data-stu-id="973e8-109">**Interval**</span></span>
<span data-ttu-id="973e8-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="973e8-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="973e8-111">Frequenza di riferimento dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="973e8-111">The frequency of reference of the object.</span></span>

<dt>

<span data-ttu-id="973e8-112">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="973e8-112">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="973e8-113">Tipo di dati di scripting: **Long**</span><span class="sxs-lookup"><span data-stu-id="973e8-113">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Interval(
  [out] LONG* retval
);
HRESULT put_Interval(
  [in] LONG lnInterval
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="973e8-114">**Level**</span><span class="sxs-lookup"><span data-stu-id="973e8-114">**Level**</span></span>
<span data-ttu-id="973e8-115"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="973e8-115"></dt> <dd> <dl></span></span>

<span data-ttu-id="973e8-116">Livello di priorità associato all'oggetto.</span><span class="sxs-lookup"><span data-stu-id="973e8-116">The priority level associated with the object.</span></span>

<dt>

<span data-ttu-id="973e8-117">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="973e8-117">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="973e8-118">Tipo di dati di scripting: **Long**</span><span class="sxs-lookup"><span data-stu-id="973e8-118">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Level(
  [out] LONG* retval
);
HRESULT put_Level(
  [in] LONG lnLevel
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="973e8-119">**ObjectName**</span><span class="sxs-lookup"><span data-stu-id="973e8-119">**ObjectName**</span></span>
<span data-ttu-id="973e8-120"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="973e8-120"></dt> <dd> <dl></span></span>

<span data-ttu-id="973e8-121">Nome di un oggetto.</span><span class="sxs-lookup"><span data-stu-id="973e8-121">The name of an object.</span></span>

<dt>

<span data-ttu-id="973e8-122">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="973e8-122">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="973e8-123">Tipo di dati di scripting: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="973e8-123">Scripting data type: **BSTR**</span></span>
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

 

## <a name="requirements"></a><span data-ttu-id="973e8-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="973e8-124">Requirements</span></span>



| <span data-ttu-id="973e8-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="973e8-125">Requirement</span></span> | <span data-ttu-id="973e8-126">Valore</span><span class="sxs-lookup"><span data-stu-id="973e8-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="973e8-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="973e8-127">Minimum supported client</span></span><br/> | <span data-ttu-id="973e8-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="973e8-128">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="973e8-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="973e8-129">Minimum supported server</span></span><br/> | <span data-ttu-id="973e8-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="973e8-130">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="973e8-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="973e8-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="973e8-132"><dt>IADs. h</dt></span><span class="sxs-lookup"><span data-stu-id="973e8-132"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="973e8-133">DLL</span><span class="sxs-lookup"><span data-stu-id="973e8-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="973e8-134"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="973e8-134"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="973e8-135">IID</span><span class="sxs-lookup"><span data-stu-id="973e8-135">IID</span></span><br/>                      | <span data-ttu-id="973e8-136">IID \_ IADsTypedName è definito come B371A349-4080-11D1-A3AC-00C04FB950DC</span><span class="sxs-lookup"><span data-stu-id="973e8-136">IID\_IADsTypedName is defined as B371A349-4080-11D1-A3AC-00C04FB950DC</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="973e8-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="973e8-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="973e8-138">**IADsTypedName**</span><span class="sxs-lookup"><span data-stu-id="973e8-138">**IADsTypedName**</span></span>](/windows/desktop/api/Iads/nn-iads-iadstypedname)
</dt> <dt>

[<span data-ttu-id="973e8-139">**ADS \_ digitato**</span><span class="sxs-lookup"><span data-stu-id="973e8-139">**ADS\_TYPEDNAME**</span></span>](/windows/win32/api/iads/ns-iads-ads_typedname)
</dt> </dl>

 

 






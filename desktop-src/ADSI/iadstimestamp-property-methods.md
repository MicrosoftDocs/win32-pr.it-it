---
title: Metodi di proprietà IADsTimestamp (IADs. h)
description: Il metodo Property dell'interfaccia IADsTimestamp imposta la proprietà descritta nella tabella seguente. Per altre informazioni, vedere Metodi della proprietà di interfaccia.
ms.assetid: 0f00d270-3c11-4c60-95b3-178130e31caa
ms.tgt_platform: multiple
keywords:
- Metodi di proprietà IADsTimestamp ADSI
topic_type:
- apiref
api_name:
- IADsTimestamp Property Methods
- IADsTimestamp.WholeSeconds
- IADsTimestamp.get_WholeSeconds
- IADsTimestamp.put_WholeSeconds
- IADsTimestamp.EventID
- IADsTimestamp.get_EventID
- IADsTimestamp.put_EventID
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a77db7a6a3b3814cd10beca5da5e3166ab1b61a2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476348"
---
# <a name="iadstimestamp-property-methods"></a><span data-ttu-id="62c36-105">Metodi di proprietà IADsTimestamp</span><span class="sxs-lookup"><span data-stu-id="62c36-105">IADsTimestamp Property Methods</span></span>

<span data-ttu-id="62c36-106">Il metodo Property dell'interfaccia [**IADsTimestamp**](/windows/desktop/api/Iads/nn-iads-iadstimestamp) imposta la proprietà descritta nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="62c36-106">The property method of the [**IADsTimestamp**](/windows/desktop/api/Iads/nn-iads-iadstimestamp) interface sets the property described in the following table.</span></span> <span data-ttu-id="62c36-107">Per altre informazioni, vedere [metodi della proprietà di interfaccia](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="62c36-107">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="62c36-108">Proprietà</span><span class="sxs-lookup"><span data-stu-id="62c36-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="62c36-109">**EventID**</span><span class="sxs-lookup"><span data-stu-id="62c36-109">**EventID**</span></span>
<span data-ttu-id="62c36-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="62c36-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="62c36-111">Identificatore dell'evento.</span><span class="sxs-lookup"><span data-stu-id="62c36-111">An event identifier.</span></span>

<dt>

<span data-ttu-id="62c36-112">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="62c36-112">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="62c36-113">Tipo di dati di scripting: **Long**</span><span class="sxs-lookup"><span data-stu-id="62c36-113">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_EventID(
  [out] LONG* retval
);
HRESULT put_EventID(
  [in] LONG lnEventID
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="62c36-114">**WholeSeconds**</span><span class="sxs-lookup"><span data-stu-id="62c36-114">**WholeSeconds**</span></span>
<span data-ttu-id="62c36-115"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="62c36-115"></dt> <dd> <dl></span></span>

<span data-ttu-id="62c36-116">Numero di secondi con valore zero 12:00 AM, gennaio 1970, UTC.</span><span class="sxs-lookup"><span data-stu-id="62c36-116">Number of seconds with zero value being 12:00 AM, January 1970, UTC.</span></span>

<dt>

<span data-ttu-id="62c36-117">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="62c36-117">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="62c36-118">Tipo di dati di scripting: **Long**</span><span class="sxs-lookup"><span data-stu-id="62c36-118">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_WholeSeconds(
  [out] LONG* retVal
);
HRESULT put_WholeSeconds(
  [in] LONG lnWholeSeconds
);
```


</dt> </dl> </dd> </dl>

 

## <a name="requirements"></a><span data-ttu-id="62c36-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="62c36-119">Requirements</span></span>



| <span data-ttu-id="62c36-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="62c36-120">Requirement</span></span> | <span data-ttu-id="62c36-121">Valore</span><span class="sxs-lookup"><span data-stu-id="62c36-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="62c36-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="62c36-122">Minimum supported client</span></span><br/> | <span data-ttu-id="62c36-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="62c36-123">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="62c36-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="62c36-124">Minimum supported server</span></span><br/> | <span data-ttu-id="62c36-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="62c36-125">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="62c36-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="62c36-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="62c36-127"><dt>IADs. h</dt></span><span class="sxs-lookup"><span data-stu-id="62c36-127"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="62c36-128">DLL</span><span class="sxs-lookup"><span data-stu-id="62c36-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="62c36-129"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="62c36-129"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="62c36-130">IID</span><span class="sxs-lookup"><span data-stu-id="62c36-130">IID</span></span><br/>                      | <span data-ttu-id="62c36-131">IID \_ IADsTimestamp è definito come B2F5A901-4080-11D1-A3AC-00C04FB950DC</span><span class="sxs-lookup"><span data-stu-id="62c36-131">IID\_IADsTimestamp is defined as B2F5A901-4080-11D1-A3AC-00C04FB950DC</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="62c36-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="62c36-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62c36-133">**IADsTimestamp**</span><span class="sxs-lookup"><span data-stu-id="62c36-133">**IADsTimestamp**</span></span>](/windows/desktop/api/Iads/nn-iads-iadstimestamp)
</dt> <dt>

[<span data-ttu-id="62c36-134">**\_timestamp ADS**</span><span class="sxs-lookup"><span data-stu-id="62c36-134">**ADS\_TIMESTAMP**</span></span>](/windows/win32/api/iads/ns-iads-ads_timestamp)
</dt> </dl>

 

 






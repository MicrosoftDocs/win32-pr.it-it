---
title: Metodi di proprietà IADsBackLink (IADs. h)
description: Il metodo Property dell'interfaccia IADsBackLink imposta la proprietà descritta nella tabella seguente. Per altre informazioni, vedere Metodi della proprietà di interfaccia.
ms.assetid: 0a66fa6d-1bf5-4ff0-8bbd-625a69cf9594
ms.tgt_platform: multiple
keywords:
- Metodi di proprietà IADsBackLink ADSI
topic_type:
- apiref
api_name:
- IADsBackLink Property Methods
- IADsBackLink.RemoteID
- IADsBackLink.get_RemoteID
- IADsBackLink.put_RemoteID
- IADsBackLink.ObjectName
- IADsBackLink.get_ObjectName
- IADsBackLink.put_ObjectName
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c2220fff3a18b0822c0167b387ec10c324d95aa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120755"
---
# <a name="iadsbacklink-property-methods"></a><span data-ttu-id="09dd3-105">Metodi di proprietà IADsBackLink</span><span class="sxs-lookup"><span data-stu-id="09dd3-105">IADsBackLink Property Methods</span></span>

<span data-ttu-id="09dd3-106">Il metodo Property dell'interfaccia [**IADsBackLink**](/windows/desktop/api/Iads/nn-iads-iadsbacklink) imposta la proprietà descritta nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="09dd3-106">The property method of the [**IADsBackLink**](/windows/desktop/api/Iads/nn-iads-iadsbacklink) interface sets the property described in the following table.</span></span> <span data-ttu-id="09dd3-107">Per altre informazioni, vedere [metodi della proprietà di interfaccia](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="09dd3-107">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="09dd3-108">Proprietà</span><span class="sxs-lookup"><span data-stu-id="09dd3-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="09dd3-109">**ObjectName**</span><span class="sxs-lookup"><span data-stu-id="09dd3-109">**ObjectName**</span></span>
<span data-ttu-id="09dd3-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="09dd3-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="09dd3-111">Nome di un oggetto a cui è associato l'attributo **back link** .</span><span class="sxs-lookup"><span data-stu-id="09dd3-111">The name of an object the **Back Link** attribute is attached to.</span></span>

<dt>

<span data-ttu-id="09dd3-112">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="09dd3-112">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="09dd3-113">Tipo di dati di scripting: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="09dd3-113">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_ObjectName(
  [out] BSTR* retval
);
HRESULT put_ObjectName(
  [in] BSTR bstrSubjectName
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="09dd3-114">**RemoteID**</span><span class="sxs-lookup"><span data-stu-id="09dd3-114">**RemoteID**</span></span>
<span data-ttu-id="09dd3-115"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="09dd3-115"></dt> <dd> <dl></span></span>

<span data-ttu-id="09dd3-116">Identificatore del server remoto che richiede un riferimento esterno all'oggetto specificato da **ObjectName**.</span><span class="sxs-lookup"><span data-stu-id="09dd3-116">The identifier of the remote server that requires an external reference of the object specified by **ObjectName**.</span></span>

<dt>

<span data-ttu-id="09dd3-117">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="09dd3-117">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="09dd3-118">Tipo di dati di scripting: **Long**</span><span class="sxs-lookup"><span data-stu-id="09dd3-118">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_RemoteID(
  [out] LONG* retVal
);
HRESULT put_RemoteID(
  [in] LONG bstrProtectedAttrName
);
```


</dt> </dl> </dd> </dl>

 

## <a name="requirements"></a><span data-ttu-id="09dd3-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="09dd3-119">Requirements</span></span>



| <span data-ttu-id="09dd3-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="09dd3-120">Requirement</span></span> | <span data-ttu-id="09dd3-121">Valore</span><span class="sxs-lookup"><span data-stu-id="09dd3-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="09dd3-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="09dd3-122">Minimum supported client</span></span><br/> | <span data-ttu-id="09dd3-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="09dd3-123">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="09dd3-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="09dd3-124">Minimum supported server</span></span><br/> | <span data-ttu-id="09dd3-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="09dd3-125">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="09dd3-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="09dd3-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="09dd3-127"><dt>IADs. h</dt></span><span class="sxs-lookup"><span data-stu-id="09dd3-127"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="09dd3-128">DLL</span><span class="sxs-lookup"><span data-stu-id="09dd3-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="09dd3-129"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="09dd3-129"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="09dd3-130">IID</span><span class="sxs-lookup"><span data-stu-id="09dd3-130">IID</span></span><br/>                      | <span data-ttu-id="09dd3-131">IID \_ IADsBackLink è definito come FD1302BD-4080-11D1-A3AC-00C04FB950DC</span><span class="sxs-lookup"><span data-stu-id="09dd3-131">IID\_IADsBackLink is defined as FD1302BD-4080-11D1-A3AC-00C04FB950DC</span></span><br/>         |



## <a name="see-also"></a><span data-ttu-id="09dd3-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="09dd3-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="09dd3-133">**IADsBackLink**</span><span class="sxs-lookup"><span data-stu-id="09dd3-133">**IADsBackLink**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsbacklink)
</dt> <dt>

[<span data-ttu-id="09dd3-134">**\_BACKLINK annunci**</span><span class="sxs-lookup"><span data-stu-id="09dd3-134">**ADS\_BACKLINK**</span></span>](/windows/win32/api/iads/ns-iads-ads_backlink)
</dt> </dl>

 

 






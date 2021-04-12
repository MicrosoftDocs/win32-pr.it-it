---
title: Metodi di proprietà IADsAcl (IADs. h)
description: Il metodo Property dell'interfaccia IADsAcl imposta la proprietà descritta nella tabella seguente. Per altre informazioni, vedere Metodi della proprietà di interfaccia.
ms.assetid: eb4786d7-d366-4924-8255-dc28ea47a246
ms.tgt_platform: multiple
keywords:
- Metodi di proprietà IADsAcl ADSI
topic_type:
- apiref
api_name:
- IADsAcl Property Methods
- IADsAcl.ProtectedAttrName
- IADsAcl.get_ProtecteAttrName
- IADsAcl.put_ProtectedAttrName
- IADsAcl.SubjectName
- IADsAcl.get_SubjectName
- IADsAcl.put_SubjectName
- IADsAcl.Privileges
- IADsAcl.get_Privileges
- IADsAcl.put_Privileges
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9d8afb1ba3cbf7749ad8e3d14fa970662715909
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478125"
---
# <a name="iadsacl-property-methods"></a><span data-ttu-id="850fa-105">Metodi di proprietà IADsAcl</span><span class="sxs-lookup"><span data-stu-id="850fa-105">IADsAcl Property Methods</span></span>

<span data-ttu-id="850fa-106">Il metodo Property dell'interfaccia [**IADsAcl**](/windows/desktop/api/Iads/nn-iads-iadsacl) imposta la proprietà descritta nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="850fa-106">The property method of the [**IADsAcl**](/windows/desktop/api/Iads/nn-iads-iadsacl) interface sets the property described in the following table.</span></span> <span data-ttu-id="850fa-107">Per altre informazioni, vedere [metodi della proprietà di interfaccia](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="850fa-107">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="850fa-108">Proprietà</span><span class="sxs-lookup"><span data-stu-id="850fa-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="850fa-109">**Privilegi**</span><span class="sxs-lookup"><span data-stu-id="850fa-109">**Privileges**</span></span>
<span data-ttu-id="850fa-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="850fa-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="850fa-111">Impostazioni dei privilegi.</span><span class="sxs-lookup"><span data-stu-id="850fa-111">Privilege settings.</span></span>

<dt>

<span data-ttu-id="850fa-112">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="850fa-112">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="850fa-113">Tipo di dati di scripting: **Long**</span><span class="sxs-lookup"><span data-stu-id="850fa-113">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Privileges(
  [out] LONG* retval
);
HRESULT put_Privileges(
  [in] LONG lnPrivileges
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="850fa-114">**ProtectedAttrName**</span><span class="sxs-lookup"><span data-stu-id="850fa-114">**ProtectedAttrName**</span></span>
<span data-ttu-id="850fa-115"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="850fa-115"></dt> <dd> <dl></span></span>

<span data-ttu-id="850fa-116">Nome di un attributo protetto.</span><span class="sxs-lookup"><span data-stu-id="850fa-116">Name of a protected attribute.</span></span>

<dt>

<span data-ttu-id="850fa-117">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="850fa-117">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="850fa-118">Tipo di dati di scripting: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="850fa-118">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_ProtecteAttrName(
  [out] BSTR* retVal
);
HRESULT put_ProtectedAttrName(
  [in] BSTR bstrProtectedAttrName
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="850fa-119">**SubjectName**</span><span class="sxs-lookup"><span data-stu-id="850fa-119">**SubjectName**</span></span>
<span data-ttu-id="850fa-120"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="850fa-120"></dt> <dd> <dl></span></span>

<span data-ttu-id="850fa-121">Nome dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="850fa-121">Name of the subject.</span></span>

<dt>

<span data-ttu-id="850fa-122">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="850fa-122">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="850fa-123">Tipo di dati di scripting: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="850fa-123">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_SubjectName(
  [out] BSTR* retval
);
HRESULT put_SubjectName(
  [in] BSTR bstrSubjectName
);
```


</dt> </dl> </dd> </dl>

 

## <a name="requirements"></a><span data-ttu-id="850fa-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="850fa-124">Requirements</span></span>



| <span data-ttu-id="850fa-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="850fa-125">Requirement</span></span> | <span data-ttu-id="850fa-126">Valore</span><span class="sxs-lookup"><span data-stu-id="850fa-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="850fa-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="850fa-127">Minimum supported client</span></span><br/> | <span data-ttu-id="850fa-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="850fa-128">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="850fa-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="850fa-129">Minimum supported server</span></span><br/> | <span data-ttu-id="850fa-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="850fa-130">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="850fa-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="850fa-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="850fa-132"><dt>IADs. h</dt></span><span class="sxs-lookup"><span data-stu-id="850fa-132"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="850fa-133">DLL</span><span class="sxs-lookup"><span data-stu-id="850fa-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="850fa-134"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="850fa-134"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="850fa-135">IID</span><span class="sxs-lookup"><span data-stu-id="850fa-135">IID</span></span><br/>                      | <span data-ttu-id="850fa-136">IID \_ IADsAcl è definito come 8452D3AB-0869-11D1-A377-00C04FB950DC</span><span class="sxs-lookup"><span data-stu-id="850fa-136">IID\_IADsAcl is defined as 8452D3AB-0869-11D1-A377-00C04FB950DC</span></span><br/>              |



## <a name="see-also"></a><span data-ttu-id="850fa-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="850fa-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="850fa-138">**IADsAcl**</span><span class="sxs-lookup"><span data-stu-id="850fa-138">**IADsAcl**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsacl)
</dt> </dl>

 

 






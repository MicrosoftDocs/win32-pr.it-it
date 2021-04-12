---
title: Metodi di proprietà IADsEmail (IADs. h)
description: Il metodo Property dell'interfaccia IADsEmail imposta la proprietà descritta nella tabella seguente. Per altre informazioni, vedere Metodi della proprietà di interfaccia.
ms.assetid: 605ba62f-b15a-4411-839b-c4ad8acedd8a
ms.tgt_platform: multiple
keywords:
- Metodi di proprietà IADsEmail ADSI
topic_type:
- apiref
api_name:
- IADsEmail Property Methods
- IADsEmail.Type
- IADsEmail.get_Type
- IADsEmail.put_Type
- IADsEmail.Address
- IADsEmail.get_Address
- IADsEmail.put_Address
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1956d5544b36cdaefcdd9d712ae99001d42279d0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400829"
---
# <a name="iadsemail-property-methods"></a><span data-ttu-id="16bbc-105">Metodi di proprietà IADsEmail</span><span class="sxs-lookup"><span data-stu-id="16bbc-105">IADsEmail Property Methods</span></span>

<span data-ttu-id="16bbc-106">Il metodo Property dell'interfaccia [**IADsEmail**](/windows/desktop/api/Iads/nn-iads-iadsemail) imposta la proprietà descritta nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="16bbc-106">The property method of the [**IADsEmail**](/windows/desktop/api/Iads/nn-iads-iadsemail) interface sets the property described in the following table.</span></span> <span data-ttu-id="16bbc-107">Per altre informazioni, vedere [metodi della proprietà di interfaccia](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="16bbc-107">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="16bbc-108">Proprietà</span><span class="sxs-lookup"><span data-stu-id="16bbc-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="16bbc-109">**Indirizzo**</span><span class="sxs-lookup"><span data-stu-id="16bbc-109">**Address**</span></span>
<span data-ttu-id="16bbc-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="16bbc-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="16bbc-111">Indirizzo di posta elettronica dell'utente.</span><span class="sxs-lookup"><span data-stu-id="16bbc-111">The email address of the user.</span></span>

<dt>

<span data-ttu-id="16bbc-112">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="16bbc-112">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="16bbc-113">Tipo di dati di scripting: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="16bbc-113">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Address(
  [out] BSTR* retval
);
HRESULT put_Address(
  [in] BSTR bstrAddress
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="16bbc-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="16bbc-114">**Type**</span></span>
<span data-ttu-id="16bbc-115"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="16bbc-115"></dt> <dd> <dl></span></span>

<span data-ttu-id="16bbc-116">Tipo di messaggio di posta elettronica.</span><span class="sxs-lookup"><span data-stu-id="16bbc-116">The type of the email message.</span></span>

<dt>

<span data-ttu-id="16bbc-117">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="16bbc-117">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="16bbc-118">Tipo di dati di scripting: **Long**</span><span class="sxs-lookup"><span data-stu-id="16bbc-118">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Type(
  [out] LONG* retVal
);
HRESULT put_Type(
  [in] LONG lnType
);
```


</dt> </dl> </dd> </dl>

 

## <a name="requirements"></a><span data-ttu-id="16bbc-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="16bbc-119">Requirements</span></span>



| <span data-ttu-id="16bbc-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="16bbc-120">Requirement</span></span> | <span data-ttu-id="16bbc-121">Valore</span><span class="sxs-lookup"><span data-stu-id="16bbc-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="16bbc-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="16bbc-122">Minimum supported client</span></span><br/> | <span data-ttu-id="16bbc-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="16bbc-123">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="16bbc-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="16bbc-124">Minimum supported server</span></span><br/> | <span data-ttu-id="16bbc-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="16bbc-125">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="16bbc-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="16bbc-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="16bbc-127"><dt>IADs. h</dt></span><span class="sxs-lookup"><span data-stu-id="16bbc-127"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="16bbc-128">DLL</span><span class="sxs-lookup"><span data-stu-id="16bbc-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="16bbc-129"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="16bbc-129"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="16bbc-130">IID</span><span class="sxs-lookup"><span data-stu-id="16bbc-130">IID</span></span><br/>                      | <span data-ttu-id="16bbc-131">IID \_ IADsEmail è definito come 97AF011A-478E-11D1-A3B4-00C04FB950DC</span><span class="sxs-lookup"><span data-stu-id="16bbc-131">IID\_IADsEmail is defined as 97AF011A-478E-11D1-A3B4-00C04FB950DC</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="16bbc-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="16bbc-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="16bbc-133">**IADsEmail**</span><span class="sxs-lookup"><span data-stu-id="16bbc-133">**IADsEmail**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsemail)
</dt> <dt>

[<span data-ttu-id="16bbc-134">**\_posta elettronica ADS**</span><span class="sxs-lookup"><span data-stu-id="16bbc-134">**ADS\_EMAIL**</span></span>](/windows/win32/api/iads/ns-iads-ads_email)
</dt> </dl>

 

 






---
title: Metodi di proprietà IADsPostalAddress (IADs. h)
description: Il metodo Property dell'interfaccia IADsPostalAddress imposta la proprietà descritta nella tabella seguente. Per altre informazioni, vedere Metodi della proprietà di interfaccia.
ms.assetid: f7e61c69-f3a6-4ca6-a276-3cd859252571
ms.tgt_platform: multiple
keywords:
- Metodi di proprietà IADsPostalAddress ADSI
topic_type:
- apiref
api_name:
- IADsPostalAddress Property Methods
- IADsPostalAddress.PostalAddress
- IADsPostalAddress.get_PostalAddress
- IADsPostalAddress.put_PostalAddress
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a9d8eeaac8fa258a2df1452b8aa261ee59b3cc85
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302136"
---
# <a name="iadspostaladdress-property-methods"></a><span data-ttu-id="83b66-105">Metodi di proprietà IADsPostalAddress</span><span class="sxs-lookup"><span data-stu-id="83b66-105">IADsPostalAddress Property Methods</span></span>

<span data-ttu-id="83b66-106">Il metodo Property dell'interfaccia [**IADsPostalAddress**](/windows/desktop/api/Iads/nn-iads-iadspostaladdress) imposta la proprietà descritta nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="83b66-106">The property method of the [**IADsPostalAddress**](/windows/desktop/api/Iads/nn-iads-iadspostaladdress) interface sets the property described in the following table.</span></span> <span data-ttu-id="83b66-107">Per altre informazioni, vedere [metodi della proprietà di interfaccia](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="83b66-107">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="83b66-108">Proprietà</span><span class="sxs-lookup"><span data-stu-id="83b66-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="83b66-109">**PostalAddress**</span><span class="sxs-lookup"><span data-stu-id="83b66-109">**PostalAddress**</span></span>
<span data-ttu-id="83b66-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="83b66-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="83b66-111">Matrice di sei stringhe che contiene l'indirizzo postale dell'utente.</span><span class="sxs-lookup"><span data-stu-id="83b66-111">An array of six strings holding the postal address of the user.</span></span>

<dt>

<span data-ttu-id="83b66-112">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="83b66-112">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="83b66-113">Tipo di dati di scripting: **Variant**</span><span class="sxs-lookup"><span data-stu-id="83b66-113">Scripting data type: **VARIANT**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_PostalAddress(
  [out] VARIANT* retVal
);
HRESULT put_PostalAddress(
  [in] VARIANT vPostalAddress
);
```


</dt> </dl> </dd> </dl>

 

## <a name="requirements"></a><span data-ttu-id="83b66-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="83b66-114">Requirements</span></span>



| <span data-ttu-id="83b66-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="83b66-115">Requirement</span></span> | <span data-ttu-id="83b66-116">Valore</span><span class="sxs-lookup"><span data-stu-id="83b66-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="83b66-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="83b66-117">Minimum supported client</span></span><br/> | <span data-ttu-id="83b66-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="83b66-118">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="83b66-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="83b66-119">Minimum supported server</span></span><br/> | <span data-ttu-id="83b66-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="83b66-120">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="83b66-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="83b66-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="83b66-122"><dt>IADs. h</dt></span><span class="sxs-lookup"><span data-stu-id="83b66-122"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="83b66-123">DLL</span><span class="sxs-lookup"><span data-stu-id="83b66-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="83b66-124"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="83b66-124"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="83b66-125">IID</span><span class="sxs-lookup"><span data-stu-id="83b66-125">IID</span></span><br/>                      | <span data-ttu-id="83b66-126">IID \_ IADsPostalAddress è definito come 7ADECF29-4680-11D1-A3B4-00C04FB950DC</span><span class="sxs-lookup"><span data-stu-id="83b66-126">IID\_IADsPostalAddress is defined as 7ADECF29-4680-11D1-A3B4-00C04FB950DC</span></span><br/>    |



## <a name="see-also"></a><span data-ttu-id="83b66-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="83b66-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="83b66-128">**IADsPostalAddress**</span><span class="sxs-lookup"><span data-stu-id="83b66-128">**IADsPostalAddress**</span></span>](/windows/desktop/api/Iads/nn-iads-iadspostaladdress)
</dt> <dt>

[<span data-ttu-id="83b66-129">**\_POSTALADDRESS ADS**</span><span class="sxs-lookup"><span data-stu-id="83b66-129">**ADS\_POSTALADDRESS**</span></span>](/windows/win32/api/iads/ns-iads-ads_postaladdress)
</dt> </dl>

 

 






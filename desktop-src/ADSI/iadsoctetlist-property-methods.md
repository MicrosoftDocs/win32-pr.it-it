---
title: Metodi di proprietà IADsOctetList (IADs. h)
description: Il metodo Property dell'interfaccia IADsOctetList imposta la proprietà descritta nella tabella seguente. Per altre informazioni, vedere Metodi della proprietà di interfaccia.
ms.assetid: 6fe29a0d-dd53-4cc2-8152-22a0a2756c2c
ms.tgt_platform: multiple
keywords:
- Metodi di proprietà IADsOctetList ADSI
topic_type:
- apiref
api_name:
- IADsOctetList Property Methods
- IADsOctetList.OctetList
- IADsOctetList.get_OctetList
- IADsOctetList.put_OctetList
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe3631adaf00cf599214296e1792ffab8697ba5e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964658"
---
# <a name="iadsoctetlist-property-methods"></a><span data-ttu-id="53daa-105">Metodi di proprietà IADsOctetList</span><span class="sxs-lookup"><span data-stu-id="53daa-105">IADsOctetList Property Methods</span></span>

<span data-ttu-id="53daa-106">Il metodo Property dell'interfaccia [**IADsOctetList**](/windows/desktop/api/Iads/nn-iads-iadsoctetlist) imposta la proprietà descritta nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="53daa-106">The property method of the [**IADsOctetList**](/windows/desktop/api/Iads/nn-iads-iadsoctetlist) interface sets the property described in the following table.</span></span> <span data-ttu-id="53daa-107">Per altre informazioni, vedere [metodi della proprietà di interfaccia](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="53daa-107">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="53daa-108">Proprietà</span><span class="sxs-lookup"><span data-stu-id="53daa-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="53daa-109">**Ottetto**</span><span class="sxs-lookup"><span data-stu-id="53daa-109">**OctetList**</span></span>
<span data-ttu-id="53daa-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="53daa-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="53daa-111">Sequenza ordinata di matrici di byte.</span><span class="sxs-lookup"><span data-stu-id="53daa-111">An ordered sequence of byte arrays.</span></span>

<dt>

<span data-ttu-id="53daa-112">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="53daa-112">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="53daa-113">Tipo di dati di scripting: **Variant**</span><span class="sxs-lookup"><span data-stu-id="53daa-113">Scripting data type: **VARIANT**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_OctetList(
  [out] VARIANT* retVal
);
HRESULT put_OctetList(
  [in] VARIANT vOctetList
);
```


</dt> </dl> </dd> </dl>

 

## <a name="requirements"></a><span data-ttu-id="53daa-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="53daa-114">Requirements</span></span>



| <span data-ttu-id="53daa-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="53daa-115">Requirement</span></span> | <span data-ttu-id="53daa-116">Valore</span><span class="sxs-lookup"><span data-stu-id="53daa-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="53daa-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="53daa-117">Minimum supported client</span></span><br/> | <span data-ttu-id="53daa-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="53daa-118">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="53daa-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="53daa-119">Minimum supported server</span></span><br/> | <span data-ttu-id="53daa-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="53daa-120">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="53daa-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="53daa-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="53daa-122"><dt>IADs. h</dt></span><span class="sxs-lookup"><span data-stu-id="53daa-122"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="53daa-123">DLL</span><span class="sxs-lookup"><span data-stu-id="53daa-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="53daa-124"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="53daa-124"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="53daa-125">IID</span><span class="sxs-lookup"><span data-stu-id="53daa-125">IID</span></span><br/>                      | <span data-ttu-id="53daa-126">IID \_ IADsOctetList è definito come 7B28B80F-4680-11D1-A3B4-00C04FB950DC</span><span class="sxs-lookup"><span data-stu-id="53daa-126">IID\_IADsOctetList is defined as 7B28B80F-4680-11D1-A3B4-00C04FB950DC</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="53daa-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="53daa-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="53daa-128">**IADsOctetList**</span><span class="sxs-lookup"><span data-stu-id="53daa-128">**IADsOctetList**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsoctetlist)
</dt> <dt>

[<span data-ttu-id="53daa-129">**\_elenco degli ottetti Ads \_**</span><span class="sxs-lookup"><span data-stu-id="53daa-129">**ADS\_OCTET\_LIST**</span></span>](/windows/desktop/api/Iads/ns-iads-ads_octet_list)
</dt> </dl>

 

 






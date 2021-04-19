---
title: Metodi di proprietà IADsCaseIgnoreList (IADs. h)
description: Il metodo Property dell'interfaccia IADsCaseIgnoreList imposta la proprietà descritta nella tabella seguente. Per altre informazioni, vedere Metodi della proprietà di interfaccia.
ms.assetid: 4f73adbf-abe3-4552-a3e4-19cff22e0ad0
ms.tgt_platform: multiple
keywords:
- Metodi di proprietà IADsCaseIgnoreList ADSI
topic_type:
- apiref
api_name:
- IADsCaseIgnoreList Property Methods
- IADsCaseIgnoreList.CaseIgnoreList
- IADsCaseIgnoreList.get_CaseIgnoreList
- IADsCaseIgnoreList.put_CaseIgnoreList
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5aabf26508c3e38e117ad25721af8bece5d69b1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302149"
---
# <a name="iadscaseignorelist-property-methods"></a><span data-ttu-id="677c4-105">Metodi di proprietà IADsCaseIgnoreList</span><span class="sxs-lookup"><span data-stu-id="677c4-105">IADsCaseIgnoreList Property Methods</span></span>

<span data-ttu-id="677c4-106">Il metodo Property dell'interfaccia [**IADsCaseIgnoreList**](/windows/desktop/api/Iads/nn-iads-iadscaseignorelist) imposta la proprietà descritta nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="677c4-106">The property method of the [**IADsCaseIgnoreList**](/windows/desktop/api/Iads/nn-iads-iadscaseignorelist) interface sets the property described in the following table.</span></span> <span data-ttu-id="677c4-107">Per altre informazioni, vedere [metodi della proprietà di interfaccia](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="677c4-107">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="677c4-108">Proprietà</span><span class="sxs-lookup"><span data-stu-id="677c4-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="677c4-109">**CaseIgnoreList**</span><span class="sxs-lookup"><span data-stu-id="677c4-109">**CaseIgnoreList**</span></span>
<span data-ttu-id="677c4-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="677c4-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="677c4-111">Sequenza ordinata di stringhe senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="677c4-111">An ordered sequence of case insensitive strings.</span></span>

<dt>

<span data-ttu-id="677c4-112">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="677c4-112">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="677c4-113">Tipo di dati di scripting: **Variant**</span><span class="sxs-lookup"><span data-stu-id="677c4-113">Scripting data type: **VARIANT**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_CaseIgnoreList(
  [out] VARIANT* retVal
);
HRESULT put_CaseIgnoreList(
  [in] VARIANT vCaseIgnoreList
);
```


</dt> </dl> </dd> </dl>

 

## <a name="requirements"></a><span data-ttu-id="677c4-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="677c4-114">Requirements</span></span>



| <span data-ttu-id="677c4-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="677c4-115">Requirement</span></span> | <span data-ttu-id="677c4-116">Valore</span><span class="sxs-lookup"><span data-stu-id="677c4-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="677c4-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="677c4-117">Minimum supported client</span></span><br/> | <span data-ttu-id="677c4-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="677c4-118">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="677c4-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="677c4-119">Minimum supported server</span></span><br/> | <span data-ttu-id="677c4-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="677c4-120">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="677c4-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="677c4-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="677c4-122"><dt>IADs. h</dt></span><span class="sxs-lookup"><span data-stu-id="677c4-122"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="677c4-123">DLL</span><span class="sxs-lookup"><span data-stu-id="677c4-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="677c4-124"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="677c4-124"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="677c4-125">IID</span><span class="sxs-lookup"><span data-stu-id="677c4-125">IID</span></span><br/>                      | <span data-ttu-id="677c4-126">IID \_ IADsCaseIgnoreList è definito come 7B66B533-4680-11D1-A3B4-00C04FB950DC</span><span class="sxs-lookup"><span data-stu-id="677c4-126">IID\_IADsCaseIgnoreList is defined as 7B66B533-4680-11D1-A3B4-00C04FB950DC</span></span><br/>   |



## <a name="see-also"></a><span data-ttu-id="677c4-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="677c4-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="677c4-128">**IADsCaseIgnoreList**</span><span class="sxs-lookup"><span data-stu-id="677c4-128">**IADsCaseIgnoreList**</span></span>](/windows/desktop/api/Iads/nn-iads-iadscaseignorelist)
</dt> <dt>

[<span data-ttu-id="677c4-129">**\_elenco CASEIGNORE \_ ADS**</span><span class="sxs-lookup"><span data-stu-id="677c4-129">**ADS\_CASEIGNORE\_LIST**</span></span>](/windows/desktop/api/Iads/ns-iads-ads_caseignore_list)
</dt> </dl>

 

 






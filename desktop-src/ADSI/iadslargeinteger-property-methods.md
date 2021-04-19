---
title: Metodi di proprietà IADsLargeInteger (IADs. h)
description: I metodi di proprietà dell'interfaccia IADsLargeInteger ottengono e impostano le proprietà descritte nella tabella seguente. Per altre informazioni, vedere Metodi della proprietà di interfaccia.
ms.assetid: 73e0c7fe-e468-4f92-9c9e-721bf00dd4bb
ms.tgt_platform: multiple
keywords:
- Metodi di proprietà IADsLargeInteger ADSI
topic_type:
- apiref
api_name:
- IADsLargeInteger Property Methods
- IADsLargeInteger.HighPart
- IADsLargeInteger.get_HighPart
- IADsLargeInteger.put_HighPart
- IADsLargeInteger.LowPart
- IADsLargeInteger.get_LowPart
- IADsLargeInteger.put_LowPart
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 097e9ae7387658f983c691e56e4f90ba40dea407
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302141"
---
# <a name="iadslargeinteger-property-methods"></a><span data-ttu-id="15258-105">Metodi di proprietà IADsLargeInteger</span><span class="sxs-lookup"><span data-stu-id="15258-105">IADsLargeInteger Property Methods</span></span>

<span data-ttu-id="15258-106">I metodi di proprietà dell'interfaccia [**IADsLargeInteger**](/windows/desktop/api/Iads/nn-iads-iadslargeinteger) ottengono e impostano le proprietà descritte nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="15258-106">The property methods of the [**IADsLargeInteger**](/windows/desktop/api/Iads/nn-iads-iadslargeinteger) interface get and set the properties described in the following table.</span></span> <span data-ttu-id="15258-107">Per altre informazioni, vedere [metodi della proprietà di interfaccia](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="15258-107">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="15258-108">Proprietà</span><span class="sxs-lookup"><span data-stu-id="15258-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="15258-109">**HighPart**</span><span class="sxs-lookup"><span data-stu-id="15258-109">**HighPart**</span></span>
<span data-ttu-id="15258-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="15258-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="15258-111">Parte superiore dell'intero.</span><span class="sxs-lookup"><span data-stu-id="15258-111">The high part of the integer.</span></span>

<dt>

<span data-ttu-id="15258-112">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="15258-112">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="15258-113">Tipo di dati di scripting: **Long**</span><span class="sxs-lookup"><span data-stu-id="15258-113">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_HighPart(
  [out] LONG* retval
);
HRESULT put_HighPart(
  [in] LONG lnHighPart
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="15258-114">**LowPart**</span><span class="sxs-lookup"><span data-stu-id="15258-114">**LowPart**</span></span>
<span data-ttu-id="15258-115"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="15258-115"></dt> <dd> <dl></span></span>

<span data-ttu-id="15258-116">Parte inferiore dell'intero.</span><span class="sxs-lookup"><span data-stu-id="15258-116">The low part of the integer.</span></span>

<dt>

<span data-ttu-id="15258-117">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="15258-117">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="15258-118">Tipo di dati di scripting: **Long**</span><span class="sxs-lookup"><span data-stu-id="15258-118">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_LowPart(
  [out] LONG* retval
);
HRESULT put_LowPart(
  [in] LONG lnLowPart
);
```


</dt> </dl> </dd> </dl>

 

## <a name="remarks"></a><span data-ttu-id="15258-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="15258-119">Remarks</span></span>

<span data-ttu-id="15258-120">Se largeInt è del tipo **LargeInteger** , il relativo valore viene specificato da quelli di **HighPart** e **LowPart** in base alla formula seguente.</span><span class="sxs-lookup"><span data-stu-id="15258-120">If largeInt is of the **LargeInteger** type, its value is specified by those of **HighPart** and **LowPart** according to the following formula.</span></span>


```VB
largeInt = HighPart * 2^32 + LowPart
```



## <a name="examples"></a><span data-ttu-id="15258-121">Esempio</span><span class="sxs-lookup"><span data-stu-id="15258-121">Examples</span></span>

<span data-ttu-id="15258-122">L'esempio di codice seguente Visual Basic imposta un valore Integer grande su 43937327281.</span><span class="sxs-lookup"><span data-stu-id="15258-122">The following Visual Basic code example sets a large integer to 43937327281.</span></span>


```VB
Dim LI As New LargeInteger
LI.HighPart = 10
LI.LowPart = 987654321
```



## <a name="requirements"></a><span data-ttu-id="15258-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="15258-123">Requirements</span></span>



| <span data-ttu-id="15258-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="15258-124">Requirement</span></span> | <span data-ttu-id="15258-125">Valore</span><span class="sxs-lookup"><span data-stu-id="15258-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="15258-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="15258-126">Minimum supported client</span></span><br/> | <span data-ttu-id="15258-127">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="15258-127">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="15258-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="15258-128">Minimum supported server</span></span><br/> | <span data-ttu-id="15258-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="15258-129">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="15258-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="15258-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="15258-131"><dt>IADs. h</dt></span><span class="sxs-lookup"><span data-stu-id="15258-131"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="15258-132">DLL</span><span class="sxs-lookup"><span data-stu-id="15258-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="15258-133"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="15258-133"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="15258-134">IID</span><span class="sxs-lookup"><span data-stu-id="15258-134">IID</span></span><br/>                      | <span data-ttu-id="15258-135">IID \_ IADsLargeInteger è definito come 9068270B-0939-11D1-8BE1-00C04FD8D503</span><span class="sxs-lookup"><span data-stu-id="15258-135">IID\_IADsLargeInteger is defined as 9068270B-0939-11D1-8BE1-00C04FD8D503</span></span><br/>     |



## <a name="see-also"></a><span data-ttu-id="15258-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="15258-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="15258-137">**IADsLargeInteger**</span><span class="sxs-lookup"><span data-stu-id="15258-137">**IADsLargeInteger**</span></span>](/windows/desktop/api/Iads/nn-iads-iadslargeinteger)
</dt> </dl>

 

 






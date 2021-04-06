---
title: Metodi di proprietà IADsPath (IADs. h)
description: Il metodo Property dell'interfaccia IADsPath imposta la proprietà descritta nella tabella seguente. Per altre informazioni, vedere Metodi della proprietà di interfaccia.
ms.assetid: 6fc7ce1a-575b-48c4-9f66-3ea22d60c96b
ms.tgt_platform: multiple
keywords:
- Metodi di proprietà IADsPath ADSI
topic_type:
- apiref
api_name:
- IADsPath Property Methods
- IADsPath.Type
- IADsPath.get_Type
- IADsPath.put_Type
- IADsPath.VolumeName
- IADsPath.get_VolumeName
- IADsPath.put_VolumeName
- IADsPath.Path
- IADsPath.get_Path
- IADsPath.put_Path
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5adcc1c60a9b678e99074ae3547d35c7ac8c7356
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742682"
---
# <a name="iadspath-property-methods"></a><span data-ttu-id="146c9-105">Metodi di proprietà IADsPath</span><span class="sxs-lookup"><span data-stu-id="146c9-105">IADsPath Property Methods</span></span>

<span data-ttu-id="146c9-106">Il metodo Property dell'interfaccia [**IADsPath**](/windows/desktop/api/Iads/nn-iads-iadspath) imposta la proprietà descritta nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="146c9-106">The property method of the [**IADsPath**](/windows/desktop/api/Iads/nn-iads-iadspath) interface sets the property described in the following table.</span></span> <span data-ttu-id="146c9-107">Per altre informazioni, vedere [metodi della proprietà di interfaccia](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="146c9-107">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="146c9-108">Proprietà</span><span class="sxs-lookup"><span data-stu-id="146c9-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="146c9-109">**Percorso**</span><span class="sxs-lookup"><span data-stu-id="146c9-109">**Path**</span></span>
<span data-ttu-id="146c9-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="146c9-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="146c9-111">Percorso di una directory del file system.</span><span class="sxs-lookup"><span data-stu-id="146c9-111">Path of a directory of the file system.</span></span>

<dt>

<span data-ttu-id="146c9-112">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="146c9-112">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="146c9-113">Tipo di dati di scripting: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="146c9-113">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Path(
  [out] BSTR* retval
);
HRESULT put_Path(
  [in] BSTR bstrPath
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="146c9-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="146c9-114">**Type**</span></span>
<span data-ttu-id="146c9-115"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="146c9-115"></dt> <dd> <dl></span></span>

<span data-ttu-id="146c9-116">Tipo di file del file system.</span><span class="sxs-lookup"><span data-stu-id="146c9-116">File type of the file system.</span></span>

<dt>

<span data-ttu-id="146c9-117">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="146c9-117">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="146c9-118">Tipo di dati di scripting: **Long**</span><span class="sxs-lookup"><span data-stu-id="146c9-118">Scripting data type: **LONG**</span></span>
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


</dt> </dl> </dd> <dt>

<span data-ttu-id="146c9-119">**NomeVolume**</span><span class="sxs-lookup"><span data-stu-id="146c9-119">**VolumeName**</span></span>
<span data-ttu-id="146c9-120"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="146c9-120"></dt> <dd> <dl></span></span>

<span data-ttu-id="146c9-121">Nome di un volume esistente del file system.</span><span class="sxs-lookup"><span data-stu-id="146c9-121">Name of an existing volume of the file system.</span></span>

<dt>

<span data-ttu-id="146c9-122">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="146c9-122">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="146c9-123">Tipo di dati di scripting: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="146c9-123">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_VolumeName(
  [out] BSTR* retval
);
HRESULT put_VolumeName(
  [in] BSTR bstrVolumeName
);
```


</dt> </dl> </dd> </dl>

 

## <a name="requirements"></a><span data-ttu-id="146c9-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="146c9-124">Requirements</span></span>



| <span data-ttu-id="146c9-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="146c9-125">Requirement</span></span> | <span data-ttu-id="146c9-126">Valore</span><span class="sxs-lookup"><span data-stu-id="146c9-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="146c9-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="146c9-127">Minimum supported client</span></span><br/> | <span data-ttu-id="146c9-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="146c9-128">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="146c9-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="146c9-129">Minimum supported server</span></span><br/> | <span data-ttu-id="146c9-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="146c9-130">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="146c9-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="146c9-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="146c9-132"><dt>IADs. h</dt></span><span class="sxs-lookup"><span data-stu-id="146c9-132"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="146c9-133">DLL</span><span class="sxs-lookup"><span data-stu-id="146c9-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="146c9-134"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="146c9-134"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="146c9-135">IID</span><span class="sxs-lookup"><span data-stu-id="146c9-135">IID</span></span><br/>                      | <span data-ttu-id="146c9-136">IID \_ IADsPath è definito come B287FCD5-4080-11D1-A3AC-00C04FB950DC</span><span class="sxs-lookup"><span data-stu-id="146c9-136">IID\_IADsPath is defined as B287FCD5-4080-11D1-A3AC-00C04FB950DC</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="146c9-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="146c9-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="146c9-138">**IADsPath**</span><span class="sxs-lookup"><span data-stu-id="146c9-138">**IADsPath**</span></span>](/windows/desktop/api/Iads/nn-iads-iadspath)
</dt> <dt>

[<span data-ttu-id="146c9-139">**\_percorso annunci**</span><span class="sxs-lookup"><span data-stu-id="146c9-139">**ADS\_PATH**</span></span>](/windows/win32/api/iads/ns-iads-ads_path)
</dt> </dl>

 

 






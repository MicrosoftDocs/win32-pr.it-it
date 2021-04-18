---
title: Metodo GetLicense IWMDRMLicense (wmdrmsdk. h)
description: Il metodo GetLicense recupera la licenza come dati XML o XMR.
ms.assetid: 63317841-fd13-4e83-8b99-e3cab1405050
keywords:
- Metodo GetLicense formato Windows Media
- Metodo GetLicense formato Windows Media, interfaccia IWMDRMLicense
- Interfaccia IWMDRMLicense-formato Windows Media, metodo GetLicense
topic_type:
- apiref
api_name:
- IWMDRMLicense.GetLicense
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d0692afb2ff127f9456e6da3c7546c67ae22ded
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328528"
---
# <a name="iwmdrmlicensegetlicense-method"></a><span data-ttu-id="977b4-106">Metodo IWMDRMLicense:: GetLicense</span><span class="sxs-lookup"><span data-stu-id="977b4-106">IWMDRMLicense::GetLicense method</span></span>

<span data-ttu-id="977b4-107">Il metodo **GetLicense** recupera la licenza come dati XML o XMR.</span><span class="sxs-lookup"><span data-stu-id="977b4-107">The **GetLicense** method retrieves the license as XML or XMR data.</span></span>

## <a name="syntax"></a><span data-ttu-id="977b4-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="977b4-108">Syntax</span></span>


```C++
HRESULT GetLicense(
  [out] BYTE  **ppbLicense,
  [out] DWORD *pcbLicense,
  [out] DWORD *pdwLicenseType
);
```



## <a name="parameters"></a><span data-ttu-id="977b4-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="977b4-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="977b4-110">*ppbLicense* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="977b4-110">*ppbLicense* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="977b4-111">Riceve la licenza.</span><span class="sxs-lookup"><span data-stu-id="977b4-111">Receives the license.</span></span>

</dd> <dt>

<span data-ttu-id="977b4-112">*pcbLicense* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="977b4-112">*pcbLicense* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="977b4-113">Riceve le dimensioni della licenza.</span><span class="sxs-lookup"><span data-stu-id="977b4-113">Receives the size of the license.</span></span>

</dd> <dt>

<span data-ttu-id="977b4-114">*pdwLicenseType* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="977b4-114">*pdwLicenseType* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="977b4-115">Riceve il tipo della licenza restituita.</span><span class="sxs-lookup"><span data-stu-id="977b4-115">Receives the type of the license returned.</span></span> <span data-ttu-id="977b4-116">Questo valore è impostato su una delle costanti nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="977b4-116">This value is set to one of the constants in the following table.</span></span>



| <span data-ttu-id="977b4-117">Costante</span><span class="sxs-lookup"><span data-stu-id="977b4-117">Constant</span></span>                  | <span data-ttu-id="977b4-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="977b4-118">Description</span></span>                            |
|---------------------------|----------------------------------------|
| <span data-ttu-id="977b4-119">\_XML di \_ tipo di licenza WMDRM \_</span><span class="sxs-lookup"><span data-stu-id="977b4-119">WMDRM\_LICENSE\_TYPE\_XML</span></span> | <span data-ttu-id="977b4-120">La licenza recuperata è formattata come XML.</span><span class="sxs-lookup"><span data-stu-id="977b4-120">Retrieved license is formatted as XML.</span></span> |
| <span data-ttu-id="977b4-121">\_tipo di licenza WMDRM \_ \_ XMR</span><span class="sxs-lookup"><span data-stu-id="977b4-121">WMDRM\_LICENSE\_TYPE\_XMR</span></span> | <span data-ttu-id="977b4-122">La licenza recuperata è formattata come XMR.</span><span class="sxs-lookup"><span data-stu-id="977b4-122">Retrieved license is formatted as XMR.</span></span> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="977b4-123">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="977b4-123">Return value</span></span>

<span data-ttu-id="977b4-124">Il metodo restituisce un valore **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="977b4-124">The method returns an **HRESULT**.</span></span> <span data-ttu-id="977b4-125">I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="977b4-125">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="977b4-126">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="977b4-126">Return code</span></span>                                                                          | <span data-ttu-id="977b4-127">Descrizione</span><span class="sxs-lookup"><span data-stu-id="977b4-127">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="977b4-128"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="977b4-128"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="977b4-129">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="977b4-129">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="977b4-130">Commenti</span><span class="sxs-lookup"><span data-stu-id="977b4-130">Remarks</span></span>

<span data-ttu-id="977b4-131">Nessuna.</span><span class="sxs-lookup"><span data-stu-id="977b4-131">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="977b4-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="977b4-132">Requirements</span></span>



| <span data-ttu-id="977b4-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="977b4-133">Requirement</span></span> | <span data-ttu-id="977b4-134">Valore</span><span class="sxs-lookup"><span data-stu-id="977b4-134">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="977b4-135">Intestazione</span><span class="sxs-lookup"><span data-stu-id="977b4-135">Header</span></span><br/>  | <dl> <span data-ttu-id="977b4-136"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="977b4-136"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="977b4-137">Libreria</span><span class="sxs-lookup"><span data-stu-id="977b4-137">Library</span></span><br/> | <dl> <span data-ttu-id="977b4-138"><dt>Wmdrmsdk. lib</dt></span><span class="sxs-lookup"><span data-stu-id="977b4-138"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="977b4-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="977b4-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="977b4-140">**GetLicenseProperty**</span><span class="sxs-lookup"><span data-stu-id="977b4-140">**GetLicenseProperty**</span></span>](iwmdrmlicense-getlicenseproperty.md)
</dt> <dt>

[<span data-ttu-id="977b4-141">**Interfaccia IWMDRMLicense**</span><span class="sxs-lookup"><span data-stu-id="977b4-141">**IWMDRMLicense Interface**</span></span>](iwmdrmlicense.md)
</dt> </dl>

 

 






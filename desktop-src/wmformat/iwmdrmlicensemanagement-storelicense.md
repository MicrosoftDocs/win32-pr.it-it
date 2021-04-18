---
title: Metodo IWMDRMLicenseManagement StoreLicense (wmdrmsdk. h)
description: Il metodo StoreLicense include una licenza che è stata generata all'esterno del sottosistema DRM locale nell'archivio licenze locale.
ms.assetid: 2190ff8c-8969-4f03-9f90-331bff8f4da2
keywords:
- Metodo StoreLicense Windows Media Format
- Metodo StoreLicense Windows Media Format, interfaccia IWMDRMLicenseManagement
- Interfaccia IWMDRMLicenseManagement-formato Windows Media, metodo StoreLicense
topic_type:
- apiref
api_name:
- IWMDRMLicenseManagement.StoreLicense
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fcfde6347e099ceb9fc168e1183cbd62c90f9b9c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325560"
---
# <a name="iwmdrmlicensemanagementstorelicense-method"></a><span data-ttu-id="76749-106">Metodo IWMDRMLicenseManagement:: StoreLicense</span><span class="sxs-lookup"><span data-stu-id="76749-106">IWMDRMLicenseManagement::StoreLicense method</span></span>

<span data-ttu-id="76749-107">Il metodo **StoreLicense** include una licenza che è stata generata all'esterno del sottosistema DRM locale nell'archivio licenze locale.</span><span class="sxs-lookup"><span data-stu-id="76749-107">The **StoreLicense** method includes a license that was generated outside of the local DRM subsystem in the local license store.</span></span>

## <a name="syntax"></a><span data-ttu-id="76749-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="76749-108">Syntax</span></span>


```C++
HRESULT StoreLicense(
  [in] BSTR bstrLicenseResponse
);
```



## <a name="parameters"></a><span data-ttu-id="76749-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="76749-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="76749-110">*bstrLicenseResponse* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="76749-110">*bstrLicenseResponse* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="76749-111">Stringa di risposta della licenza da decodificare e aggiungere all'archivio licenze locale.</span><span class="sxs-lookup"><span data-stu-id="76749-111">License response string to be decoded and added to the local license store.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="76749-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="76749-112">Return value</span></span>

<span data-ttu-id="76749-113">Il metodo restituisce un valore **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="76749-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="76749-114">I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="76749-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="76749-115">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="76749-115">Return code</span></span>                                                                          | <span data-ttu-id="76749-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="76749-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="76749-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="76749-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="76749-118">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="76749-118">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="76749-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="76749-119">Remarks</span></span>

<span data-ttu-id="76749-120">È possibile utilizzare questo metodo per aggiungere licenze XMR create all'archivio licenze locale.</span><span class="sxs-lookup"><span data-stu-id="76749-120">You can use this method to add XMR licenses that you have created to the local license store.</span></span>

## <a name="requirements"></a><span data-ttu-id="76749-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="76749-121">Requirements</span></span>



| <span data-ttu-id="76749-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="76749-122">Requirement</span></span> | <span data-ttu-id="76749-123">Valore</span><span class="sxs-lookup"><span data-stu-id="76749-123">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="76749-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="76749-124">Header</span></span><br/>  | <dl> <span data-ttu-id="76749-125"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="76749-125"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="76749-126">Libreria</span><span class="sxs-lookup"><span data-stu-id="76749-126">Library</span></span><br/> | <dl> <span data-ttu-id="76749-127"><dt>Wmdrmsdk. lib</dt></span><span class="sxs-lookup"><span data-stu-id="76749-127"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="76749-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="76749-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="76749-129">**Interfaccia IWMDRMLicenseManagement**</span><span class="sxs-lookup"><span data-stu-id="76749-129">**IWMDRMLicenseManagement Interface**</span></span>](iwmdrmlicensemanagement.md)
</dt> </dl>

 

 






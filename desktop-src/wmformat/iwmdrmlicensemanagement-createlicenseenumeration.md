---
title: Metodo IWMDRMLicenseManagement CreateLicenseEnumeration (wmdrmsdk. h)
description: Il metodo CreateLicenseEnumeration crea un oggetto enumeratore di licenze con il quale è possibile ottenere informazioni sulle licenze nell'archivio licenze locale.
ms.assetid: 48da1ef4-89bc-4cba-b5c9-0e202eb2986f
keywords:
- Metodo CreateLicenseEnumeration Windows Media Format
- Metodo CreateLicenseEnumeration Windows Media Format, interfaccia IWMDRMLicenseManagement
- Interfaccia IWMDRMLicenseManagement-formato Windows Media, metodo CreateLicenseEnumeration
topic_type:
- apiref
api_name:
- IWMDRMLicenseManagement.CreateLicenseEnumeration
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6bb75d21cc640da39c3679ac118ead629b24f719
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325107"
---
# <a name="iwmdrmlicensemanagementcreatelicenseenumeration-method"></a><span data-ttu-id="bd363-106">Metodo IWMDRMLicenseManagement:: CreateLicenseEnumeration</span><span class="sxs-lookup"><span data-stu-id="bd363-106">IWMDRMLicenseManagement::CreateLicenseEnumeration method</span></span>

<span data-ttu-id="bd363-107">Il metodo **CreateLicenseEnumeration** crea un oggetto enumeratore di licenze con il quale è possibile ottenere informazioni sulle licenze nell'archivio licenze locale.</span><span class="sxs-lookup"><span data-stu-id="bd363-107">The **CreateLicenseEnumeration** method creates a license enumerator object with which you can get information about licenses in the local license store.</span></span>

## <a name="syntax"></a><span data-ttu-id="bd363-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="bd363-108">Syntax</span></span>


```C++
HRESULT CreateLicenseEnumeration(
  [in]  WMDRM_LICENSE_FILTER *pLicenseFilter,
  [out] IWMDRMLicense        **pEnumerator
);
```



## <a name="parameters"></a><span data-ttu-id="bd363-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="bd363-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bd363-110">*pLicenseFilter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bd363-110">*pLicenseFilter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bd363-111">Puntatore a una struttura di [**\_ \_ filtro delle licenze WMDRM**](wmdrm-license-filter.md) contenente i parametri di filtro per l'elenco di licenze nell'enumeratore.</span><span class="sxs-lookup"><span data-stu-id="bd363-111">Pointer to a [**WMDRM\_LICENSE\_FILTER**](wmdrm-license-filter.md) structure containing the filtering parameters for the list of licenses in the enumerator.</span></span>

</dd> <dt>

<span data-ttu-id="bd363-112">*pEnumerator* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="bd363-112">*pEnumerator* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bd363-113">Puntatore che riceve l'indirizzo dell'interfaccia [**IWMDRMLicense**](iwmdrmlicense.md) dell'oggetto enumeratore licenze appena creato.</span><span class="sxs-lookup"><span data-stu-id="bd363-113">Pointer that receives the address of the [**IWMDRMLicense**](iwmdrmlicense.md) interface of the newly created license enumerator object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bd363-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="bd363-114">Return value</span></span>

<span data-ttu-id="bd363-115">Il metodo restituisce un valore **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="bd363-115">The method returns an **HRESULT**.</span></span> <span data-ttu-id="bd363-116">I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="bd363-116">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="bd363-117">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="bd363-117">Return code</span></span>                                                                                                | <span data-ttu-id="bd363-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bd363-118">Description</span></span>                                              |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <span data-ttu-id="bd363-119"><dt>**NS \_ E \_ DRM di DRM \_ \_ troppo \_ piccoli**</dt></span><span class="sxs-lookup"><span data-stu-id="bd363-119"><dt>**NS\_E\_DRM\_RIV\_TOO\_SMALL**</dt></span></span> </dl> | <span data-ttu-id="bd363-120">È necessario un elenco di revoche di contenuti aggiornato.</span><span class="sxs-lookup"><span data-stu-id="bd363-120">An updated content revocation list is needed.</span></span><br/> |
| <dl> <span data-ttu-id="bd363-121"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="bd363-121"><dt>**S\_OK**</dt></span></span> </dl>                       | <span data-ttu-id="bd363-122">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="bd363-122">The method succeeded.</span></span><br/>                         |



 

## <a name="remarks"></a><span data-ttu-id="bd363-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="bd363-123">Remarks</span></span>

<span data-ttu-id="bd363-124">Nessuna.</span><span class="sxs-lookup"><span data-stu-id="bd363-124">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="bd363-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bd363-125">Requirements</span></span>



| <span data-ttu-id="bd363-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="bd363-126">Requirement</span></span> | <span data-ttu-id="bd363-127">Valore</span><span class="sxs-lookup"><span data-stu-id="bd363-127">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bd363-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="bd363-128">Header</span></span><br/>  | <dl> <span data-ttu-id="bd363-129"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="bd363-129"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="bd363-130">Libreria</span><span class="sxs-lookup"><span data-stu-id="bd363-130">Library</span></span><br/> | <dl> <span data-ttu-id="bd363-131"><dt>Wmdrmsdk. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bd363-131"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bd363-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bd363-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bd363-133">**Enumerazione delle licenze nell'archivio licenze locale**</span><span class="sxs-lookup"><span data-stu-id="bd363-133">**Enumerating Licenses in the Local License Store**</span></span>](enumerating-licenses-in-the-local-license-store.md)
</dt> <dt>

[<span data-ttu-id="bd363-134">**Interfaccia IWMDRMLicenseManagement**</span><span class="sxs-lookup"><span data-stu-id="bd363-134">**IWMDRMLicenseManagement Interface**</span></span>](iwmdrmlicensemanagement.md)
</dt> </dl>

 

 






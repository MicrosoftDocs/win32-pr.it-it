---
title: Metodo IWMDRMLicenseManagement DeleteLicense (wmdrmsdk. h)
description: Il metodo DeleteLicense rimuove una licenza dall'archivio licenze locale temporaneo.
ms.assetid: 0aa7143a-845a-41a4-8b3c-a04c68ee280a
keywords:
- Metodo DeleteLicense Windows Media Format
- Metodo DeleteLicense Windows Media Format, interfaccia IWMDRMLicenseManagement
- Interfaccia IWMDRMLicenseManagement-formato Windows Media, metodo DeleteLicense
topic_type:
- apiref
api_name:
- IWMDRMLicenseManagement.DeleteLicense
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5d5b52f6277459f147285f46fc791669e56061a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329280"
---
# <a name="iwmdrmlicensemanagementdeletelicense-method"></a><span data-ttu-id="f12e4-106">IWMDRMLicenseManagement::D Metodo eleteLicense</span><span class="sxs-lookup"><span data-stu-id="f12e4-106">IWMDRMLicenseManagement::DeleteLicense method</span></span>

<span data-ttu-id="f12e4-107">Il metodo **DeleteLicense** rimuove una licenza dall'archivio licenze locale temporaneo.</span><span class="sxs-lookup"><span data-stu-id="f12e4-107">The **DeleteLicense** method removes a license from the temporary local license store.</span></span>

## <a name="syntax"></a><span data-ttu-id="f12e4-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f12e4-108">Syntax</span></span>


```C++
HRESULT DeleteLicense(
  [in] BSTR  bstrKID,
  [in] DWORD dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="f12e4-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="f12e4-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f12e4-110">*bstrKID* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f12e4-110">*bstrKID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f12e4-111">ID chiave (KID) della licenza da eliminare.</span><span class="sxs-lookup"><span data-stu-id="f12e4-111">Key ID (KID) of the license to be deleted.</span></span>

</dd> <dt>

<span data-ttu-id="f12e4-112">*dwFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f12e4-112">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f12e4-113">Flag dell'opzione di eliminazione delle licenze.</span><span class="sxs-lookup"><span data-stu-id="f12e4-113">License deletion option flags.</span></span> <span data-ttu-id="f12e4-114">Impostare su uno dei valori riportati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="f12e4-114">Set to one of the values in the following table.</span></span>



| <span data-ttu-id="f12e4-115">Valore</span><span class="sxs-lookup"><span data-stu-id="f12e4-115">Value</span></span>                                    | <span data-ttu-id="f12e4-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f12e4-116">Description</span></span>                                                                                                                                                                                           |
|------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f12e4-117">WMDRM \_ eliminare \_ immediatamente la licenza \_</span><span class="sxs-lookup"><span data-stu-id="f12e4-117">WMDRM\_DELETE\_LICENSE\_IMMEDIATELY</span></span>      | <span data-ttu-id="f12e4-118">Specifica che la licenza deve essere rimossa immediatamente dall'archivio.</span><span class="sxs-lookup"><span data-stu-id="f12e4-118">Specifies that the license should be removed from the store immediately.</span></span>                                                                                                                              |
| <span data-ttu-id="f12e4-119">WMDRM \_ eliminare \_ il \_ contrassegno \_ di licenza per l' \_ eliminazione</span><span class="sxs-lookup"><span data-stu-id="f12e4-119">WMDRM\_DELETE\_LICENSE\_MARK\_FOR\_PURGE</span></span> | <span data-ttu-id="f12e4-120">Specifica che la licenza deve essere contrassegnata per l'eliminazione, ma non deve essere rimossa dall'archivio fino a quando non viene chiamato il metodo [**CleanLicenseStore**](iwmdrmlicensemanagement-cleanlicensestore.md) .</span><span class="sxs-lookup"><span data-stu-id="f12e4-120">Specifies that the license should be marked for deletion, but should not be removed from the store until the [**CleanLicenseStore**](iwmdrmlicensemanagement-cleanlicensestore.md) method is called.</span></span> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f12e4-121">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f12e4-121">Return value</span></span>

<span data-ttu-id="f12e4-122">Il metodo restituisce un valore **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="f12e4-122">The method returns an **HRESULT**.</span></span> <span data-ttu-id="f12e4-123">I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="f12e4-123">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="f12e4-124">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="f12e4-124">Return code</span></span>                                                                                            | <span data-ttu-id="f12e4-125">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f12e4-125">Description</span></span>                                                                                                         |
|--------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="f12e4-126"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="f12e4-126"><dt>**S\_OK**</dt></span></span> </dl>                   | <span data-ttu-id="f12e4-127">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="f12e4-127">The method succeeded.</span></span><br/>                                                                                    |
| <dl> <span data-ttu-id="f12e4-128"><dt>**DRM \_ E \_ LICENSENOTFOUND**</dt></span><span class="sxs-lookup"><span data-stu-id="f12e4-128"><dt>**DRM\_E\_LICENSENOTFOUND**</dt></span></span> </dl> | <span data-ttu-id="f12e4-129">La licenza specificata non esiste nell'archivio.</span><span class="sxs-lookup"><span data-stu-id="f12e4-129">The specified license does not exist in the store.</span></span><br/> <span data-ttu-id="f12e4-130">oppure</span><span class="sxs-lookup"><span data-stu-id="f12e4-130">- OR -</span></span><br/> <span data-ttu-id="f12e4-131">L'archivio non è stato trovato.</span><span class="sxs-lookup"><span data-stu-id="f12e4-131">The store was not found.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="f12e4-132">Commenti</span><span class="sxs-lookup"><span data-stu-id="f12e4-132">Remarks</span></span>

<span data-ttu-id="f12e4-133">Per eliminare le licenze dall'archivio licenze locale permanente, è necessario utilizzare la revoca delle licenze.</span><span class="sxs-lookup"><span data-stu-id="f12e4-133">To delete licenses from the permanent local license store, you must use license revocation.</span></span>

## <a name="requirements"></a><span data-ttu-id="f12e4-134">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f12e4-134">Requirements</span></span>



| <span data-ttu-id="f12e4-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="f12e4-135">Requirement</span></span> | <span data-ttu-id="f12e4-136">Valore</span><span class="sxs-lookup"><span data-stu-id="f12e4-136">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f12e4-137">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f12e4-137">Header</span></span><br/>  | <dl> <span data-ttu-id="f12e4-138"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="f12e4-138"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="f12e4-139">Libreria</span><span class="sxs-lookup"><span data-stu-id="f12e4-139">Library</span></span><br/> | <dl> <span data-ttu-id="f12e4-140"><dt>Wmdrmsdk. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f12e4-140"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f12e4-141">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f12e4-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f12e4-142">**Interfaccia IWMDRMLicenseManagement**</span><span class="sxs-lookup"><span data-stu-id="f12e4-142">**IWMDRMLicenseManagement Interface**</span></span>](iwmdrmlicensemanagement.md)
</dt> </dl>

 

 






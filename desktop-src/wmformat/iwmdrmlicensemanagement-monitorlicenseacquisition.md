---
title: Metodo IWMDRMLicenseManagement MonitorLicenseAcquisition (wmdrmsdk. h)
description: Il metodo MonitorLicenseAcquisition avvia il monitoraggio per un processo di acquisizione delle licenze.
ms.assetid: 725cd51a-a50b-4ff5-a880-7f551f6dba8f
keywords:
- Metodo MonitorLicenseAcquisition Windows Media Format
- Metodo MonitorLicenseAcquisition Windows Media Format, interfaccia IWMDRMLicenseManagement
- Interfaccia IWMDRMLicenseManagement-formato Windows Media, metodo MonitorLicenseAcquisition
topic_type:
- apiref
api_name:
- IWMDRMLicenseManagement.MonitorLicenseAcquisition
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 25171d36a9d360f7c8eb77211c580c4f7676618f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324046"
---
# <a name="iwmdrmlicensemanagementmonitorlicenseacquisition-method"></a><span data-ttu-id="b2ec1-106">Metodo IWMDRMLicenseManagement:: MonitorLicenseAcquisition</span><span class="sxs-lookup"><span data-stu-id="b2ec1-106">IWMDRMLicenseManagement::MonitorLicenseAcquisition method</span></span>

<span data-ttu-id="b2ec1-107">Il metodo **MonitorLicenseAcquisition** avvia il monitoraggio per un processo di acquisizione delle licenze.</span><span class="sxs-lookup"><span data-stu-id="b2ec1-107">The **MonitorLicenseAcquisition** method initiates monitoring for a license acquisition process.</span></span>

## <a name="syntax"></a><span data-ttu-id="b2ec1-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b2ec1-108">Syntax</span></span>


```C++
HRESULT MonitorLicenseAcquisition(
  [in]  BSTR     bstrKID,
  [in]  BSTR     bstrHeader,
  [in]  BSTR     bstrActions,
  [out] IUnknown **ppunkCancelationCookie
);
```



## <a name="parameters"></a><span data-ttu-id="b2ec1-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="b2ec1-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b2ec1-110">*bstrKID* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b2ec1-110">*bstrKID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b2ec1-111">ID chiave (KID) della licenza che si sta acquisendo.</span><span class="sxs-lookup"><span data-stu-id="b2ec1-111">Key ID (KID) of the license being acquired.</span></span>

</dd> <dt>

<span data-ttu-id="b2ec1-112">*bstrHeader* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b2ec1-112">*bstrHeader* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b2ec1-113">Intestazione del contenuto utilizzata nella chiamata al metodo [**AcquireLicense**](iwmdrmlicensemanagement-acquirelicense.md) .</span><span class="sxs-lookup"><span data-stu-id="b2ec1-113">Content header that was used in the call to the [**AcquireLicense**](iwmdrmlicensemanagement-acquirelicense.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="b2ec1-114">*bstrActions* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b2ec1-114">*bstrActions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b2ec1-115">Stringa contenente le azioni richieste nella chiamata al metodo **AcquireLicense** .</span><span class="sxs-lookup"><span data-stu-id="b2ec1-115">String containing the actions requested in the call to the **AcquireLicense** method.</span></span>

</dd> <dt>

<span data-ttu-id="b2ec1-116">*ppunkCancelationCookie* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="b2ec1-116">*ppunkCancelationCookie* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b2ec1-117">Puntatore che riceve un puntatore all'interfaccia **IUnknown** di un oggetto che identifica la chiamata asincrona.</span><span class="sxs-lookup"><span data-stu-id="b2ec1-117">Pointer that receives a pointer to the **IUnknown** interface of an object that identifies this asynchronous call.</span></span> <span data-ttu-id="b2ec1-118">Questo puntatore di interfaccia può essere utilizzato per annullare la chiamata asincrona chiamando il metodo [**IWMDRMEventGenerator:: CancelAsyncOperation**](iwmdrmeventgenerator-cancelasyncoperation.md) .</span><span class="sxs-lookup"><span data-stu-id="b2ec1-118">This interface pointer can be used to cancel the asynchronous call by calling the [**IWMDRMEventGenerator::CancelAsyncOperation**](iwmdrmeventgenerator-cancelasyncoperation.md) method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b2ec1-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b2ec1-119">Return value</span></span>

<span data-ttu-id="b2ec1-120">Il metodo restituisce un valore **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="b2ec1-120">The method returns an **HRESULT**.</span></span> <span data-ttu-id="b2ec1-121">I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="b2ec1-121">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="b2ec1-122">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="b2ec1-122">Return code</span></span>                                                                          | <span data-ttu-id="b2ec1-123">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b2ec1-123">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="b2ec1-124"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="b2ec1-124"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="b2ec1-125">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="b2ec1-125">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="b2ec1-126">Commenti</span><span class="sxs-lookup"><span data-stu-id="b2ec1-126">Remarks</span></span>

<span data-ttu-id="b2ec1-127">Nessuna.</span><span class="sxs-lookup"><span data-stu-id="b2ec1-127">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="b2ec1-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b2ec1-128">Requirements</span></span>



| <span data-ttu-id="b2ec1-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="b2ec1-129">Requirement</span></span> | <span data-ttu-id="b2ec1-130">Valore</span><span class="sxs-lookup"><span data-stu-id="b2ec1-130">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b2ec1-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b2ec1-131">Header</span></span><br/>  | <dl> <span data-ttu-id="b2ec1-132"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="b2ec1-132"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="b2ec1-133">Libreria</span><span class="sxs-lookup"><span data-stu-id="b2ec1-133">Library</span></span><br/> | <dl> <span data-ttu-id="b2ec1-134"><dt>Wmdrmsdk. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b2ec1-134"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b2ec1-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b2ec1-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b2ec1-136">**Interfaccia IWMDRMLicenseManagement**</span><span class="sxs-lookup"><span data-stu-id="b2ec1-136">**IWMDRMLicenseManagement Interface**</span></span>](iwmdrmlicensemanagement.md)
</dt> </dl>

 

 






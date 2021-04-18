---
title: Metodo IWMDRMLicenseManagement RestoreLicenses (wmdrmsdk. h)
description: Il metodo RestoreLicenses Ripristina le licenze da un backup delle licenze creato chiamando il metodo BackupLicenses.
ms.assetid: 83e4b748-0f69-4a9e-b531-047c9a2be1fe
keywords:
- Metodo RestoreLicenses Windows Media Format
- Metodo RestoreLicenses Windows Media Format, interfaccia IWMDRMLicenseManagement
- Interfaccia IWMDRMLicenseManagement-formato Windows Media, metodo RestoreLicenses
topic_type:
- apiref
api_name:
- IWMDRMLicenseManagement.RestoreLicenses
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb07f3989ff19faa723e4b1d1cd50dc4e269f219
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327464"
---
# <a name="iwmdrmlicensemanagementrestorelicenses-method"></a><span data-ttu-id="6096f-106">Metodo IWMDRMLicenseManagement:: RestoreLicenses</span><span class="sxs-lookup"><span data-stu-id="6096f-106">IWMDRMLicenseManagement::RestoreLicenses method</span></span>

<span data-ttu-id="6096f-107">Il metodo **RestoreLicenses** Ripristina le licenze da un backup delle licenze creato chiamando il metodo [**BackupLicenses**](iwmdrmlicensemanagement-backuplicenses.md) .</span><span class="sxs-lookup"><span data-stu-id="6096f-107">The **RestoreLicenses** method restores licenses from a license backup that was created by calling the [**BackupLicenses**](iwmdrmlicensemanagement-backuplicenses.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="6096f-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6096f-108">Syntax</span></span>


```C++
HRESULT RestoreLicenses(
  [in]  BSTR     bstrBackupDirectory,
  [in]  DWORD    dwFlags,
  [out] IUnknown **ppunkCancelationCookie
);
```



## <a name="parameters"></a><span data-ttu-id="6096f-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="6096f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6096f-110">*bstrBackupDirectory* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6096f-110">*bstrBackupDirectory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6096f-111">Percorso UNC della posizione da cui verranno ripristinate le licenze.</span><span class="sxs-lookup"><span data-stu-id="6096f-111">UNC path of the location from which the licenses will be restored.</span></span>

</dd> <dt>

<span data-ttu-id="6096f-112">*dwFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6096f-112">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6096f-113">Flag che specificano le opzioni di ripristino da utilizzare.</span><span class="sxs-lookup"><span data-stu-id="6096f-113">Flags specifying the restore options to use.</span></span> <span data-ttu-id="6096f-114">L'unico flag attualmente supportato è WMDRM \_ Restore \_ individualizzato, che configura il metodo per eseguire l'individualizzazione come parte del ripristino, se necessario.</span><span class="sxs-lookup"><span data-stu-id="6096f-114">The only flag currently supported is WMDRM\_RESTORE\_INDIVIDUALIZE, which configures the method to perform individualization as part of the restoration, if required.</span></span>

</dd> <dt>

<span data-ttu-id="6096f-115">*ppunkCancelationCookie* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="6096f-115">*ppunkCancelationCookie* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6096f-116">Puntatore che riceve un puntatore all'interfaccia **IUnknown** di un oggetto che identifica la chiamata asincrona.</span><span class="sxs-lookup"><span data-stu-id="6096f-116">Pointer that receives a pointer to the **IUnknown** interface of an object that identifies this asynchronous call.</span></span> <span data-ttu-id="6096f-117">Questo puntatore di interfaccia può essere utilizzato per annullare la chiamata asincrona chiamando il metodo [**IWMDRMEventGenerator:: CancelAsyncOperation**](iwmdrmeventgenerator-cancelasyncoperation.md) .</span><span class="sxs-lookup"><span data-stu-id="6096f-117">This interface pointer can be used to cancel the asynchronous call by calling the [**IWMDRMEventGenerator::CancelAsyncOperation**](iwmdrmeventgenerator-cancelasyncoperation.md) method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6096f-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6096f-118">Return value</span></span>

<span data-ttu-id="6096f-119">Il metodo restituisce un valore **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="6096f-119">The method returns an **HRESULT**.</span></span> <span data-ttu-id="6096f-120">I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="6096f-120">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="6096f-121">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="6096f-121">Return code</span></span>                                                                          | <span data-ttu-id="6096f-122">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6096f-122">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="6096f-123"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="6096f-123"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="6096f-124">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="6096f-124">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="6096f-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="6096f-125">Remarks</span></span>

<span data-ttu-id="6096f-126">Questo metodo viene eseguito in modo asincrono.</span><span class="sxs-lookup"><span data-stu-id="6096f-126">This method executes asynchronously.</span></span> <span data-ttu-id="6096f-127">Viene restituito immediatamente dopo la chiamata di e quindi genera una serie di eventi **MEWMDRMLicenseRestoreProgress** seguiti da un evento **MEWMDRMLicenseRestoreCompleted** al termine dell'elaborazione.</span><span class="sxs-lookup"><span data-stu-id="6096f-127">It returns immediately after being called and then generates a series of **MEWMDRMLicenseRestoreProgress** events followed by an **MEWMDRMLicenseRestoreCompleted** event when processing is complete.</span></span> <span data-ttu-id="6096f-128">Il valore di ogni evento **MEWMDRMLicenseRestoreProgress** ottenuto chiamando **IMFMediaEvent:: GetValue** è un puntatore **IUnknown** .</span><span class="sxs-lookup"><span data-stu-id="6096f-128">The value of each of the **MEWMDRMLicenseRestoreProgress** events obtained by calling **IMFMediaEvent::GetValue** is an **IUnknown** pointer.</span></span> <span data-ttu-id="6096f-129">È possibile chiamare il metodo **QueryInterface** dell'interfaccia **IUnknown** recuperata per ottenere un'istanza dell'interfaccia [**IWMDRMLicenseBackupRestoreStatus**](iwmdrmlicensebackuprestorestatus.md) .</span><span class="sxs-lookup"><span data-stu-id="6096f-129">You can call the **QueryInterface** method of the retrieved **IUnknown** interface to get an instance of the [**IWMDRMLicenseBackupRestoreStatus**](iwmdrmlicensebackuprestorestatus.md) interface.</span></span>

<span data-ttu-id="6096f-130">Per ulteriori informazioni sull'utilizzo dei metodi asincroni delle API estese del client Windows Media DRM, vedere [utilizzo del modello di eventi Media Foundation](using-the-media-foundation-model.md).</span><span class="sxs-lookup"><span data-stu-id="6096f-130">For more information about using the asynchronous methods of the Windows Media DRM Client Extended APIs, see [Using the Media Foundation Event Model](using-the-media-foundation-model.md).</span></span>

<span data-ttu-id="6096f-131">Il backup può provenire dal computer locale o da un computer diverso.</span><span class="sxs-lookup"><span data-stu-id="6096f-131">The backup can be from the local machine or from a different machine.</span></span>

## <a name="requirements"></a><span data-ttu-id="6096f-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6096f-132">Requirements</span></span>



| <span data-ttu-id="6096f-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="6096f-133">Requirement</span></span> | <span data-ttu-id="6096f-134">Valore</span><span class="sxs-lookup"><span data-stu-id="6096f-134">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6096f-135">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6096f-135">Header</span></span><br/>  | <dl> <span data-ttu-id="6096f-136"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="6096f-136"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="6096f-137">Libreria</span><span class="sxs-lookup"><span data-stu-id="6096f-137">Library</span></span><br/> | <dl> <span data-ttu-id="6096f-138"><dt>Wmdrmsdk. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6096f-138"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6096f-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6096f-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6096f-140">**Interfaccia IWMDRMLicenseManagement**</span><span class="sxs-lookup"><span data-stu-id="6096f-140">**IWMDRMLicenseManagement Interface**</span></span>](iwmdrmlicensemanagement.md)
</dt> </dl>

 

 






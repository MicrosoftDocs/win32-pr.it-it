---
title: Metodo IWMDRMLicenseManagement BackupLicenses (wmdrmsdk. h)
description: Il metodo BackupLicenses crea una copia di backup delle licenze nell'archivio licenze locale.
ms.assetid: f265254d-b240-4a9f-9c67-de9c92e8a14d
keywords:
- Metodo BackupLicenses Windows Media Format
- Metodo BackupLicenses Windows Media Format, interfaccia IWMDRMLicenseManagement
- Interfaccia IWMDRMLicenseManagement-formato Windows Media, metodo BackupLicenses
topic_type:
- apiref
api_name:
- IWMDRMLicenseManagement.BackupLicenses
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61c7f676b532353c839a428571f6d28540851bee
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327265"
---
# <a name="iwmdrmlicensemanagementbackuplicenses-method"></a><span data-ttu-id="e9e07-106">Metodo IWMDRMLicenseManagement:: BackupLicenses</span><span class="sxs-lookup"><span data-stu-id="e9e07-106">IWMDRMLicenseManagement::BackupLicenses method</span></span>

<span data-ttu-id="e9e07-107">Il metodo **BackupLicenses** crea una copia di backup delle licenze nell'archivio licenze locale.</span><span class="sxs-lookup"><span data-stu-id="e9e07-107">The **BackupLicenses** method creates a backup of the licenses in the local license store.</span></span>

## <a name="syntax"></a><span data-ttu-id="e9e07-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e9e07-108">Syntax</span></span>


```C++
HRESULT BackupLicenses(
  [in]  BSTR     bstrBackupDirectory,
  [in]  DWORD    dwFlags,
  [out] IUnknown **ppunkCancelationCookie
);
```



## <a name="parameters"></a><span data-ttu-id="e9e07-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="e9e07-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e9e07-110">*bstrBackupDirectory* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e9e07-110">*bstrBackupDirectory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e9e07-111">Percorso UNC della posizione in cui verrà eseguito il backup delle licenze.</span><span class="sxs-lookup"><span data-stu-id="e9e07-111">UNC path of the location to which the licenses will be backed up.</span></span>

</dd> <dt>

<span data-ttu-id="e9e07-112">*dwFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e9e07-112">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e9e07-113">Flag che specificano le opzioni di backup da utilizzare.</span><span class="sxs-lookup"><span data-stu-id="e9e07-113">Flags specifying the backup options to use.</span></span> <span data-ttu-id="e9e07-114">L'unico flag attualmente supportato è WMDRM \_ backup \_ overwrite, che configura il metodo per sovrascrivere eventuali file di backup esistenti nella directory.</span><span class="sxs-lookup"><span data-stu-id="e9e07-114">The only flag currently supported is WMDRM\_BACKUP\_OVERWRITE, which configures the method to overwrite any existing backup files in the directory.</span></span>

</dd> <dt>

<span data-ttu-id="e9e07-115">*ppunkCancelationCookie* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="e9e07-115">*ppunkCancelationCookie* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e9e07-116">Puntatore che riceve un puntatore all'interfaccia **IUnknown** di un oggetto che identifica la chiamata asincrona.</span><span class="sxs-lookup"><span data-stu-id="e9e07-116">Pointer that receives a pointer to the **IUnknown** interface of an object that identifies this asynchronous call.</span></span> <span data-ttu-id="e9e07-117">Questo puntatore di interfaccia può essere utilizzato per annullare la chiamata asincrona chiamando il metodo [**IWMDRMEventGenerator:: CancelAsyncOperation**](iwmdrmeventgenerator-cancelasyncoperation.md) .</span><span class="sxs-lookup"><span data-stu-id="e9e07-117">This interface pointer can be used to cancel the asynchronous call by calling the [**IWMDRMEventGenerator::CancelAsyncOperation**](iwmdrmeventgenerator-cancelasyncoperation.md) method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e9e07-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e9e07-118">Return value</span></span>

<span data-ttu-id="e9e07-119">Il metodo restituisce un valore **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="e9e07-119">The method returns an **HRESULT**.</span></span> <span data-ttu-id="e9e07-120">I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="e9e07-120">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="e9e07-121">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="e9e07-121">Return code</span></span>                                                                          | <span data-ttu-id="e9e07-122">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e9e07-122">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="e9e07-123"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="e9e07-123"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="e9e07-124">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="e9e07-124">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="e9e07-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="e9e07-125">Remarks</span></span>

<span data-ttu-id="e9e07-126">Questo metodo viene eseguito in modo asincrono.</span><span class="sxs-lookup"><span data-stu-id="e9e07-126">This method executes asynchronously.</span></span> <span data-ttu-id="e9e07-127">Viene restituito immediatamente dopo la chiamata di e quindi genera una serie di eventi **MEWMDRMLicenseBackupProgress** seguiti da un evento **MEWMDRMLicenseBackupCompleted** al termine dell'elaborazione.</span><span class="sxs-lookup"><span data-stu-id="e9e07-127">It returns immediately after being called and then generates a series of **MEWMDRMLicenseBackupProgress** events followed by an **MEWMDRMLicenseBackupCompleted** event when processing is complete.</span></span> <span data-ttu-id="e9e07-128">Il valore di ogni evento **MEWMDRMLicenseBackupProgress** ottenuto chiamando **IMFMediaEvent:: GetValue** è un puntatore **IUnknown** .</span><span class="sxs-lookup"><span data-stu-id="e9e07-128">The value of each of the **MEWMDRMLicenseBackupProgress** events obtained by calling **IMFMediaEvent::GetValue** is an **IUnknown** pointer.</span></span> <span data-ttu-id="e9e07-129">È possibile chiamare il metodo **QueryInterface** dell'interfaccia **IUnknown** recuperata per ottenere un'istanza dell'interfaccia [**IWMDRMLicenseBackupRestoreStatus**](iwmdrmlicensebackuprestorestatus.md) .</span><span class="sxs-lookup"><span data-stu-id="e9e07-129">You can call the **QueryInterface** method of the retrieved **IUnknown** interface to get an instance of the [**IWMDRMLicenseBackupRestoreStatus**](iwmdrmlicensebackuprestorestatus.md) interface.</span></span>

<span data-ttu-id="e9e07-130">Per ulteriori informazioni sull'utilizzo dei metodi asincroni delle API estese del client Windows Media DRM, vedere [utilizzo del modello di eventi Media Foundation](using-the-media-foundation-model.md).</span><span class="sxs-lookup"><span data-stu-id="e9e07-130">For more information about using the asynchronous methods of the Windows Media DRM Client Extended APIs, see [Using the Media Foundation Event Model](using-the-media-foundation-model.md).</span></span>

<span data-ttu-id="e9e07-131">Non è consentito eseguire il backup di tutte le licenze.</span><span class="sxs-lookup"><span data-stu-id="e9e07-131">Not all licenses are permitted to be backed up.</span></span> <span data-ttu-id="e9e07-132">Questo metodo esegue il backup solo delle licenze che lo consentono.</span><span class="sxs-lookup"><span data-stu-id="e9e07-132">This method only backs up licenses that allow it.</span></span>

## <a name="requirements"></a><span data-ttu-id="e9e07-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e9e07-133">Requirements</span></span>



| <span data-ttu-id="e9e07-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="e9e07-134">Requirement</span></span> | <span data-ttu-id="e9e07-135">Valore</span><span class="sxs-lookup"><span data-stu-id="e9e07-135">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e9e07-136">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e9e07-136">Header</span></span><br/>  | <dl> <span data-ttu-id="e9e07-137"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="e9e07-137"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="e9e07-138">Libreria</span><span class="sxs-lookup"><span data-stu-id="e9e07-138">Library</span></span><br/> | <dl> <span data-ttu-id="e9e07-139"><dt>Wmdrmsdk. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e9e07-139"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e9e07-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e9e07-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e9e07-141">**Interfaccia IWMDRMLicenseManagement**</span><span class="sxs-lookup"><span data-stu-id="e9e07-141">**IWMDRMLicenseManagement Interface**</span></span>](iwmdrmlicensemanagement.md)
</dt> </dl>

 

 






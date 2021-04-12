---
title: Interfaccia IWMDRMLicenseManagement
description: L'interfaccia IWMDRMLicenseManagement fornisce metodi che eseguono operazioni generali correlate all'archivio licenze locale. Per ottenere un'istanza di questa interfaccia, chiamare IWMDRMProvider CreateObject. Passare IID \_ IWMDRMLicenseManagement come parametro riid.
ms.assetid: 254bf54e-8ea6-4fd1-8abd-9d32539d529b
keywords:
- Formato Windows Media Interface IWMDRMLicenseManagement
- Interfaccia IWMDRMLicenseManagement-formato Windows Media, descritto
topic_type:
- apiref
api_name:
- IWMDRMLicenseManagement
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 14a7c555200e2eac99def75a1ad8c1d5dc1223fc
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104333935"
---
# <a name="iwmdrmlicensemanagement-interface"></a><span data-ttu-id="f671e-106">Interfaccia IWMDRMLicenseManagement</span><span class="sxs-lookup"><span data-stu-id="f671e-106">IWMDRMLicenseManagement interface</span></span>

<span data-ttu-id="f671e-107">L'interfaccia **IWMDRMLicenseManagement** fornisce metodi che eseguono operazioni generali correlate all'archivio licenze locale.</span><span class="sxs-lookup"><span data-stu-id="f671e-107">The **IWMDRMLicenseManagement** interface provides methods that perform general operations related to the local license store.</span></span>

<span data-ttu-id="f671e-108">Per ottenere un'istanza di questa interfaccia, chiamare [**IWMDRMProvider:: CreateObject**](iwmdrmprovider-createobject.md).</span><span class="sxs-lookup"><span data-stu-id="f671e-108">To obtain an instance of this interface, call [**IWMDRMProvider::CreateObject**](iwmdrmprovider-createobject.md).</span></span> <span data-ttu-id="f671e-109">Passare **IID \_ IWMDRMLicenseManagement** come parametro *riid* .</span><span class="sxs-lookup"><span data-stu-id="f671e-109">Pass **IID\_IWMDRMLicenseManagement** as the *riid* parameter.</span></span>

## <a name="members"></a><span data-ttu-id="f671e-110">Membri</span><span class="sxs-lookup"><span data-stu-id="f671e-110">Members</span></span>

<span data-ttu-id="f671e-111">L'interfaccia **IWMDRMLicenseManagement** eredita da [**IWMDRMEventGenerator**](iwmdrmeventgenerator.md).</span><span class="sxs-lookup"><span data-stu-id="f671e-111">The **IWMDRMLicenseManagement** interface inherits from [**IWMDRMEventGenerator**](iwmdrmeventgenerator.md).</span></span> <span data-ttu-id="f671e-112">**IWMDRMLicenseManagement** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="f671e-112">**IWMDRMLicenseManagement** also has these types of members:</span></span>

-   [<span data-ttu-id="f671e-113">Metodi</span><span class="sxs-lookup"><span data-stu-id="f671e-113">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="f671e-114">Metodi</span><span class="sxs-lookup"><span data-stu-id="f671e-114">Methods</span></span>

<span data-ttu-id="f671e-115">L'interfaccia **IWMDRMLicenseManagement** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="f671e-115">The **IWMDRMLicenseManagement** interface has these methods.</span></span>



| <span data-ttu-id="f671e-116">Metodo</span><span class="sxs-lookup"><span data-stu-id="f671e-116">Method</span></span>                                                                                               | <span data-ttu-id="f671e-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f671e-117">Description</span></span>                                                                                                             |
|:-----------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f671e-118">**AcquireLicense**</span><span class="sxs-lookup"><span data-stu-id="f671e-118">**AcquireLicense**</span></span>](iwmdrmlicensemanagement-acquirelicense.md)                                     | <span data-ttu-id="f671e-119">Acquisisce in modo asincrono una licenza da un URL specificato.</span><span class="sxs-lookup"><span data-stu-id="f671e-119">Asynchronously acquires a license from a specified URL.</span></span><br/>                                                      |
| [<span data-ttu-id="f671e-120">**BackupLicenses**</span><span class="sxs-lookup"><span data-stu-id="f671e-120">**BackupLicenses**</span></span>](iwmdrmlicensemanagement-backuplicenses.md)                                     | <span data-ttu-id="f671e-121">Crea una copia di backup delle licenze nell'archivio licenze locale.</span><span class="sxs-lookup"><span data-stu-id="f671e-121">Creates a backup of the licenses in the local license store.</span></span><br/>                                                 |
| [<span data-ttu-id="f671e-122">**CleanLicenseStore**</span><span class="sxs-lookup"><span data-stu-id="f671e-122">**CleanLicenseStore**</span></span>](iwmdrmlicensemanagement-cleanlicensestore.md)                               | <span data-ttu-id="f671e-123">Rimuove le licenze contrassegnate dall'archivio licenze e deframmenta l'archivio per migliorare le prestazioni.</span><span class="sxs-lookup"><span data-stu-id="f671e-123">Removes marked licenses from the license store and defragments the store to improve performance.</span></span><br/>             |
| [<span data-ttu-id="f671e-124">**CreateLicenseEnumeration**</span><span class="sxs-lookup"><span data-stu-id="f671e-124">**CreateLicenseEnumeration**</span></span>](iwmdrmlicensemanagement-createlicenseenumeration.md)                 | <span data-ttu-id="f671e-125">Crea un oggetto enumeratore di licenze popolato con le informazioni sulla licenza basate sui valori dei parametri.</span><span class="sxs-lookup"><span data-stu-id="f671e-125">Creates a license enumerator object populated with license information based on parameter values.</span></span><br/>            |
| [<span data-ttu-id="f671e-126">**CreateLicenseRevocationChallenge**</span><span class="sxs-lookup"><span data-stu-id="f671e-126">**CreateLicenseRevocationChallenge**</span></span>](iwmdrmlicensemanagement-createlicenserevocationchallenge.md) | <span data-ttu-id="f671e-127">Genera una richiesta di revoca delle licenze.</span><span class="sxs-lookup"><span data-stu-id="f671e-127">Generates a license revocation challenge.</span></span><br/>                                                                    |
| [<span data-ttu-id="f671e-128">**DeleteLicense**</span><span class="sxs-lookup"><span data-stu-id="f671e-128">**DeleteLicense**</span></span>](iwmdrmlicensemanagement-deletelicense.md)                                       | <span data-ttu-id="f671e-129">Elimina una licenza dall'archivio licenze locale temporaneo.</span><span class="sxs-lookup"><span data-stu-id="f671e-129">Deletes a license from the temporary local license store.</span></span><br/>                                                    |
| [<span data-ttu-id="f671e-130">**MonitorLicenseAcquisition**</span><span class="sxs-lookup"><span data-stu-id="f671e-130">**MonitorLicenseAcquisition**</span></span>](iwmdrmlicensemanagement-monitorlicenseacquisition.md)               | <span data-ttu-id="f671e-131">Avvia il monitoraggio per un processo di acquisizione delle licenze.</span><span class="sxs-lookup"><span data-stu-id="f671e-131">Initiates monitoring for a license acquisition process.</span></span><br/>                                                      |
| [<span data-ttu-id="f671e-132">**ProcessLicenseDeletionMessage**</span><span class="sxs-lookup"><span data-stu-id="f671e-132">**ProcessLicenseDeletionMessage**</span></span>](iwmdrmlicensemanagement-processlicensedeletionmessage.md)       | <span data-ttu-id="f671e-133">Elimina una licenza importata per il contenuto originariamente protetto con un altro sistema di protezione del contenuto.</span><span class="sxs-lookup"><span data-stu-id="f671e-133">Deletes a license that was imported for content originally protected with another content protection system.</span></span><br/> |
| [<span data-ttu-id="f671e-134">**ProcessLicenseRevocationResponse**</span><span class="sxs-lookup"><span data-stu-id="f671e-134">**ProcessLicenseRevocationResponse**</span></span>](iwmdrmlicensemanagement-processlicenserevocationresponse.md) | <span data-ttu-id="f671e-135">Revoca le licenze dall'archivio licenze locale.</span><span class="sxs-lookup"><span data-stu-id="f671e-135">Revokes licenses from the local license store.</span></span><br/>                                                               |
| [<span data-ttu-id="f671e-136">**RestoreLicenses**</span><span class="sxs-lookup"><span data-stu-id="f671e-136">**RestoreLicenses**</span></span>](iwmdrmlicensemanagement-restorelicenses.md)                                   | <span data-ttu-id="f671e-137">Ripristina le licenze di cui è stato eseguito il backup in precedenza.</span><span class="sxs-lookup"><span data-stu-id="f671e-137">Restores previously backed up licenses.</span></span><br/>                                                                      |
| [<span data-ttu-id="f671e-138">**StoreLicense**</span><span class="sxs-lookup"><span data-stu-id="f671e-138">**StoreLicense**</span></span>](iwmdrmlicensemanagement-storelicense.md)                                         | <span data-ttu-id="f671e-139">Aggiunge una licenza all'archivio licenze locale.</span><span class="sxs-lookup"><span data-stu-id="f671e-139">Adds a license to the local license store.</span></span><br/>                                                                   |



 

## <a name="see-also"></a><span data-ttu-id="f671e-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f671e-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f671e-141">**Interfacce**</span><span class="sxs-lookup"><span data-stu-id="f671e-141">**Interfaces**</span></span>](drm-interfaces.md)
</dt> <dt>

[<span data-ttu-id="f671e-142">**IWMDRMEventGenerator**</span><span class="sxs-lookup"><span data-stu-id="f671e-142">**IWMDRMEventGenerator**</span></span>](iwmdrmeventgenerator.md)
</dt> </dl>

 

 






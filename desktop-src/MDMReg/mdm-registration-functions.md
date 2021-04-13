---
title: Funzioni di registrazione MDM
description: Le funzioni seguenti vengono usate dalla registrazione MDM.
ms.assetid: 1b063a56-f59f-4b02-949f-c8b6bbf45a13
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 821e08d9c6631bbb300a86ab6b9c480a3af0c25b
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/08/2020
ms.locfileid: "104339439"
---
# <a name="mdm-registration-functions"></a><span data-ttu-id="b758f-103">Funzioni di registrazione MDM</span><span class="sxs-lookup"><span data-stu-id="b758f-103">MDM Registration Functions</span></span>

<span data-ttu-id="b758f-104">Le funzioni seguenti vengono usate dalla registrazione MDM.</span><span class="sxs-lookup"><span data-stu-id="b758f-104">The following functions are used by MDM Registration.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="b758f-105">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="b758f-105">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="b758f-106">**DiscoverManagementService**</span><span class="sxs-lookup"><span data-stu-id="b758f-106">**DiscoverManagementService**</span></span>](/windows/desktop/api/MDMRegistration/nf-mdmregistration-discovermanagementservice)
</dt> <dd>

<span data-ttu-id="b758f-107">Individua il servizio MDM.</span><span class="sxs-lookup"><span data-stu-id="b758f-107">Discovers the MDM service.</span></span>

</dd> <dt>

[<span data-ttu-id="b758f-108">**DiscoverManagementServiceEx**</span><span class="sxs-lookup"><span data-stu-id="b758f-108">**DiscoverManagementServiceEx**</span></span>](/windows/desktop/api/MDMRegistration/nf-mdmregistration-discovermanagementserviceex)
</dt> <dd>

<span data-ttu-id="b758f-109">Individua il servizio MDM utilizzando un server candidato.</span><span class="sxs-lookup"><span data-stu-id="b758f-109">Discovers the MDM service using a candidate server.</span></span>

</dd> <dt>

[<span data-ttu-id="b758f-110">**GetDeviceRegistrationInfo**</span><span class="sxs-lookup"><span data-stu-id="b758f-110">**GetDeviceRegistrationInfo**</span></span>](/windows/desktop/api/MDMRegistration/nf-mdmregistration-getdeviceregistrationinfo)
</dt> <dd>

<span data-ttu-id="b758f-111">Recupera le informazioni di registrazione del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b758f-111">Retrieves the device registration information.</span></span>

</dd> <dt>

[<span data-ttu-id="b758f-112">**GetManagementAppHyperlink**</span><span class="sxs-lookup"><span data-stu-id="b758f-112">**GetManagementAppHyperlink**</span></span>](/windows/desktop/api/MDMRegistration/nf-mdmregistration-getmanagementapphyperlink)
</dt> <dd>

<span data-ttu-id="b758f-113">Recupera il collegamento ipertestuale dell'app di gestione associato al servizio MDM.</span><span class="sxs-lookup"><span data-stu-id="b758f-113">Retrieves the management app hyperlink associated with the MDM service.</span></span>

</dd> <dt>

[<span data-ttu-id="b758f-114">**IsDeviceRegisteredWithManagement**</span><span class="sxs-lookup"><span data-stu-id="b758f-114">**IsDeviceRegisteredWithManagement**</span></span>](/windows/desktop/api/MDMRegistration/nf-mdmregistration-isdeviceregisteredwithmanagement)
</dt> <dd>

<span data-ttu-id="b758f-115">Controlla se il dispositivo è registrato con un servizio MDM.</span><span class="sxs-lookup"><span data-stu-id="b758f-115">Checks whether the device is registered with an MDM service.</span></span>

</dd> <dt>

[<span data-ttu-id="b758f-116">**IsManagementRegistrationAllowed**</span><span class="sxs-lookup"><span data-stu-id="b758f-116">**IsManagementRegistrationAllowed**</span></span>](/windows/desktop/api/MDMRegistration/nf-mdmregistration-ismanagementregistrationallowed)
</dt> <dd>

<span data-ttu-id="b758f-117">Verifica se la registrazione MDM è consentita dai criteri locali.</span><span class="sxs-lookup"><span data-stu-id="b758f-117">Checks whether MDM registration is allowed by local policy.</span></span>

</dd> <dt>

[<span data-ttu-id="b758f-118">**RegisterDeviceWithManagement**</span><span class="sxs-lookup"><span data-stu-id="b758f-118">**RegisterDeviceWithManagement**</span></span>](/windows/desktop/api/MDMRegistration/nf-mdmregistration-registerdevicewithmanagement)
</dt> <dd>

<span data-ttu-id="b758f-119">Registra un dispositivo con un servizio MDM usando il [ \[ protocollo MS-MDE \] : registrazione del dispositivo mobile](/openspecs/windows_protocols/ms-mde/5c841535-042e-489e-913c-9d783d741267).</span><span class="sxs-lookup"><span data-stu-id="b758f-119">Registers a device with a MDM service, using the [\[MS-MDE\]: Mobile Device Enrollment Protocol](/openspecs/windows_protocols/ms-mde/5c841535-042e-489e-913c-9d783d741267).</span></span>

</dd> <dt>

[<span data-ttu-id="b758f-120">**RegisterDeviceWithManagementUsingAADCredentials**</span><span class="sxs-lookup"><span data-stu-id="b758f-120">**RegisterDeviceWithManagementUsingAADCredentials**</span></span>](/windows/desktop/api/MDMRegistration/nf-mdmregistration-registerdevicewithmanagementusingaadcredentials)
</dt> <dd>

<span data-ttu-id="b758f-121">Registra un dispositivo con un servizio MDM, usando le credenziali Azure Active Directory (AAD).</span><span class="sxs-lookup"><span data-stu-id="b758f-121">Registers a device with a MDM service, using Azure Active Directory (AAD) credentials.</span></span>

</dd> <dt>

[<span data-ttu-id="b758f-122">**SetManagedExternally**</span><span class="sxs-lookup"><span data-stu-id="b758f-122">**SetManagedExternally**</span></span>](/windows/desktop/api/MDMRegistration/nf-mdmregistration-setmanagedexternally)
</dt> <dd>

<span data-ttu-id="b758f-123">Indica all'agente MDM che il dispositivo è gestito esternamente e non deve essere registrato con un servizio MDM.</span><span class="sxs-lookup"><span data-stu-id="b758f-123">Indicates to the MDM agent that the device is managed externally and is not to be registered with an MDM service.</span></span>

</dd> <dt>

[<span data-ttu-id="b758f-124">**UnregisterDeviceWithManagement**</span><span class="sxs-lookup"><span data-stu-id="b758f-124">**UnregisterDeviceWithManagement**</span></span>](/windows/desktop/api/MDMRegistration/nf-mdmregistration-unregisterdevicewithmanagement)
</dt> <dd>

<span data-ttu-id="b758f-125">Annulla la registrazione di un dispositivo con il servizio MDM</span><span class="sxs-lookup"><span data-stu-id="b758f-125">Unregisters a device with the MDM service</span></span>

</dd> </dl>

 

 
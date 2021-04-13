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
# <a name="mdm-registration-functions"></a>Funzioni di registrazione MDM

Le funzioni seguenti vengono usate dalla registrazione MDM.

## <a name="in-this-section"></a>Contenuto della sezione

<dl> <dt>

[**DiscoverManagementService**](/windows/desktop/api/MDMRegistration/nf-mdmregistration-discovermanagementservice)
</dt> <dd>

Individua il servizio MDM.

</dd> <dt>

[**DiscoverManagementServiceEx**](/windows/desktop/api/MDMRegistration/nf-mdmregistration-discovermanagementserviceex)
</dt> <dd>

Individua il servizio MDM utilizzando un server candidato.

</dd> <dt>

[**GetDeviceRegistrationInfo**](/windows/desktop/api/MDMRegistration/nf-mdmregistration-getdeviceregistrationinfo)
</dt> <dd>

Recupera le informazioni di registrazione del dispositivo.

</dd> <dt>

[**GetManagementAppHyperlink**](/windows/desktop/api/MDMRegistration/nf-mdmregistration-getmanagementapphyperlink)
</dt> <dd>

Recupera il collegamento ipertestuale dell'app di gestione associato al servizio MDM.

</dd> <dt>

[**IsDeviceRegisteredWithManagement**](/windows/desktop/api/MDMRegistration/nf-mdmregistration-isdeviceregisteredwithmanagement)
</dt> <dd>

Controlla se il dispositivo è registrato con un servizio MDM.

</dd> <dt>

[**IsManagementRegistrationAllowed**](/windows/desktop/api/MDMRegistration/nf-mdmregistration-ismanagementregistrationallowed)
</dt> <dd>

Verifica se la registrazione MDM è consentita dai criteri locali.

</dd> <dt>

[**RegisterDeviceWithManagement**](/windows/desktop/api/MDMRegistration/nf-mdmregistration-registerdevicewithmanagement)
</dt> <dd>

Registra un dispositivo con un servizio MDM usando il [ \[ protocollo MS-MDE \] : registrazione del dispositivo mobile](/openspecs/windows_protocols/ms-mde/5c841535-042e-489e-913c-9d783d741267).

</dd> <dt>

[**RegisterDeviceWithManagementUsingAADCredentials**](/windows/desktop/api/MDMRegistration/nf-mdmregistration-registerdevicewithmanagementusingaadcredentials)
</dt> <dd>

Registra un dispositivo con un servizio MDM, usando le credenziali Azure Active Directory (AAD).

</dd> <dt>

[**SetManagedExternally**](/windows/desktop/api/MDMRegistration/nf-mdmregistration-setmanagedexternally)
</dt> <dd>

Indica all'agente MDM che il dispositivo è gestito esternamente e non deve essere registrato con un servizio MDM.

</dd> <dt>

[**UnregisterDeviceWithManagement**](/windows/desktop/api/MDMRegistration/nf-mdmregistration-unregisterdevicewithmanagement)
</dt> <dd>

Annulla la registrazione di un dispositivo con il servizio MDM

</dd> </dl>

 

 
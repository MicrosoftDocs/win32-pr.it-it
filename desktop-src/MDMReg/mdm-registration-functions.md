---
title: Funzioni di registrazione MDM
description: Le funzioni seguenti vengono dichiarate in `mdmregistration.h` e vengono usate dalla registrazione MDM.
ms.assetid: 1b063a56-f59f-4b02-949f-c8b6bbf45a13
ms.localizationpriority: low
ms.topic: reference
ms.date: 11/19/2020
ms.openlocfilehash: 2ca04c3c28f3de289bad6f06feaab0aff9ef2909
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/27/2021
ms.locfileid: "110550556"
---
# <a name="mdm-registration-functions"></a>Funzioni di registrazione MDM

Le funzioni seguenti vengono dichiarate in `mdmregistration.h` e vengono usate dalla registrazione MDM.

## <a name="in-this-section"></a>Contenuto della sezione

| Argomento | Descrizione |
|-|-|
| [**DiscoverManagementService**](/windows/win32/api/MDMRegistration/nf-mdmregistration-discovermanagementservice) | Individua il servizio MDM. |
| [**DiscoverManagementServiceEx**](/windows/win32/api/MDMRegistration/nf-mdmregistration-discovermanagementserviceex) | Individua il servizio MDM usando un server candidato. |
| [**GetDeviceManagementConfigInfo**](/windows/win32/api/mdmregistration/nf-mdmregistration-getdevicemanagementconfiginfo) | Ottiene le informazioni di configurazione associate all'ID provider. |
| [**GetDeviceRegistrationInfo**](/windows/win32/api/MDMRegistration/nf-mdmregistration-getdeviceregistrationinfo) | Recupera le informazioni di registrazione del dispositivo. |
| [**GetManagementAppHyperlink**](/windows/win32/api/MDMRegistration/nf-mdmregistration-getmanagementapphyperlink) | Recupera il collegamento ipertestuale dell'app di gestione associato al servizio MDM. |
| [**IsDeviceRegisteredWithManagement**](/windows/win32/api/MDMRegistration/nf-mdmregistration-isdeviceregisteredwithmanagement) | Controlla se il dispositivo è registrato con un servizio MDM. |
| [**IsManagementRegistrationAllowed**](/windows/win32/api/MDMRegistration/nf-mdmregistration-ismanagementregistrationallowed) | Controlla se la registrazione MDM è consentita dai criteri locali. |
| [**RegisterDeviceWithManagement**](/windows/win32/api/MDMRegistration/nf-mdmregistration-registerdevicewithmanagement) | Registra un dispositivo con un servizio MDM usando [ \[ MS-MDE: \] Mobile Device Enrollment Protocol.](/openspecs/windows_protocols/ms-mde/5c841535-042e-489e-913c-9d783d741267) |
| [**RegisterDeviceWithManagementUsingAADCredentials**](/windows/win32/api/MDMRegistration/nf-mdmregistration-registerdevicewithmanagementusingaadcredentials) | Registra un dispositivo con un servizio MDM usando Azure Active Directory (AAD). |
| [**SetDeviceManagementConfigInfo**](/windows/win32/api/mdmregistration/nf-mdmregistration-setdevicemanagementconfiginfo) | Imposta le informazioni di configurazione associate all'ID provider. |
| [**SetManagedExternally**](/windows/win32/api/MDMRegistration/nf-mdmregistration-setmanagedexternally) | Indica all'agente MDM che il dispositivo è gestito esternamente e non deve essere registrato con un servizio MDM. |
| [**UnregisterDeviceWithManagement**](/windows/win32/api/MDMRegistration/nf-mdmregistration-unregisterdevicewithmanagement) | Annulla la registrazione di un dispositivo con il servizio MDM. |

## <a name="related-topics"></a>Argomenti correlati

* [Informazioni di riferimento sulla registrazione MDM](./mdm-registration-reference.md)

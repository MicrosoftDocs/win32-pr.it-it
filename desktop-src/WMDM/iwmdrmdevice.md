---
title: Interfaccia IWMDRMDevice
description: Questa interfaccia non è progettata per essere implementata da un provider di servizi, ma viene fornita ai fini della documentazione completa. L'interfaccia IWMDRMDevice consente a un provider di contenuti protetto di comunicare con i dispositivi che usano Windows Media DRM 10 per i dispositivi portatili.
ms.assetid: ebad4acd-16cc-433f-a5e0-fcae59030f55
keywords:
- Interfaccia IWMDRMDevice Windows Media Gestione dispositivi
- Interfaccia IWMDRMDevice Windows Media Gestione dispositivi, descritta
topic_type:
- apiref
api_name:
- IWMDRMDevice
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ca240f01f552dfdedb0145e49f61f2ead1f18832
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104337927"
---
# <a name="iwmdrmdevice-interface"></a>Interfaccia IWMDRMDevice

Questa interfaccia non è progettata per essere implementata da un provider di servizi, ma viene fornita ai fini della documentazione completa.

L'interfaccia **IWMDRMDevice** consente a un provider di contenuti protetto di comunicare con i dispositivi che usano Windows Media DRM 10 per i dispositivi portatili.

## <a name="members"></a>Membri

L'interfaccia **IWMDRMDevice** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IWMDRMDevice** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **IWMDRMDevice** dispone di questi metodi.



| Metodo                                                                  | Descrizione                                                                                  |
|:------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------|
| [**CleanDataStore**](iwmdrmdevice-cleandatastore.md)                   | Avvia il processo di pulizia dell'archivio dati DRM sul dispositivo.<br/>                  |
| [**GetDeviceCertificate**](iwmdrmdevice-getdevicecertificate.md)       | Recupera il certificato del dispositivo.<br/>                                                 |
| [**GetMeterChallenge**](iwmdrmdevice-getmeterchallenge.md)             | Recupera la richiesta di misurazione.<br/>                                                 |
| [**GetSecureClock**](iwmdrmdevice-getsecureclock.md)                   | Recupera il clock protetto.<br/>                                                       |
| [**GetSecureClockChallenge**](iwmdrmdevice-getsecureclockchallenge.md) | Recupera la richiesta di clock sicura.<br/>                                             |
| [**Getsynct**](iwmdrmdevice-getsynclist.md)                         | Recupera l'elenco di sincronizzazione delle licenze.<br/>                                       |
| [**IsWMDRMDevice**](iwmdrmdevice-iswmdrmdevice.md)                     | Determina se il dispositivo supporta Windows Media DRM 10 per i dispositivi portatili.<br/> |
| [**Viene chiamato SetLicenseResponse**](iwmdrmdevice-setlicenseresponse.md)           | Imposta la risposta della licenza.<br/>                                                        |
| [**SetMeterResponse**](iwmdrmdevice-setmeterresponse.md)               | Imposta la risposta di misurazione.<br/>                                                       |
| [**SetSecureClockResponse**](iwmdrmdevice-setsecureclockresponse.md)   | Imposta la risposta del clock protetto.<br/>                                                   |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfacce per i provider di servizi**](interfaces-for-service-providers.md)
</dt> </dl>

 


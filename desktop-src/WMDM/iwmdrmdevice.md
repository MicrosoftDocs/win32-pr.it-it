---
title: Interfaccia IWMDRMDevice
description: Questa interfaccia non deve essere implementata da un provider di servizi, ma viene fornita ai fini della documentazione completa. L'interfaccia IWMDRMDevice consente a un provider di contenuti sicuro di comunicare con i dispositivi che usano Windows Media DRM 10 per dispositivi portatili.
ms.assetid: ebad4acd-16cc-433f-a5e0-fcae59030f55
keywords:
- Interfaccia IWMDRMDevice windows Media Device Manager
- Interfaccia IWMDRMDevice di Gestione dispositivi multimediali , descritta
topic_type:
- apiref
api_name:
- IWMDRMDevice
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: fee40eb6fdada2374b0f571a201ff53fb38f41de7f3cac5eeaa2159475bfdb11
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120005121"
---
# <a name="iwmdrmdevice-interface"></a>Interfaccia IWMDRMDevice

Questa interfaccia non deve essere implementata da un provider di servizi, ma viene fornita ai fini della documentazione completa.

**L'interfaccia IWMDRMDevice** consente a un provider di contenuti sicuro di comunicare con i dispositivi che usano Windows Media DRM 10 per dispositivi portatili.

## <a name="members"></a>Membri

**L'interfaccia IWMDRMDevice** eredita dall'interfaccia [**IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IWMDRMDevice** include anche questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

**L'interfaccia IWMDRMDevice** include questi metodi.



| Metodo                                                                  | Descrizione                                                                                  |
|:------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------|
| [**CleanDataStore**](iwmdrmdevice-cleandatastore.md)                   | Avvia il processo di pulizia dell'archivio dati DRM nel dispositivo.<br/>                  |
| [**GetDeviceCertificate**](iwmdrmdevice-getdevicecertificate.md)       | Recupera il certificato del dispositivo.<br/>                                                 |
| [**GetMeterChallenge**](iwmdrmdevice-getmeterchallenge.md)             | Recupera la richiesta di misurazione.<br/>                                                 |
| [**GetSecureClock**](iwmdrmdevice-getsecureclock.md)                   | Recupera l'orologio protetto.<br/>                                                       |
| [**GetSecureClockChallenge**](iwmdrmdevice-getsecureclockchallenge.md) | Recupera la richiesta di clock sicuro.<br/>                                             |
| [**GetSyncList**](iwmdrmdevice-getsynclist.md)                         | Recupera l'elenco di sincronizzazione delle licenze.<br/>                                       |
| [**IsWMDRMDevice**](iwmdrmdevice-iswmdrmdevice.md)                     | Determina se il dispositivo supporta Windows Media DRM 10 per dispositivi portatili.<br/> |
| [**SetLicenseResponse**](iwmdrmdevice-setlicenseresponse.md)           | Imposta la risposta della licenza.<br/>                                                        |
| [**SetMeterResponse**](iwmdrmdevice-setmeterresponse.md)               | Imposta la risposta di misurazione.<br/>                                                       |
| [**SetSecureClockResponse**](iwmdrmdevice-setsecureclockresponse.md)   | Imposta la risposta dell'orologio protetto.<br/>                                                   |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfacce per i provider di servizi**](interfaces-for-service-providers.md)
</dt> </dl>

 


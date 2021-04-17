---
title: Interfaccia IWMDRMDeviceApp
description: L'interfaccia IWMDRMDeviceApp consente a un'applicazione di misurare, sincronizzare le licenze e aggiornare i componenti DRM di un dispositivo.
ms.assetid: e47167c2-ea14-4173-8ce9-8d8540a0fc73
keywords:
- Interfaccia IWMDRMDeviceApp Windows Media Gestione dispositivi
- Interfaccia IWMDRMDeviceApp Windows Media Gestione dispositivi, descritta
topic_type:
- apiref
api_name:
- IWMDRMDeviceApp
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9cf44295c9972d7549eb4a82fda7c415ba81c31d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106300308"
---
# <a name="iwmdrmdeviceapp-interface"></a>Interfaccia IWMDRMDeviceApp

\[La funzionalità DRM di Windows Media è deprecata e non deve essere utilizzata. In alternativa, usare [Microsoft PlayReady](/windows/uwp/audio-video-camera/playready-client-sdk) .\]

L'interfaccia **IWMDRMDeviceApp** consente a un'applicazione di misurare, sincronizzare le licenze e aggiornare i componenti DRM di un dispositivo. Questa interfaccia funziona solo con i dispositivi che supportano Windows Media DRM 10 per i dispositivi portatili.

Per ottenere questa interfaccia, chiamare **CoCreateInstance**, passando CLSID \_ WMDRMDeviceApp.

> [!Note]  
> Questa interfaccia viene definita nel file di intestazione compilato da WMDRMDeviceApp. idl. Questa intestazione **\# include** s "WMDM. h". Potrebbe essere necessario modificare il nome del file in modo che corrisponda all'intestazione compilata da WMDM. idl.

 

## <a name="members"></a>Membri

L'interfaccia **IWMDRMDeviceApp** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IWMDRMDeviceApp** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **IWMDRMDeviceApp** dispone di questi metodi.



| Metodo                                                                   | Descrizione                                                                                                                                |
|:-------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------|
| [**AcquireDeviceData**](iwmdrmdeviceapp-acquiredevicedata.md)           | Inizializza o reimposta un clock sicuro del dispositivo<br/>                                                                                     |
| [**GenerateMeterChallenge**](iwmdrmdeviceapp-generatemeterchallenge.md) | Acquisisce i dati di misurazione da un dispositivo.<br/>                                                                                           |
| [**ProcessMeterResponse**](iwmdrmdeviceapp-processmeterresponse.md)     | Reimposta alcuni o tutti i conteggi di misurazione in un dispositivo, dopo che i dati del dispositivo sono stati inviati ed elaborati dal server.<br/> |
| [**QueryDeviceStatus**](iwmdrmdeviceapp-querydevicestatus.md)           | Esegue una query su un dispositivo per lo stato e le funzionalità DRM correnti.<br/>                                                                   |
| [**SynchronizeLicenses**](iwmdrmdeviceapp-synchronizelicenses.md)       | Aggiorna le licenze in un dispositivo quando la scadenza è prossima.<br/>                                                                   |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Gestione del contenuto protetto nell'applicazione**](handling-protected-content-in-the-application.md)
</dt> <dt>

[**Interfacce per le applicazioni**](interfaces-for-applications.md)
</dt> <dt>

[**Misurazione dell'utilizzo del contenuto**](metering-content-usage.md)
</dt> </dl>

 


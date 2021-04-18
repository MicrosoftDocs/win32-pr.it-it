---
description: L'interfaccia ITAudioDeviceControl espone metodi che consentono a un'applicazione di ottenere e impostare parametri per il controllo di un dispositivo audio.
ms.assetid: 9a557cb2-acad-406c-9a87-18cbe96e8a9f
title: Interfaccia ITAudioDeviceControl (Ipmsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 589bf50ee219f200a81aed7057b7755f203b2275
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331905"
---
# <a name="itaudiodevicecontrol-interface"></a>Interfaccia ITAudioDeviceControl

\[ Questa interfaccia non è disponibile per l'utilizzo in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo. L'API del client RTC fornisce funzionalità simili.\]

L'interfaccia **ITAudioDeviceControl** espone metodi che consentono a un'applicazione di ottenere e impostare parametri per il controllo di un dispositivo audio.

Questa interfaccia viene implementata da [IPConf msp](ipconf-msp.md) e [H323 msp](h323-msp.md). Viene esposto quando una chiamata utilizza questi provider di servizi o un provider di servizi di terze parti che implementa questa interfaccia. Per ottenere un puntatore all'interfaccia **ITAudioDeviceControl** , chiamare **QueryInterface** sull'interfaccia [**ITStream**](/windows/win32/api/tapi3if/nn-tapi3if-itstream) che controlla il dispositivo audio corrispondente al flusso. Il tipo di supporto dell'interfaccia **ITStream** deve essere audio per l'esposizione dell'interfaccia **ITAudioDeviceControl** .

## <a name="members"></a>Membri

L'interfaccia **ITAudioDeviceControl** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **ITAudioDeviceControl** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **ITAudioDeviceControl** dispone di questi metodi.



| Metodo                                              | Descrizione                                                                                             |
|:----------------------------------------------------|:--------------------------------------------------------------------------------------------------------|
| [**Ottieni**](/windows/desktop/api/tapi3if/nf-tapi3if-itasrterminalevent-get_call)          | Ottiene il valore di una [proprietà del dispositivo audio](audiodeviceproperty.md)specificata.<br/>                  |
| [**GetRange**](/windows/desktop/api/tapi3if/nf-tapi3if-itasrterminalevent-get_terminal) | Ottiene l'intervallo di valori validi per una determinata [proprietà del dispositivo audio](audiodeviceproperty.md).<br/> |
| [**Set**](/windows/desktop/api/tapi3if/nf-tapi3if-itasrterminalevent-get_error)         | Imposta il valore di una [proprietà del dispositivo audio](audiodeviceproperty.md)specificata.<br/>                  |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|--------------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 3,1<br/>                                                         |
| Intestazione<br/>       | <dl> <dt>Ipmsp. h</dt> </dl>   |
| Libreria<br/>      | <dl> <dt>UUID. lib</dt> </dl>  |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[MSP IPConf](ipconf-msp.md)
</dt> </dl>

 


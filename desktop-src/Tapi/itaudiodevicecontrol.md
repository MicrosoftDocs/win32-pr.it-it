---
description: L'interfaccia ITAudioDeviceControl espone metodi che consentono a un'applicazione di ottenere e impostare parametri per il controllo di un dispositivo audio.
ms.assetid: 9a557cb2-acad-406c-9a87-18cbe96e8a9f
title: Interfaccia ITAudioDeviceControl (Ipmsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac06118300d9170f4928d7be5d2cf1bc3b69261f0062d6ffecd403389e564d48
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119003439"
---
# <a name="itaudiodevicecontrol-interface"></a>Interfaccia ITAudioDeviceControl

\[Questa interfaccia non è disponibile per l'uso in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo. L'API client RTC offre funzionalità simili.\]

**L'interfaccia ITAudioDeviceControl** espone metodi che consentono a un'applicazione di ottenere e impostare parametri per il controllo di un dispositivo audio.

Questa interfaccia viene implementata da [IPConf MSP](ipconf-msp.md) e [H323 MSP.](h323-msp.md) Viene esposto quando una chiamata usa questi provider di servizi o un provider di servizi di terze parti che implementa questa interfaccia. Per ottenere un puntatore **all'interfaccia ITAudioDeviceControl,** chiamare **QueryInterface** sull'interfaccia [**ITStream**](/windows/win32/api/tapi3if/nn-tapi3if-itstream) che controlla il dispositivo audio corrispondente al flusso. Il tipo di supporto **dell'interfaccia ITStream** deve essere audio per **l'esposizione dell'interfaccia ITAudioDeviceControl.**

## <a name="members"></a>Membri

**L'interfaccia ITAudioDeviceControl** eredita dall'interfaccia [**IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **ITAudioDeviceControl** include anche questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

**L'interfaccia ITAudioDeviceControl** include questi metodi.



| Metodo                                              | Descrizione                                                                                             |
|:----------------------------------------------------|:--------------------------------------------------------------------------------------------------------|
| [**Ottieni**](/windows/desktop/api/tapi3if/nf-tapi3if-itasrterminalevent-get_call)          | Ottiene il valore di una determinata [proprietà del dispositivo audio.](audiodeviceproperty.md)<br/>                  |
| [**GetRange**](/windows/desktop/api/tapi3if/nf-tapi3if-itasrterminalevent-get_terminal) | Ottiene l'intervallo di valori validi per una determinata [proprietà del dispositivo audio.](audiodeviceproperty.md)<br/> |
| [**Impostare**](/windows/desktop/api/tapi3if/nf-tapi3if-itasrterminalevent-get_error)         | Imposta il valore di una determinata [proprietà del dispositivo audio.](audiodeviceproperty.md)<br/>                  |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|--------------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 3.1<br/>                                                         |
| Intestazione<br/>       | <dl> <dt>Ipmsp.h</dt> </dl>   |
| Libreria<br/>      | <dl> <dt>Uuid.lib</dt> </dl>  |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[IPConf MSP](ipconf-msp.md)
</dt> </dl>

 


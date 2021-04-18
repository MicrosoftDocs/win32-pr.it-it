---
description: L'interfaccia ITAudioSettings espone metodi che consentono a un'applicazione di ottenere e impostare parametri per il controllo di un dispositivo audio.
ms.assetid: 56607024-255d-4d1b-9ca0-6086eff7b7b2
title: Interfaccia ITAudioSettings (Ipmsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eaf2566c7438dbcd14cdacee46cc4d5ec4166731
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331598"
---
# <a name="itaudiosettings-interface"></a>Interfaccia ITAudioSettings

\[ Questa interfaccia non è disponibile per l'utilizzo in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo. L'API del client RTC fornisce funzionalità simili.\]

L'interfaccia **ITAudioSettings** espone metodi che consentono a un'applicazione di ottenere e impostare parametri per il controllo di un dispositivo audio.

Questa interfaccia viene implementata da [IPConf msp](ipconf-msp.md) e [H323 msp](h323-msp.md). Viene esposto solo quando una chiamata utilizza questi provider di servizi.

## <a name="members"></a>Membri

L'interfaccia **ITAudioSettings** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **ITAudioSettings** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **ITAudioSettings** dispone di questi metodi.



| Metodo                                              | Descrizione                                                                                                |
|:----------------------------------------------------|:-----------------------------------------------------------------------------------------------------------|
| [**Ottieni**](/windows/desktop/api/tapi3if/nf-tapi3if-itasrterminalevent-get_call)          | Ottiene il valore di una [proprietà dell'impostazione audio](audiosettingsproperty.md)specificata.<br/>                  |
| [**GetRange**](/windows/desktop/api/tapi3if/nf-tapi3if-itasrterminalevent-get_terminal) | Ottiene l'intervallo di valori validi per una [proprietà di impostazione audio](audiosettingsproperty.md)specificata.<br/> |
| [**Set**](/windows/desktop/api/tapi3if/nf-tapi3if-itasrterminalevent-get_error)         | Imposta il valore di una [proprietà dell'impostazione audio](audiosettingsproperty.md)specificata.<br/>                  |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|--------------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 3,1<br/>                                                         |
| Intestazione<br/>       | <dl> <dt>Ipmsp. h</dt> </dl>   |
| Libreria<br/>      | <dl> <dt>UUID. lib</dt> </dl>  |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl> |



 


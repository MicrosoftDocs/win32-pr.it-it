---
description: L'interfaccia ITAudioSettings espone metodi che consentono a un'applicazione di ottenere e impostare parametri per il controllo di un dispositivo audio.
ms.assetid: 56607024-255d-4d1b-9ca0-6086eff7b7b2
title: Interfaccia ITAudioSettings (Ipmsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85ce0c7a92e34583947be983ed4d28391eb70c02697313aedee21a7158c9c3b3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119140384"
---
# <a name="itaudiosettings-interface"></a>Interfaccia ITAudioSettings

\[Questa interfaccia non è disponibile per l'uso in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo. L'API client rtc offre funzionalità simili.\]

**L'interfaccia ITAudioSettings** espone metodi che consentono a un'applicazione di ottenere e impostare parametri per il controllo di un dispositivo audio.

Questa interfaccia viene implementata da [IPConf MSP](ipconf-msp.md) e [H323 MSP.](h323-msp.md) Viene esposto solo quando una chiamata utilizza questi provider di servizi.

## <a name="members"></a>Membri

**L'interfaccia ITAudioSettings** eredita dall'interfaccia [**IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **ITAudioSettings** include anche questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

**L'interfaccia ITAudioSettings** include questi metodi.



| Metodo                                              | Descrizione                                                                                                |
|:----------------------------------------------------|:-----------------------------------------------------------------------------------------------------------|
| [**Ottieni**](/windows/desktop/api/tapi3if/nf-tapi3if-itasrterminalevent-get_call)          | Ottiene il valore di una determinata proprietà [dell'impostazione audio](audiosettingsproperty.md).<br/>                  |
| [**GetRange**](/windows/desktop/api/tapi3if/nf-tapi3if-itasrterminalevent-get_terminal) | Ottiene l'intervallo di valori validi per una determinata proprietà [dell'impostazione audio](audiosettingsproperty.md).<br/> |
| [**Impostare**](/windows/desktop/api/tapi3if/nf-tapi3if-itasrterminalevent-get_error)         | Imposta il valore di una determinata proprietà [dell'impostazione audio](audiosettingsproperty.md).<br/>                  |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|--------------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 3.1<br/>                                                         |
| Intestazione<br/>       | <dl> <dt>Ipmsp.h</dt> </dl>   |
| Libreria<br/>      | <dl> <dt>Uuid.lib</dt> </dl>  |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl> |



 


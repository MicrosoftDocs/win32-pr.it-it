---
description: L'interfaccia ITParticipantSubStreamControl viene implementata da IPConf MSP.
ms.assetid: d5af0fb1-af18-4efb-9b68-1fa60c1272f6
title: Interfaccia ITParticipantSubStreamControl (Confpriv.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e910022d45ca9f9516adbe8aeebbdb172d66f28ab1bf8cb23219c2eee80f56cf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119774601"
---
# <a name="itparticipantsubstreamcontrol-interface"></a>Interfaccia ITParticipantSubStreamControl

\[**ITParticipantSubStreamControl** non è disponibile per l'uso in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo. L'API client rtc offre funzionalità simili.\]

**L'interfaccia ITParticipantSubStreamControl** viene implementata da IPConf MSP. Questa interfaccia viene esposta nell'oggetto di chiamata. Questa interfaccia fornisce metodi che consentono a un'applicazione di individuare o controllare la corrispondenza tra il flusso secondario e il partecipante. **L'interfaccia ITParticipantSubStreamControl** viene creata chiamando **QueryInterface** [**in ITCallInfo.**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo)

## <a name="members"></a>Membri

**L'interfaccia ITParticipantSubStreamControl** eredita dall'interfaccia [**IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **ITParticipantSubStreamControl** include anche questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

**L'interfaccia ITParticipantSubStreamControl** include questi metodi.



| Metodo                                                                                              | Descrizione                                                     |
|:----------------------------------------------------------------------------------------------------|:----------------------------------------------------------------|
| [**get \_ ParticipantFromSubStream**](itparticipantsubstreamcontrol-get-participantfromsubstream.md) | Ottiene i partecipanti associati a un flusso secondario specificato.<br/> |
| [**get \_ SubStreamFromParticipant**](itparticipantsubstreamcontrol-get-substreamfromparticipant.md) | Ottiene i sottostream associati a un determinato partecipante.<br/> |
| [**SwitchTerminalToSubStream**](itparticipantsubstreamcontrol-switchterminaltosubstream.md)        | Imposta un partecipante in un flusso secondario.<br/>                   |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|---------------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 3.0 o versione successiva<br/>                                                 |
| Intestazione<br/>       | <dl> <dt>Confpriv.h</dt> </dl> |
| Libreria<br/>      | <dl> <dt>Uuid.lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl>  |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ITParticipant**](itparticipant.md)
</dt> <dt>

[**ITSubStream**](/windows/win32/api/tapi3if/nn-tapi3if-itsubstream)
</dt> </dl>

 


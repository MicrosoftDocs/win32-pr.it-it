---
description: L'interfaccia ITParticipantSubStreamControl viene implementata da IPConf MSP.
ms.assetid: d5af0fb1-af18-4efb-9b68-1fa60c1272f6
title: Interfaccia ITParticipantSubStreamControl (Confpriv. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 799b1a85c6619e1175e620f2c5c5ef851005ba50
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333664"
---
# <a name="itparticipantsubstreamcontrol-interface"></a>Interfaccia ITParticipantSubStreamControl

\[**ITParticipantSubStreamControl** non è disponibile per l'utilizzo in Windows Vista, windows Server 2008 e nelle versioni successive del sistema operativo. L'API del client RTC fornisce funzionalità simili.\]

L'interfaccia **ITParticipantSubStreamControl** viene implementata da IPConf msp. Questa interfaccia viene esposta nell'oggetto chiamata. Questa interfaccia fornisce metodi che consentono a un'applicazione di individuare o controllare la corrispondenza del sottoflusso al partecipante. L'interfaccia **ITParticipantSubStreamControl** viene creata chiamando **QueryInterface** in [**ITCallInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo).

## <a name="members"></a>Membri

L'interfaccia **ITParticipantSubStreamControl** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **ITParticipantSubStreamControl** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **ITParticipantSubStreamControl** dispone di questi metodi.



| Metodo                                                                                              | Descrizione                                                     |
|:----------------------------------------------------------------------------------------------------|:----------------------------------------------------------------|
| [**ottenere \_ ParticipantFromSubStream**](itparticipantsubstreamcontrol-get-participantfromsubstream.md) | Ottiene i partecipanti associati a un sottoflusso specificato.<br/> |
| [**ottenere \_ SubStreamFromParticipant**](itparticipantsubstreamcontrol-get-substreamfromparticipant.md) | Ottiene i flussi sottoflussi associati a un determinato partecipante.<br/> |
| [**SwitchTerminalToSubStream**](itparticipantsubstreamcontrol-switchterminaltosubstream.md)        | Imposta un partecipante a un sottoflusso.<br/>                   |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|---------------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 3,0 o versione successiva<br/>                                                 |
| Intestazione<br/>       | <dl> <dt>Confpriv. h</dt> </dl> |
| Libreria<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl>  |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ITParticipant**](itparticipant.md)
</dt> <dt>

[**ITSubStream**](/windows/win32/api/tapi3if/nn-tapi3if-itsubstream)
</dt> </dl>

 


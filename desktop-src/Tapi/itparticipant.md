---
description: L'interfaccia ITParticipant viene implementata da IPConf MSP. Consente a un'applicazione di recuperare informazioni sui partecipanti alla conferenza e ottenere i puntatori ai flussi associati a tali partecipanti.
ms.assetid: 8c3edfc1-3165-48b7-9d83-8892c192498b
title: Interfaccia ITParticipant (Ipmsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e8b7aa9d845d8d2489be0850bcc3fcf3f93ccdac
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331046"
---
# <a name="itparticipant-interface"></a>Interfaccia ITParticipant

\[**ITParticipant** non è disponibile per l'utilizzo in Windows Vista, windows Server 2008 e nelle versioni successive del sistema operativo. L'API del client RTC fornisce funzionalità simili.\]

L'interfaccia **ITParticipant** viene implementata da [IPConf msp](ipconf-msp.md). Consente a un'applicazione di recuperare informazioni sui partecipanti alla conferenza e ottenere i puntatori ai flussi associati a tali partecipanti.

Questa interfaccia viene esposta nell'oggetto chiamata quando una chiamata utilizza la conferenza IP. È possibile ottenere un puntatore chiamando **QueryInterface** utilizzando un puntatore [**ITCallInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo) .

## <a name="members"></a>Membri

L'interfaccia **ITParticipant** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **ITParticipant** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **ITParticipant** dispone di questi metodi.



| Metodo                                                                      | Descrizione                                                                                                                                                             |
|:----------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**EnumerateStreams**](itparticipant-enumeratestreams.md)                  | Enumera i flussi associati al partecipante corrente.<br/>                                                                                                  |
| [**ottenere \_ MediaTypes**](itparticipant-get-mediatypes.md)                     | Ottiene i [**tipi di supporto**](tapimediatype--constants.md) associati a un partecipante.<br/>                                                                      |
| [**ottenere \_ ParticipantTypedInfo**](itparticipant-get-participanttypedinfo.md) | Ottiene una rappresentazione BSTR del tipo di informazioni necessario, ad esempio PTI \_ EMAILADDRESS.<br/>                                                                     |
| [**ottenere \_ lo stato**](itparticipant-get-status.md)                             | Ottiene lo stato del partecipante.<br/>                                                                                                                          |
| [**ottenere i \_ flussi**](itparticipant-get-streams.md)                           | Crea una raccolta di flussi associati al partecipante corrente. Fornito per le applicazioni client di automazione, ad esempio quelle scritte in Visual Basic.<br/> |
| [**Inserisci \_ stato**](itparticipant-put-status.md)                             | Imposta un valore che indica se un flusso associato al partecipante è abilitato.<br/>                                                                                            |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|--------------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 3,0 o versione successiva<br/>                                                |
| Intestazione<br/>       | <dl> <dt>Ipmsp. h</dt> </dl>   |
| Libreria<br/>      | <dl> <dt>UUID. lib</dt> </dl>  |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[MSP IPConf](ipconf-msp.md)
</dt> <dt>

[Interfacce MSP IPConf](ipconf-msp-interfaces.md)
</dt> <dt>

[**ITCallInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo)
</dt> </dl>

 


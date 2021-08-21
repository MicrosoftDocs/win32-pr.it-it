---
description: L'interfaccia ITParticipant viene implementata da IPConf MSP. Consente a un'applicazione di recuperare informazioni sui partecipanti alla conferenza e di ottenere puntatori ai flussi associati a tali partecipanti.
ms.assetid: 8c3edfc1-3165-48b7-9d83-8892c192498b
title: Interfaccia ITParticipant (Ipmsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fab4ff4c496616804efc1a65a728bbb658fba5bb1278939bdfb2185705684c64
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119682651"
---
# <a name="itparticipant-interface"></a>Interfaccia ITParticipant

\[**ITParticipant** non è disponibile per l'uso in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo. L'API client RTC offre funzionalità simili.\]

**L'interfaccia ITParticipant** viene implementata da [IPConf MSP.](ipconf-msp.md) Consente a un'applicazione di recuperare informazioni sui partecipanti alla conferenza e di ottenere puntatori ai flussi associati a tali partecipanti.

Questa interfaccia viene esposta nell'oggetto chiamata quando una chiamata usa la conferenza IP. È possibile ottenere un puntatore chiamando **QueryInterface** usando un [**puntatore ITCallInfo.**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo)

## <a name="members"></a>Membri

**L'interfaccia ITParticipant** eredita dall'interfaccia [**IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **ITParticipant** include anche questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

**L'interfaccia ITParticipant** include questi metodi.



| Metodo                                                                      | Descrizione                                                                                                                                                             |
|:----------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**EnumerateStreams**](itparticipant-enumeratestreams.md)                  | Enumera i flussi associati al partecipante corrente.<br/>                                                                                                  |
| [**get \_ MediaTypes**](itparticipant-get-mediatypes.md)                     | Ottiene i [**tipi di supporti**](tapimediatype--constants.md) associati a un partecipante.<br/>                                                                      |
| [**get \_ ParticipantTypedInfo**](itparticipant-get-participanttypedinfo.md) | Ottiene una rappresentazione BSTR del tipo necessario di informazioni, ad esempio PTI \_ EMAILADDRESS.<br/>                                                                     |
| [**ottenere \_ lo stato**](itparticipant-get-status.md)                             | Ottiene lo stato del partecipante.<br/>                                                                                                                          |
| [**ottenere \_ Flussi**](itparticipant-get-streams.md)                           | Crea una raccolta di flussi associati al partecipante corrente. Fornito per le applicazioni client di Automazione, ad esempio quelle scritte in Visual Basic.<br/> |
| [**Put \_ Status (Stato put)**](itparticipant-put-status.md)                             | Imposta se un flusso associato al partecipante è abilitato.<br/>                                                                                            |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|--------------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 3.0 o versione successiva<br/>                                                |
| Intestazione<br/>       | <dl> <dt>Ipmsp.h</dt> </dl>   |
| Libreria<br/>      | <dl> <dt>Uuid.lib</dt> </dl>  |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[IPConf MSP](ipconf-msp.md)
</dt> <dt>

[Interfacce MSP IPConf](ipconf-msp-interfaces.md)
</dt> <dt>

[**ITCallInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo)
</dt> </dl>

 


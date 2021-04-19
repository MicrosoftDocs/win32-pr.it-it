---
description: L'interfaccia ITLocalParticipant viene esposta nell'oggetto flusso quando IPConf MSP supporta la chiamata.
ms.assetid: 64965ae2-e30b-4353-a502-f96018da71a5
title: Interfaccia ITLocalParticipant (Confpriv. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d4017837a0b970cb791cdf454437fe2d48720028
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330369"
---
# <a name="itlocalparticipant-interface"></a>Interfaccia ITLocalParticipant

L'interfaccia **ITLocalParticipant** viene esposta nell'oggetto flusso quando IPConf msp supporta la chiamata. Il MSP implementa i metodi che consentono a un'applicazione di ottenere e impostare informazioni sul partecipante. L'interfaccia **ITLocalParticipant** viene creata chiamando **QueryInterface** in [**ITStream**](/windows/win32/api/tapi3if/nn-tapi3if-itstream).

## <a name="members"></a>Membri

L'interfaccia **ITLocalParticipant** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **ITLocalParticipant** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **ITLocalParticipant** dispone di questi metodi.



| Metodo                                                                                     | Descrizione                                                                            |
|:-------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------|
| [**ottenere \_ LocalParticipantTypedInfo**](itlocalparticipant-get-localparticipanttypedinfo.md) | Ottiene le informazioni sul partecipante, ad esempio il nome della posta elettronica o la posizione geografica.<br/> |
| [**Inserisci \_ LocalParticipantTypedInfo**](itlocalparticipant-put-localparticipanttypedinfo.md) | Imposta le informazioni sul partecipante.<br/>                                               |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|---------------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 3,0 o versione successiva<br/>                                                 |
| Intestazione<br/>       | <dl> <dt>Confpriv. h</dt> </dl> |
| Libreria<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl>  |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ITStream**](/windows/win32/api/tapi3if/nn-tapi3if-itstream)
</dt> </dl>

 


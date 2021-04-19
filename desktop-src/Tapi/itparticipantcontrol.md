---
description: L'interfaccia ITParticipantControl viene implementata da IPConf MSP.
ms.assetid: e617f2a4-6be8-4cb1-9f03-470c5100b834
title: Interfaccia ITParticipantControl (Confpriv. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 96075748f0c35cbc5af3c6cd07277d15222e0658
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328731"
---
# <a name="itparticipantcontrol-interface"></a>Interfaccia ITParticipantControl

\[**ITParticipantControl** non è disponibile per l'utilizzo in Windows Vista, windows Server 2008 e nelle versioni successive del sistema operativo. L'API del client RTC fornisce funzionalità simili.\]

L'interfaccia **ITParticipantControl** viene implementata da IPConf msp. Questa interfaccia viene esposta nell'oggetto chiamata. Questa interfaccia consente a un'applicazione di recuperare i puntatori ai partecipanti in una conferenza. L'interfaccia **ITParticipantControl** viene creata chiamando **QueryInterface** in [**ITCallInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo).

## <a name="members"></a>Membri

L'interfaccia **ITParticipantControl** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **ITParticipantControl** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **ITParticipantControl** dispone di questi metodi.



| Metodo                                                                      | Descrizione                                                                                                                                                                 |
|:----------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**EnumerateParticipants**](itparticipantcontrol-enumerateparticipants.md) | Enumera i partecipanti attualmente associati alla conferenza.<br/>                                                                                                    |
| [**Ricevi \_ i partecipanti**](itparticipantcontrol-get-participants.md)          | Crea una raccolta di partecipanti associati alla conferenza corrente. Fornito per le applicazioni client di automazione, ad esempio quelle scritte in Visual Basic.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|---------------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 3,0 o versione successiva<br/>                                                 |
| Intestazione<br/>       | <dl> <dt>Confpriv. h</dt> </dl> |
| Libreria<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl>  |



 


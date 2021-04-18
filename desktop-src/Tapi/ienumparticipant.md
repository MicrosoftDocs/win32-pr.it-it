---
description: "L'interfaccia IEnumParticipant fornisce metodi di enumerazione standard COM per l'interfaccia ITParticipant. Il metodo ITParticipantControl:: EnumerateParticipants restituisce un puntatore a IEnumParticipant."
ms.assetid: 8534d102-06ce-4e82-8f9c-9ab9f0d14df9
title: Interfaccia IEnumParticipant (Confpriv. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 21a20a2cd8e72c5c44b054fc4658b304c8b4fa41
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330747"
---
# <a name="ienumparticipant-interface"></a>Interfaccia IEnumParticipant

\[**IEnumParticipant** non è disponibile per l'utilizzo in Windows Vista, windows Server 2008 e nelle versioni successive del sistema operativo. L'API del client RTC fornisce funzionalità simili.\]

L'interfaccia **IEnumParticipant** fornisce metodi di enumerazione standard com per l'interfaccia [**ITParticipant**](itparticipant.md) . Il metodo [**ITParticipantControl:: EnumerateParticipants**](itparticipantcontrol-enumerateparticipants.md) restituisce un puntatore a **IEnumParticipant**.

L'interfaccia **IEnumParticipant** è nascosta per Visual Basic e linguaggi di scripting.

## <a name="members"></a>Membri

L'interfaccia **IEnumParticipant** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IEnumParticipant** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **IEnumParticipant** dispone di questi metodi.



| Metodo                                  | Descrizione                                                                                        |
|:----------------------------------------|:---------------------------------------------------------------------------------------------------|
| [**Clone**](ienumparticipant-clone.md) | Crea un altro enumeratore che contiene lo stesso stato di enumerazione di quello corrente.<br/> |
| [**Avanti**](ienumparticipant-next.md)   | Ottiene il numero specificato successivo di elementi nella sequenza di enumerazione.<br/>                 |
| [**Reset**](ienumparticipant-reset.md) | Reimposta l'inizio della sequenza di enumerazione.<br/>                                    |
| [**Ignora**](ienumparticipant-skip.md)   | Ignora il numero specificato successivo di elementi nella sequenza di enumerazione.<br/>           |



 

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
</dt> </dl>

 


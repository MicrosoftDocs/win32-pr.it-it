---
description: Modifica una descrizione della conferenza testuale.
ms.assetid: b9ce61d1-3fc5-4963-8d2f-586a4b6a159d
title: Interfaccia ITConferenceBlob (sdpblb. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c961b8fb006f1e172f82827216292cb9d12a158f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328226"
---
# <a name="itconferenceblob-interface"></a>Interfaccia ITConferenceBlob

\[ I controlli e le interfacce per la comunicazione di telefonia IP Rendezvous non sono disponibili per l'uso in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo. L'API del client RTC fornisce funzionalità simili.\]

L'interfaccia **ITConferenceBlob** manipola una descrizione della conferenza testuale. L'interfaccia è progettata per essere indipendente dal formato e dalla sintassi della descrizione della conferenza. Per modificare aspetti specifici della descrizione della conferenza, l'applicazione deve eseguire una query per un'altra interfaccia. Attualmente sono supportate solo le descrizioni delle conferenze SDP; l'applicazione deve usare **QueryInterface** per [**ITSdp**](itsdp.md) per accedere ai diversi campi della descrizione della conferenza SDP. L'interfaccia **ITConferenceBlob** viene creata chiamando **QueryInterface** in [**ITDirectoryObject**](/windows/desktop/api/Rend/nn-rend-itdirectoryobject).

## <a name="members"></a>Membri

L'interfaccia **ITConferenceBlob** eredita dall'interfaccia [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **ITConferenceBlob** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **ITConferenceBlob** dispone di questi metodi.



| Metodo                                                             | Descrizione                                                                                                                                   |
|:-------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------|
| [**Ottieni \_ caratteri**](itconferenceblob-get-characterset.md)     | Ottiene l'indicatore del [**\_ \_ set di caratteri BLOB**](blob-character-set.md) che indica se i caratteri BLOB sono ASCII, Unicode e così via.<br/> |
| [**ottenere \_ ConferenceBlob**](itconferenceblob-get-conferenceblob.md) | Ottiene un puntatore al BLOB della conferenza.<br/>                                                                                             |
| [**Init**](itconferenceblob-init.md)                              | Inizializza il BLOB della conferenza.<br/>                                                                                                   |
| [**SetConferenceBlob**](itconferenceblob-setconferenceblob.md)    | Salva le modifiche apportate al BLOB della conferenza.<br/>                                                                                            |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|---------------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 3,0 o versione successiva<br/>                                                 |
| Intestazione<br/>       | <dl> <dt>Sdpblb. h</dt> </dl>   |
| Libreria<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



 


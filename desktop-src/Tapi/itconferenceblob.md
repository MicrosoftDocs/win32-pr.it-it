---
description: Modifica una descrizione testuale della conferenza.
ms.assetid: b9ce61d1-3fc5-4963-8d2f-586a4b6a159d
title: Interfaccia ITConferenceBlob (Sdpblb.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa130e4456f206b27e41d03ead47138c777f9dad9e41d5d834bb018b29fc5447
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119379091"
---
# <a name="itconferenceblob-interface"></a>Interfaccia ITConferenceBlob

\[Le interfacce e i controlli della conferenza di telefonia IP di Rendezvous non sono disponibili per l'uso in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo. L'API client rtc offre funzionalità simili.\]

**L'interfaccia ITConferenceBlob** modifica una descrizione testuale della conferenza. L'interfaccia deve essere indipendente dal formato e dalla sintassi della descrizione della conferenza. Per modificare aspetti specifici della descrizione della conferenza, l'applicazione deve eseguire una query per un'altra interfaccia. Attualmente sono supportate solo le descrizioni delle conferenze SDP. L'applicazione deve usare **QueryInterface** per [**ITSdp**](itsdp.md) per accedere ai vari campi della descrizione della conferenza SDP. **L'interfaccia ITConferenceBlob** viene creata chiamando **QueryInterface** [**su ITDirectoryObject.**](/windows/desktop/api/Rend/nn-rend-itdirectoryobject)

## <a name="members"></a>Membri

**L'interfaccia ITConferenceBlob** eredita dall'interfaccia [**IDispatch.**](/windows/win32/api/oaidl/nn-oaidl-idispatch) **ITConferenceBlob** include anche questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

**L'interfaccia ITConferenceBlob** include questi metodi.



| Metodo                                                             | Descrizione                                                                                                                                   |
|:-------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------|
| [**get \_ CharacterSet**](itconferenceblob-get-characterset.md)     | Ottiene [**\_ l'indicatore BLOB CHARACTER \_ SET**](blob-character-set.md) che indica se i caratteri BLOB sono in formato ASCII, Unicode e così via.<br/> |
| [**get \_ ConferenceBlob**](itconferenceblob-get-conferenceblob.md) | Ottiene un puntatore al BLOB della conferenza.<br/>                                                                                             |
| [**Init**](itconferenceblob-init.md)                              | Inizializza il BLOB della conferenza.<br/>                                                                                                   |
| [**SetConferenceBlob**](itconferenceblob-setconferenceblob.md)    | Esegue il commit delle modifiche nel BLOB della conferenza.<br/>                                                                                            |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|---------------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 3.0 o versione successiva<br/>                                                 |
| Intestazione<br/>       | <dl> <dt>Sdpblb.h</dt> </dl>   |
| Libreria<br/>      | <dl> <dt>Uuid.lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



 


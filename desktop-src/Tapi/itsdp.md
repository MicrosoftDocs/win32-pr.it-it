---
description: L'interfaccia ITSdp fornisce i metodi per la manipolazione di un componente BLOB della conferenza di Session Descriptor Protocol (SDP, see RFC 2327).
ms.assetid: 77c1e302-6290-4eeb-b7c9-462a13b29dcd
title: Interfaccia ITSdp (sdpblb. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 401dbe2548375227be2ca024ee75de3054fa6f6f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333968"
---
# <a name="itsdp-interface"></a>Interfaccia ITSdp

\[ I controlli e le interfacce per la comunicazione di telefonia IP Rendezvous non sono disponibili per l'uso in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo. L'API del client RTC fornisce funzionalità simili.\]

L'interfaccia **ITSdp** fornisce i metodi per la manipolazione di un componente BLOB della conferenza di Session Descriptor Protocol (SDP, see RFC 2327). Offre le funzionalità seguenti:

-   Consente di accedere ad alcune delle proprietà comuni a tutti i supporti. Sono inclusi gli attributi relativi alle informazioni personali del creatore, alla descrizione della sessione e al tipo di indirizzo.
-   Fornisce il punto di partenza per l'accesso alle raccolte di tempo e supporti tramite proprietà.

L'interfaccia **ITSdp** viene creata chiamando **QueryInterface** in [**ITConferenceBlob**](itconferenceblob.md).

## <a name="members"></a>Membri

L'interfaccia **ITSdp** eredita dall'interfaccia [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **ITSdp** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **ITSdp** dispone di questi metodi.



| Metodo                                                    | Descrizione                                                                                         |
|:----------------------------------------------------------|:----------------------------------------------------------------------------------------------------|
| [**ottenere una \_ Descrizione**](itsdp-get-description.md)         | Ottiene la descrizione della sessione.<br/>                                                            |
| [**ottenere \_ IsValid**](itsdp-get-isvalid.md)                 | Convalida il BLOB SDP per i valori di struttura e di campo.<br/>                                   |
| [**ottenere \_ MachineAddress**](itsdp-get-machineaddress.md)   | Ottiene l'indirizzo del computer dell'host di origine.<br/>                                        |
| [**ottenere \_ mediacollection**](itsdp-get-mediacollection.md) | Ottiene il puntatore all'interfaccia [**ITMediaCollection**](itmediacollection.md) per la conferenza.<br/> |
| [**Ottieni \_ nome**](itsdp-get-name.md)                       | Ottiene il nome della sessione.<br/>                                                                   |
| [**Ottieni \_ origine**](itsdp-get-originator.md)           | Ottiene l'origine della conferenza.<br/>                                                              |
| [**ottenere \_ ProtocolVersion**](itsdp-get-protocolversion.md) | Ottiene la versione del protocollo SDP.<br/>                                                           |
| [**Ottieni \_ SessionID**](itsdp-get-sessionid.md)             | Ottiene il valore NTP (Network Time Protocol) a 32 bit che funge da identificatore di sessione.<br/> |
| [**ottenere \_ SessionVersion**](itsdp-get-sessionversion.md)   | Ottiene il valore (idealmente NTP) a 32 bit che funge da versione della sessione.<br/>                  |
| [**Get \_ TimeCollection**](itsdp-get-timecollection.md)   | Ottiene il puntatore all'interfaccia [**ITTimeCollection**](ittimecollection.md) per la conferenza.<br/>   |
| [**Ottieni \_ URL**](itsdp-get-url.md)                         | Ottiene l'URL.<br/>                                                                            |
| [**GetEmailNames**](itsdp-getemailnames.md)              | Ottiene una matrice di nomi e indirizzi di posta elettronica associati al BLOB della conferenza.<br/>                |
| [**GetPhoneNumbers**](itsdp-getphonenumbers.md)          | Ottiene i numeri di telefono.<br/>                                                                  |
| [**Inserisci \_ Descrizione**](itsdp-put-description.md)         | Imposta la descrizione della sessione.<br/>                                                            |
| [**Inserisci \_ MachineAddress**](itsdp-put-machineaddress.md)   | Imposta l'indirizzo del computer dell'host di origine.<br/>                                        |
| [**\_nome put**](itsdp-put-name.md)                       | Imposta il nome della sessione.<br/>                                                                   |
| [**Inserisci \_ origine**](itsdp-put-originator.md)           | Ottiene l'origine della conferenza.<br/>                                                              |
| [**Inserisci \_ SessionVersion**](itsdp-put-sessionversion.md)   | Imposta la versione della sessione.<br/>                                                                    |
| [**Inserisci \_ URL**](itsdp-put-url.md)                         | Imposta l'URL.<br/>                                                                            |
| [**SetEmailNames**](itsdp-setemailnames.md)              | Imposta la matrice di nomi e indirizzi di posta elettronica associati al BLOB della conferenza.<br/>                 |
| [**SetPhoneNumbers**](itsdp-setphonenumbers.md)          | Imposta i numeri di telefono.<br/>                                                                  |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|---------------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 3,0 o versione successiva<br/>                                                 |
| Intestazione<br/>       | <dl> <dt>Sdpblb. h</dt> </dl>   |
| Libreria<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



 


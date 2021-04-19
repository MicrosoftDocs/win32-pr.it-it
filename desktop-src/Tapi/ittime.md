---
description: L'interfaccia ITTime è un'interfaccia specifica del provider per un oggetto BLOB di conferenza SDP (Session Descriptor Protocol).
ms.assetid: 24d33259-dcbe-47e4-9c71-fcc25f6e9a76
title: Interfaccia ITTime (sdpblb. h)
ms.topic: interface
ms.date: 05/31/2018
ms.openlocfilehash: 964fa197318d8cbe9614beb97c5bea0db94f242b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326760"
---
# <a name="ittime-interface"></a>Interfaccia ITTime

\[ I controlli e le interfacce per la comunicazione di telefonia IP Rendezvous non sono disponibili per l'uso in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo. L'API del client RTC fornisce funzionalità simili.\]

L'interfaccia **ITTime** è un'interfaccia specifica del provider per un oggetto BLOB di conferenza SDP (Session Descriptor Protocol). Consente di accedere a un set di tempi di attivazione per la sessione. I metodi [**IEnumTime:: Next**](ienumtime-next.md) e [**ITTimeCollection:: create**](ittimecollection-create.md) creano l'interfaccia **ITTime** .

## <a name="members"></a>Membri

L'interfaccia **ITTime** eredita dall'interfaccia [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **ITTime** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **ITTime** dispone di questi metodi.



| Metodo                                         | Descrizione                                                                 |
|:-----------------------------------------------|:----------------------------------------------------------------------------|
| [**ottenere \_ StartTime**](ittime-get-starttime.md) | Ottiene il valore dell'ora di inizio (NTP) a 32 bit (Network Time Protocol).<br/> |
| [**ottenere \_ StopTime**](ittime-get-stoptime.md)   | Ottiene il valore dell'ora di fine NTP.<br/>                                  |
| [**Inserisci \_ StartTime**](ittime-put-starttime.md) | Imposta il valore dell'ora di inizio NTP a 32 bit.<br/>                         |
| [**Inserisci \_ StopTime**](ittime-put-stoptime.md)   | Imposta il valore dell'ora di fine NTP.<br/>                                  |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|---------------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 3,0 o versione successiva<br/>                                                 |
| Intestazione<br/>       | <dl> <dt>Sdpblb. h</dt> </dl>   |
| Libreria<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



 


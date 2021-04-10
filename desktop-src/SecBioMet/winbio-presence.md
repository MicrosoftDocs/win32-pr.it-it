---
title: Struttura WINBIO_PRESENCE ( \_ tipi WINBIO. h)
description: Contiene informazioni sulla presenza di un utente la cui presenza viene monitorata.
ms.assetid: 810D452E-DDFA-4AB2-AEFB-0C170C0C18D4
keywords:
- Struttura di WINBIO_PRESENCE Windows Biometric Framework API
- API Windows Biometric Framework puntatore alla struttura PWINBIO_PRESENCE
topic_type:
- apiref
api_name:
- WINBIO_PRESENCE
api_location:
- winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a4a917f09f419ce8dd5eb59c9c277293261bffa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119882"
---
# <a name="winbio_presence-structure"></a>\_Struttura di presenza WINBIO

Contiene informazioni sulla presenza di un utente la cui presenza viene monitorata.

## <a name="syntax"></a>Sintassi


```C++
typedef struct _WINBIO_PRESENCE {
  WINBIO_BIOMETRIC_TYPE      Factor;
  WINBIO_BIOMETRIC_SUBTYPE   SubFactor;
  HRESULT                    Status;
  WINBIO_REJECT_DETAIL       RejectDetail;
  WINBIO_IDENTITY            Identity;
  ULONGLONG                  TrackingId;
  WINBIO_PROTECTION_TICKET   Ticket;
  WINBIO_PRESENCE_PROPERTIES Properties;
} WINBIO_PRESENCE, *PWINBIO_PRESENCE;
```



## <a name="members"></a>Members

<dl> <dt>

**Fattore**
</dt> <dd>

Fattore biometrico utilizzato per monitorare la presenza del singolo utente.

</dd> <dt>

**Sottofattore**
</dt> <dd>

Qualificatore del sottodatore biometrico per il fattore biometrico utilizzato per monitorare la presenza del singolo utente.

</dd> <dt>

**Status**
</dt> <dd>

Stato della procedura di identificazione per il singolo utente.

</dd> <dt>

**RejectDetail**
</dt> <dd>

Informazioni aggiuntive sull'errore per riconoscere un individuo, incluso il feedback che spiega come correggere l'errore.

</dd> <dt>

**Identità**
</dt> <dd>

Identità dell'utente la cui presenza viene monitorata, una volta identificata la persona.

</dd> <dt>

**TrackingId**
</dt> <dd>

Intero generato dall'adapter e che identifica in modo univoco l'oggetto singolo. L'identificatore di rilevamento assegnato dall'adapter a un particolare utente è sempre costante finché tale utente rimane nel frame della fotocamera.

</dd> <dt>

**Ticket**
</dt> <dd>

Riservato. Impostare su 0 dalla scheda.

</dd> <dt>

**Proprietà**
</dt> <dd>

Informazioni specifiche del fattore sulla posizione di un singolo utente.

</dd> </dl>

## <a name="remarks"></a>Commenti

La funzione [**EngineAdapterIdentifyAll**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_identify_all_fn) crea una matrice di strutture di **\_ presenza WINBIO** e invia questa matrice al servizio biometrico. Il servizio biometrico usa la matrice per aggiornare il rispettivo modello interno di persone vicino al computer.

A seconda dei risultati di questo aggiornamento, il servizio biometrico può generare una struttura dei [**\_ \_ risultati asincrona WINBIO**](/windows/desktop/api/Winbio/ns-winbio-winbio_async_result) per la funzione [**WinBioMonitorPresence**](/windows/desktop/api/winbio/nf-winbio-winbiomonitorpresence) per tutti i client con monitoraggi presenza attiva. **\_ Risultato asincrono WINBIO \_ .** Il membro Operation della struttura contiene **la \_ \_ \_ presenza del monitoraggio dell'operazione WINBIO** e il **\_ risultato asincrono WINBIO \_ . Il membro Parameters. MonitorPresence. ChangeType** fornisce informazioni aggiuntive sullo stato del singolo utente.

Quando un utente associato a un particolare identificatore di rilevamento viene visualizzato nel flusso di input per la prima volta, il servizio biometrico genera una struttura dei [**\_ \_ risultati asincrona WINBIO**](/windows/desktop/api/Winbio/ns-winbio-winbio_async_result) sul lato client dove il **\_ risultato asincrono di WINBIO \_ . Parameters. MonitorPresence. ChangeType** è un membro del **\_ \_ tipo \_ di modifica WINBIO**. Questa struttura viene inviata alla funzione di callback dell'applicazione o alla coda di messaggi dell'applicazione prima di qualsiasi altra struttura di **\_ \_ risultato asincrono di WINBIO** in cui il **\_ risultato asincrono di WINBIO \_ . Parameters. MonitorPresence. PresenceArray** include una struttura di **\_ presenza WINBIO** con lo stesso valore per la **\_ presenza WINBIO. TrackingId**.

Le combinazioni di valori seguenti nella matrice di strutture **di \_ presenza WINBIO** che il **\_ risultato asincrono di WINBIO \_ . Il membro Parameters. MonitorPresence. PresenceArray** indica tipi specifici di modifiche nello stato di un singolo utente.

-   Quando un utente è visibile nel frame della fotocamera, ma il motore sta ancora tentando di identificare il singolo utente, i membri della struttura di **\_ presenza WINBIO** hanno i valori riportati nella tabella seguente.

    

    | Membro            | Valore                                                    |
    |-------------------|----------------------------------------------------------|
    | **TrackingId**    | Intero che identifica l'oggetto singolo al motore. |
    | **Status**        | **\_OK**                                                |
    | **Identity. Type** | **\_tipo di ID WINBIO \_ \_ null**                               |

    

     

    In questo caso, il servizio biometrico estende l'ora di scadenza per l'utente singolo e non genera una struttura dei [**\_ \_ risultati asincrona WINBIO**](/windows/desktop/api/Winbio/ns-winbio-winbio_async_result) sul lato client per l'identificatore di rilevamento in cui il **\_ risultato asincrono di WINBIO \_ . Parameters. MonitorPresence. ChangeType** membro è **WINBIO \_ tipo di modifica \_ \_ RECOGNIZE**.

    La prima volta che una struttura di [**\_ \_ risultati asincrona di WINBIO**](/windows/desktop/api/Winbio/ns-winbio-winbio_async_result) include la struttura di **\_ presenza WINBIO** in cui il membro di **stato** è **\_ OK** e il membro **Identity. Type** è **WINBIO \_ ID \_ Type \_ null** dopo che una o più strutture di **\_ \_ risultati asincrone WINBIO** includono una struttura di **\_ presenza WINBIO** con un membro di **stato** **WINBIO \_ E \_ Bad \_ Capture**, il monitoraggio della presenza genera una singola struttura di **\_ \_ risultati asincrono WINBIO** per l'identificatore di rilevamento in **\_ \_ Il membro Parameters. MonitorPresence. ChangeType** è **WINBIO \_ Change \_ Type \_ Track**. Questa struttura di **\_ \_ risultati asincrona di WINBIO** dove il **\_ risultato asincrono di WINBIO \_ . Parameters. MonitorPresence. ChangeType** membro is **WINBIO \_ Change \_ Type \_ Track** informa il client che il problema che ha causato l'errore **di \_ \_ \_ acquisizione WINBIO E Bad** è stato risolto. Per ulteriori informazioni sulle circostanze in cui una struttura di **\_ presenza WINBIO** dispone di un membro di **stato** **WINBIO \_ E \_ Bad \_ Capture**, vedere la descrizione del modo in cui l'adattatore del motore fornisce feedback all'utente per correggere gli errori di riconoscimento più avanti in queste osservazioni.

-   Quando un utente è visibile nel frame della fotocamera, ma il motore sta ancora tentando di identificare il singolo e desidera fornire un feedback all'utente su come correggere un errore di riconoscimento, i membri della struttura **di \_ presenza WINBIO** hanno i valori riportati nella tabella seguente.

    

    | Membro                                                                                                      | Valore                                                                         |
    |-------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
    | **TrackingId**                                                                                              | Intero che identifica l'oggetto singolo al motore.                      |
    | **Status**                                                                                                  | **WINBIO \_ E \_ acquisizione non valida \_**                                                   |
    | **Identity. Type**                                                                                           | **\_tipo di ID WINBIO \_ \_ null**                                                    |
    | **Properties. FacialFeatures. BoundingBox**, se il valore di **Factor** è **WINBIO \_ \_ \_ funzionalità facciali del tipo** | Posizione della faccia del singolo all'interno del frame della fotocamera.           |
    | **Properties. Iris. BoundingBox**, se il valore di **Factor** è **WINBIO di \_ tipo \_ Iris**                       | Posizione degli Iris o degli Iris del singolo oggetto all'interno del frame della fotocamera. |

    

     

    In questo caso, il servizio biometrico estende l'ora di scadenza per per l'utente singolo e genera una struttura di [**\_ \_ risultati asincrona WINBIO**](/windows/desktop/api/Winbio/ns-winbio-winbio_async_result) per l'identificatore di rilevamento in cui il **\_ risultato asincrono WINBIO \_ . Il membro Parameters. MonitorPresence. ChangeType** è **WINBIO \_ Change \_ Type \_ Track**.

-   Quando un utente è visibile nel frame della fotocamera e l'adattatore del motore determina l'identità del singolo utente, i membri della struttura **di \_ presenza WINBIO** hanno i valori riportati nella tabella seguente.

    

    | Membro                        | Valore                                                    |
    |-------------------------------|----------------------------------------------------------|
    | **TrackingId**                | Intero che identifica l'oggetto singolo al motore. |
    | **Status**                    | **\_OK**                                                |
    | **Identity. Type**             | **\_ \_ SID tipo ID \_ WINBIO**                                |
    | **Identity. Value. AccountSid** | ID di sicurezza (SID) dell'utente.         |

    

     

    In questo caso, il servizio biometrico associa l'identificatore di rilevamento al SID per l'utente singolo e genera una struttura [**di \_ \_ risultati asincrona WINBIO**](/windows/desktop/api/Winbio/ns-winbio-winbio_async_result) sul lato client per l'identificatore di rilevamento dove il **\_ risultato asincrono di WINBIO \_ . Parameters. MonitorPresence. ChangeType** membro è **WINBIO \_ tipo di modifica \_ \_ RECOGNIZE**. Il servizio biometrico non genera ulteriori strutture di **\_ \_ risultati asincrone WINBIO** sul lato client per l'identificatore di rilevamento, a meno che il singolo non lasci il frame della fotocamera.

-   Quando un utente è visibile nel frame della fotocamera, ma l'adattatore del motore determina che l'utente non è registrato, i membri della struttura di **\_ presenza WINBIO** hanno i valori riportati nella tabella seguente.

    

    | Membro            | Valore                                                    |
    |-------------------|----------------------------------------------------------|
    | **TrackingId**    | Intero che identifica l'oggetto singolo al motore. |
    | **Status**        | **\_ID WINBIO E \_ sconosciuto \_**                               |
    | **Identity. Type** | **\_tipo di ID WINBIO \_ \_ null**                               |

    

     

    In questo caso, il servizio biometrico associa l'identificatore di rilevamento del singolo oggetto con un'identità sconosciuta e genera una struttura dei [**\_ \_ risultati asincrona WINBIO**](/windows/desktop/api/Winbio/ns-winbio-winbio_async_result) sul lato client per l'identificatore di rilevamento in cui il **\_ risultato asincrono di WINBIO \_ . Parameters. MonitorPresence. ChangeType** membro è **WINBIO \_ tipo di modifica \_ \_ RECOGNIZE**. Il servizio biometrico non genera ulteriori strutture di **\_ \_ risultati asincrone WINBIO** sul lato client per l'identificatore di rilevamento, a meno che il singolo non lasci il frame della fotocamera.

Quando un utente associato a un determinato identificatore di rilevamento lascia il frame della fotocamera e si interrompe la visualizzazione dei valori restituiti dalla funzione [**EngineAdapterIdentifyAll**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_identify_all_fn) , l'identificatore di rilevamento scade. Quando l'identificatore di rilevamento scade, il servizio biometrico genera una struttura dei [**\_ \_ risultati asincrona WINBIO**](/windows/desktop/api/Winbio/ns-winbio-winbio_async_result) sul lato client dove il **\_ risultato asincrono di WINBIO \_ . Il membro Parameters. MonitorPresence. ChangeType** è **WINBIO \_ \_ tipo \_ di modifica**. L'adattatore del motore può impedire al servizio biometrico di generare questa struttura con il valore di **WINBIO del \_ \_ tipo \_ di modifica** , includendo una struttura di **\_ presenza WINBIO** nella matrice restituita da **EngineAdapterIdentifyAll** , in cui la **presenza del WINBIO \_ .** Il membro di stato è **\_ OK** e **la \_ presenza WINBIO. Identity. Type** member è **WINBIO \_ ID \_ Type \_ null** come descritto in precedenza in queste osservazioni. Questa azione estende l'ora di scadenza per l'identificatore di rilevamento senza causare alcuna attività lato client.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows 10\]<br/>                                                                                                                              |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2016\]<br/>                                                                                                                     |
| Intestazione<br/>                   | <dl> <dt>WinBio \_ types. h (includere WinBio. h per le applicazioni client o WinBio \_ Adapters. h per gli adapter)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_risultato asincrono \_ WINBIO**](/windows/desktop/api/Winbio/ns-winbio-winbio_async_result)
</dt> <dt>

[**WinBioMonitorPresence**](/windows/desktop/api/winbio/nf-winbio-winbiomonitorpresence)
</dt> <dt>

[**EngineAdapterIdentifyAll**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_identify_all_fn)
</dt> </dl>

 

 






---
title: WINBIO_PRESENCE struttura (Winbio \_ types.h)
description: Contiene informazioni sulla presenza di un utente la cui presenza viene monitorata.
ms.assetid: 810D452E-DDFA-4AB2-AEFB-0C170C0C18D4
keywords:
- WINBIO_PRESENCE struttura Windows'API Biometric Framework
- PWINBIO_PRESENCE puntatore alla struttura Windows'API Biometric Framework
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
ms.openlocfilehash: 2671faaee7bc277f9389d7c993e4d511dac03db459755b40bf3f659ff5256a56
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118909579"
---
# <a name="winbio_presence-structure"></a>Struttura WINBIO \_ PRESENCE

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

Fattore biometrico usato per monitorare la presenza dell'utente.

</dd> <dt>

**Sottofactoring**
</dt> <dd>

Qualificatore del sottofactor biometrico per il fattore biometrico usato per monitorare la presenza dell'utente.

</dd> <dt>

**Status**
</dt> <dd>

Stato della procedura di identificazione per l'utente.

</dd> <dt>

**RejectDetail**
</dt> <dd>

Informazioni aggiuntive sull'errore di riconoscimento di una persona, inclusi i commenti e suggerimenti che spiegano come correggere l'errore.

</dd> <dt>

**Identità**
</dt> <dd>

Identità dell'utente di cui viene monitorata la presenza, dopo che l'utente è stato identificato.

</dd> <dt>

**TrackingId**
</dt> <dd>

Intero generato dall'adapter e che identifica in modo univoco l'utente. L'identificatore di rilevamento assegnato dall'adattatore a una determinata persona è garantito come costante, purché tale persona rimanga nel fotogramma della fotocamera.

</dd> <dt>

**Ticket**
</dt> <dd>

Riservato. Impostare su 0 dall'adapter.

</dd> <dt>

**Proprietà**
</dt> <dd>

Informazioni specifiche del fattore sulla posizione di un singolo utente.

</dd> </dl>

## <a name="remarks"></a>Commenti

La [**funzione EngineAdapterIdentifyAll**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_identify_all_fn) crea una matrice di **strutture WINBIO \_ PRESENCE** e la invia al servizio biometrico. Il servizio biometrico usa la matrice per aggiornare il modello interno degli esseri umani vicino al computer.

A seconda dei risultati di questo aggiornamento, il servizio biometrico può generare una struttura [**\_ WINBIO ASYNC \_ RESULT**](/windows/desktop/api/Winbio/ns-winbio-winbio_async_result) per la funzione [**WinBioMonitorPresence**](/windows/desktop/api/winbio/nf-winbio-winbiomonitorpresence) per tutti i client con monitoraggi presenza attivi. RISULTATO **ASINCRONO WINBIO. \_ \_ Il** membro dell'operazione della struttura **contiene WINBIO \_ OPERATION MONITOR \_ \_ PRESENCE** e **WINBIO \_ ASYNC \_ RESULT. Il membro Parameters.MonitorPresence.ChangeType** fornisce informazioni aggiuntive sullo stato dell'utente.

Quando un utente associato dall'adattatore motore a un identificatore di rilevamento specifico viene visualizzato nel flusso di input per la prima volta, il servizio biometrico genera una struttura [**WINBIO \_ ASYNC \_ RESULT**](/windows/desktop/api/Winbio/ns-winbio-winbio_async_result) sul lato client in cui **WINBIO \_ ASYNC \_ RESULT. Il membro Parameters.MonitorPresence.ChangeType** è **WINBIO \_ CHANGE TYPE \_ \_ ARRIVAL.** Questa struttura viene inviata alla funzione di callback dell'applicazione o alla coda di messaggi dell'applicazione prima di qualsiasi altra struttura **\_ WINBIO ASYNC \_ RESULT** in cui **WINBIO \_ ASYNC \_ RESULT. Parameters.MonitorPresence.PresenceArray** include una **struttura WINBIO \_ PRESENCE** con lo stesso valore per **WINBIO \_ PRESENCE. TrackingId**.

Le combinazioni di valori seguenti nella matrice di **strutture WINBIO \_ PRESENCE** restituite da **WINBIO \_ ASYNC \_ RESULT. Il membro Parameters.MonitorPresence.PresenceArray** indica tipi specifici di modifiche nello stato di un singolo utente.

-   Quando una persona è visibile nel frame della fotocamera, ma il motore sta ancora tentando di identificare la persona, i membri della struttura **WINBIO \_ PRESENCE** hanno i valori nella tabella seguente.

    

    | Membro            | Valore                                                    |
    |-------------------|----------------------------------------------------------|
    | **TrackingId**    | Intero che identifica l'utente al motore. |
    | **Status**        | **S \_ OK**                                                |
    | **Identity.Type** | **TIPO DI ID WINBIO \_ \_ \_ NULL**                               |

    

     

    In questo caso, il servizio biometrico estende il tempo di scadenza per l'utente e non genera una struttura [**WINBIO \_ ASYNC \_ RESULT**](/windows/desktop/api/Winbio/ns-winbio-winbio_async_result) sul lato client per l'identificatore di rilevamento in cui **WINBIO \_ ASYNC \_ RESULT. Il membro Parameters.MonitorPresence.ChangeType** è **WINBIO \_ CHANGE TYPE \_ \_ RECOGNIZE**.

    La prima volta che  una struttura [**WINBIO \_ ASYNC \_ RESULT**](/windows/desktop/api/Winbio/ns-winbio-winbio_async_result) include la struttura **WINBIO \_ PRESENCE** in cui il membro Status è S **\_ OK** e il membro **Identity.Type** è **WINBIO \_ ID TYPE \_ \_ NULL** dopo che una o più strutture **WINBIO \_ ASYNC \_ RESULT** includevano una struttura **WINBIO \_ PRESENCE** con un membro Status di **WINBIO \_ E BAD \_ \_ CAPTURE,** il monitoraggio della presenza genera una singola struttura **WINBIO \_ ASYNC \_ RESULT** per l'identificatore di rilevamento in cui  **WINBIO \_ ASYNC \_ RESULT. Il membro Parameters.MonitorPresence.ChangeType** è **WINBIO \_ CHANGE TYPE \_ \_ TRACK**. Struttura **WINBIO \_ ASYNC \_ RESULT** in cui viene restituito IL RISULTATO **\_ ASINCRONO WINBIO. \_ Il membro Parameters.MonitorPresence.ChangeType** è **WINBIO \_ CHANGE TYPE \_ \_ TRACK** informa il client che il problema che ha causato l'errore **WINBIO \_ E BAD \_ \_ CAPTURE** è stato risolto. Per altre informazioni sulle circostanze in cui una struttura **WINBIO \_ PRESENCE** ha il membro **Status** di **WINBIO \_ E BAD \_ \_ CAPTURE,** vedere la descrizione del modo in cui l'adattatore motore fornisce feedback all'utente per correggere gli errori di riconoscimento più avanti in queste osservazioni.

-   Quando una persona è visibile nel frame della fotocamera, ma il motore sta ancora tentando di identificare l'utente e vuole fornire un feedback all'utente su come correggere un errore di riconoscimento, i membri della struttura **WINBIO \_ PRESENCE** hanno i valori nella tabella seguente.

    

    | Membro                                                                                                      | Valore                                                                         |
    |-------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
    | **TrackingId**                                                                                              | Intero che identifica l'utente al motore.                      |
    | **Status**                                                                                                  | **WINBIO \_ E \_ BAD \_ CAPTURE**                                                   |
    | **Identity.Type**                                                                                           | **TIPO DI ID WINBIO \_ \_ \_ NULL**                                                    |
    | **Properties.FacialFeatures.BoundingBox**, se il valore di **Factor** è **WINBIO \_ TYPE FACIAL \_ \_ FEATURES** | Posizione del viso dell'utente all'interno della cornice della fotocamera.           |
    | **Properties.Iris.BoundingBox,** se il valore di **Factor** è **WINBIO \_ TYPE \_ IRIS**                       | Posizione dell'iris o dell'iris dell'utente all'interno della cornice della fotocamera. |

    

     

    In questo caso, il servizio biometrico estende il tempo di scadenza per l'utente singolo e genera una struttura [**\_ WINBIO ASYNC \_ RESULT**](/windows/desktop/api/Winbio/ns-winbio-winbio_async_result) per l'identificatore di rilevamento in cui **WINBIO \_ ASYNC \_ RESULT. Il membro Parameters.MonitorPresence.ChangeType** è **WINBIO \_ CHANGE TYPE \_ \_ TRACK**.

-   Quando una persona è visibile nel frame della fotocamera e l'adattatore motore determina l'identità della persona, i membri della struttura **WINBIO \_ PRESENCE** hanno i valori nella tabella seguente.

    

    | Membro                        | Valore                                                    |
    |-------------------------------|----------------------------------------------------------|
    | **TrackingId**                | Intero che identifica l'utente al motore. |
    | **Status**                    | **S \_ OK**                                                |
    | **Identity.Type**             | **SID DEL TIPO DI ID WINBIO \_ \_ \_**                                |
    | **Identity.Value.AccountSid** | Identificatore di sicurezza (SID) dell'utente.         |

    

     

    In questo caso, il servizio biometrico associa l'identificatore di rilevamento al SID per l'utente singolo e genera una struttura [**WINBIO \_ ASYNC \_ RESULT**](/windows/desktop/api/Winbio/ns-winbio-winbio_async_result) sul lato client per l'identificatore di rilevamento in cui **WINBIO \_ ASYNC \_ RESULT. Il membro Parameters.MonitorPresence.ChangeType** è **WINBIO \_ CHANGE TYPE \_ \_ RECOGNIZE**. Il servizio biometrico non genera strutture **WINBIO \_ ASYNC \_ RESULT aggiuntive** sul lato client per l'identificatore di rilevamento, a meno che la persona non lasci il fotogramma della fotocamera.

-   Quando una persona è visibile nel frame della fotocamera, ma l'adattatore del motore determina per certo che l'utente non è registrato, i membri della struttura **WINBIO \_ PRESENCE** hanno i valori nella tabella seguente.

    

    | Membro            | Valore                                                    |
    |-------------------|----------------------------------------------------------|
    | **TrackingId**    | Intero che identifica l'utente al motore. |
    | **Status**        | **ID WINBIO \_ E \_ SCONOSCIUTO \_**                               |
    | **Identity.Type** | **TIPO DI ID WINBIO \_ \_ \_ NULL**                               |

    

     

    In questo caso, il servizio biometrico associa l'identificatore di rilevamento della persona a un'identità UNKNOWN e genera una struttura [**WINBIO \_ ASYNC \_ RESULT**](/windows/desktop/api/Winbio/ns-winbio-winbio_async_result) sul lato client per l'identificatore di rilevamento in cui **WINBIO \_ ASYNC \_ RESULT. Il membro Parameters.MonitorPresence.ChangeType** è **WINBIO \_ CHANGE TYPE \_ \_ RECOGNIZE**. Il servizio biometrico non genera strutture **WINBIO \_ ASYNC \_ RESULT aggiuntive** sul lato client per l'identificatore di rilevamento, a meno che la persona non lasci il fotogramma della fotocamera.

Quando un utente associato dall'adattatore motore a un identificatore di rilevamento specifico lascia il fotogramma della fotocamera e smette di comparire nei valori restituiti dalla funzione [**EngineAdapterIdentifyAll,**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_identify_all_fn) l'identificatore di rilevamento scade. Quando l'identificatore di rilevamento scade, il servizio biometrico genera una struttura [**WINBIO \_ ASYNC \_ RESULT**](/windows/desktop/api/Winbio/ns-winbio-winbio_async_result) sul lato client in cui **WINBIO \_ ASYNC \_ RESULT. Il membro Parameters.MonitorPresence.ChangeType** è **WINBIO \_ CHANGE TYPE \_ \_ DEPART.** L'adattatore del motore può impedire al servizio biometrico di generare questa struttura con il valore **WINBIO \_ CHANGE \_ TYPE \_ DEPART** includendo una struttura **WINBIO \_ PRESENCE** nella matrice restituita da **EngineAdapterIdentifyAll,** dove **WINBIO \_ PRESENCE. Il** membro di stato **è S \_ OK** e **WINBIO \_ PRESENCE. Il membro Identity.Type** è **WINBIO \_ ID TYPE \_ \_ NULL,** come descritto in precedenza in queste osservazioni. Questa azione estende il tempo di scadenza per l'identificatore di rilevamento senza causare alcuna attività sul lato client.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 10 solo app desktop\]<br/>                                                                                                                              |
| Server minimo supportato<br/> | \[Windows Server 2016 solo app desktop\]<br/>                                                                                                                     |
| Intestazione<br/>                   | <dl> <dt>Winbio \_ types.h (includere Winbio.h per le applicazioni client o Adapters.h Winbio \_ per gli adapter)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**RISULTATO ASINCRONO WINBIO \_ \_**](/windows/desktop/api/Winbio/ns-winbio-winbio_async_result)
</dt> <dt>

[**WinBioMonitorPresence**](/windows/desktop/api/winbio/nf-winbio-winbiomonitorpresence)
</dt> <dt>

[**EngineAdapterIdentifyAll**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_identify_all_fn)
</dt> </dl>

 

 






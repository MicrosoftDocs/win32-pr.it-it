---
title: Controllo Up-Down
description: Questa sezione contiene informazioni sugli elementi di programmazione usati con i controlli di scorrimento.
ms.assetid: 48c6b4bd-65b4-4388-959e-efffa7658274
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8364eb44ee01e27439c82d1d77e674bfb9e3165
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044551"
---
# <a name="up-down-control"></a>Controllo Up-Down

Questa sezione contiene informazioni sugli elementi di programmazione usati con i controlli di scorrimento.

### <a name="overviews"></a>Cenni preliminari



| Argomento                                    | Contenuto                                                                                                                                                                                                            |
|------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Controlli di scorrimento](up-down-controls.md) | Un controllo di scorrimento è una coppia di pulsanti freccia su cui l'utente può fare clic per incrementare o decrementare un valore, ad esempio una posizione di scorrimento o un numero visualizzato in un controllo complementare (chiamato finestra di Buddy).<br/> |



 

### <a name="functions"></a>Funzioni



| Argomento                                              | Contenuto                                                                                                                                                |
|----------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CreateUpDownControl**](/windows/desktop/api/Commctrl/nf-commctrl-createupdowncontrol) | Crea un controllo di scorrimento. Nota: questa funzione è obsoleta. Si tratta di una funzione a 16 bit e non è in grado di gestire valori di bit 32 per l'intervallo e la posizione.<br/> |



 

### <a name="messages"></a>Messaggi



| Argomento                                                 | Contenuto                                                                                                                                                                                                                               |
|-------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_GETACCEL UDM**](udm-getaccel.md)                 | Recupera le informazioni di accelerazione per un controllo di scorrimento. <br/>                                                                                                                                                                 |
| [**UDM \_ GETbase**](udm-getbase.md)                   | Recupera la base radice corrente, ovvero in base 10 o 16, per un controllo di scorrimento. <br/>                                                                                                                                   |
| [**UDM \_ GETbuddy**](udm-getbuddy.md)                 | Recupera l'handle per la finestra Buddy corrente. <br/>                                                                                                                                                                          |
| [**\_GETPOS UDM**](udm-getpos.md)                     | Recupera la posizione corrente di un controllo di scorrimento con precisione a 16 bit. <br/>                                                                                                                                                |
| [**\_GETPOS32 UDM**](udm-getpos32.md)                 | Restituisce la posizione a 32 bit di un controllo di scorrimento.<br/>                                                                                                                                                                          |
| [**UDM \_ GETrange**](udm-getrange.md)                 | Recupera le posizioni minime e massime (intervallo) per un controllo di scorrimento. <br/>                                                                                                                                                |
| [**\_GETRANGE32 UDM**](udm-getrange32.md)             | Recupera l'intervallo di 32 bit di un controllo di scorrimento. <br/>                                                                                                                                                                          |
| [**\_GETUNICODEFORMAT UDM**](udm-getunicodeformat.md) | Recupera il flag del formato carattere Unicode per il controllo. <br/>                                                                                                                                                               |
| [**\_SETACCEL UDM**](udm-setaccel.md)                 | Imposta l'accelerazione per un controllo di scorrimento. <br/>                                                                                                                                                                              |
| [**UDM di \_ base**](udm-setbase.md)                   | Imposta la base radice per un controllo di scorrimento. Il valore di base determina se la finestra Buddy Visualizza numeri in cifre decimali o esadecimali. I numeri esadecimali sono sempre senza segno e i numeri decimali sono firmati. <br/> |
| [**UDM \_ SEbuddy**](udm-setbuddy.md)                 | Imposta la finestra buddy per un controllo di scorrimento. <br/>                                                                                                                                                                              |
| [**\_SETPOS UDM**](udm-setpos.md)                     | Imposta la posizione corrente per un controllo di scorrimento con precisione a 16 bit. <br/>                                                                                                                                                    |
| [**\_SETPOS32 UDM**](udm-setpos32.md)                 | Imposta la posizione di un controllo di scorrimento con precisione a 32 bit.<br/>                                                                                                                                                              |
| [**\_SEtrange UDM**](udm-setrange.md)                 | Imposta le posizioni minime e massime (intervallo) per un controllo di scorrimento.<br/>                                                                                                                                                      |
| [**\_SETRANGE32 UDM**](udm-setrange32.md)             | Imposta l'intervallo di 32 bit di un controllo di scorrimento. <br/>                                                                                                                                                                               |
| [**\_SETUNICODEFORMAT UDM**](udm-setunicodeformat.md) | Imposta il flag di formato carattere Unicode per il controllo. Questo messaggio consente di modificare il set di caratteri utilizzato dal controllo in fase di esecuzione anziché dover ricreare il controllo. <br/>                                   |



 

### <a name="notifications"></a>Notifiche



| Argomento                                                            | Contenuto                                                                                                                                                                                                                                                                                                                                                       |
|------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [NM \_ RELEASEDCAPTURE (Down)](nm-releasedcapture-up-down-.md) | Notifica alla finestra padre di un controllo di scorrimento che il controllo sta rilasciando l'acquisizione del mouse. Questa notifica viene inviata sotto forma di messaggio di [**\_ notifica WM**](wm-notify.md) . <br/>                                                                                                                                                                       |
| [\_DELTAPOS UDN](udn-deltapos.md)                                | Inviato dal sistema operativo alla finestra padre di un controllo di scorrimento quando la posizione del controllo sta per essere modificata. Questo errore si verifica quando l'utente richiede una modifica nel valore premendo la freccia su o giù del controllo. Il messaggio [UDN \_ DELTAPOS](udn-deltapos.md) viene inviato sotto forma di messaggio di [**\_ notifica WM**](wm-notify.md) . <br/> |



 

### <a name="structures"></a>Strutture



| Argomento                        | Contenuto                                                                                                                                          |
|------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| [**NMUPDOWN**](/windows/win32/api/commctrl/ns-commctrl-nmupdown) | Contiene informazioni specifiche per i messaggi di notifica del controllo di scorrimento. È identica a e sostituisce la struttura **a \_ discesa Nm** . <br/> |
| [**UDACCEL**](/windows/desktop/api/Commctrl/ns-commctrl-udaccel)   | Contiene informazioni sull'accelerazione per un controllo di scorrimento. <br/>                                                                             |



 

### <a name="constants"></a>Costanti



| Argomento                                                | Contenuto                                                                      |
|------------------------------------------------------|-------------------------------------------------------------------------------|
| [Stili di controllo di scorrimento](up-down-control-styles.md) | Questa sezione elenca gli stili usati per la creazione di controlli di scorrimento.<br/> |



 

 

 






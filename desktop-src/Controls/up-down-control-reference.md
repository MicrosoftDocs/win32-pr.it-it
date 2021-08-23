---
title: Up-Down controllo
description: Questa sezione contiene informazioni sugli elementi di programmazione usati con i controlli up-down.
ms.assetid: 48c6b4bd-65b4-4388-959e-efffa7658274
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2979ac08889761cb7f226b58a9d951d407bc82420957ed9327de1a880d0d9bb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119018589"
---
# <a name="up-down-control"></a>Up-Down controllo

Questa sezione contiene informazioni sugli elementi di programmazione usati con i controlli up-down.

### <a name="overviews"></a>Cenni preliminari



| Argomento                                    | Contenuto                                                                                                                                                                                                            |
|------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Controlli up-down](up-down-controls.md) | Un controllo verso l'alto è una coppia di pulsanti freccia su cui l'utente può fare clic per incrementare o decrementare un valore, ad esempio una posizione di scorrimento o un numero visualizzato in un controllo complementare (chiamato finestra di controllo amico).<br/> |



 

### <a name="functions"></a>Funzioni



| Argomento                                              | Contenuto                                                                                                                                                |
|----------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CreateUpDownControl**](/windows/desktop/api/Commctrl/nf-commctrl-createupdowncontrol) | Crea un controllo up-down. Nota: questa funzione è obsoleta. Si tratta di una funzione a 16 bit e non può gestire valori a 32 bit per intervallo e posizione.<br/> |



 

### <a name="messages"></a>Messaggi



| Argomento                                                 | Contenuto                                                                                                                                                                                                                               |
|-------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UDM \_ GETACCEL**](udm-getaccel.md)                 | Recupera le informazioni sull'accelerazione per un controllo up-down. <br/>                                                                                                                                                                 |
| [**UDM \_ GETBASE**](udm-getbase.md)                   | Recupera la base della radice corrente, ovvero in base 10 o 16, per un controllo verso l'alto. <br/>                                                                                                                                   |
| [**UDM \_ GETBUDDY**](udm-getbuddy.md)                 | Recupera l'handle per la finestra corrente. <br/>                                                                                                                                                                          |
| [**UDM \_ GETPOS**](udm-getpos.md)                     | Recupera la posizione corrente di un controllo verso l'alto con precisione a 16 bit. <br/>                                                                                                                                                |
| [**UDM \_ GETPOS32**](udm-getpos32.md)                 | Restituisce la posizione a 32 bit di un controllo verso l'alto.<br/>                                                                                                                                                                          |
| [**UDM \_ GETRANGE**](udm-getrange.md)                 | Recupera le posizioni minima e massima (intervallo) per un controllo up-down. <br/>                                                                                                                                                |
| [**UDM \_ GETRANGE32**](udm-getrange32.md)             | Recupera l'intervallo a 32 bit di un controllo up-down. <br/>                                                                                                                                                                          |
| [**UDM \_ GETUNICODEFORMAT**](udm-getunicodeformat.md) | Recupera il flag di formato carattere Unicode per il controllo. <br/>                                                                                                                                                               |
| [**UDM \_ SETACCEL**](udm-setaccel.md)                 | Imposta l'accelerazione per un controllo verso l'alto. <br/>                                                                                                                                                                              |
| [**UDM \_ SETBASE**](udm-setbase.md)                   | Imposta la base della radice per un controllo verso l'alto. Il valore di base determina se nella finestra degli amici vengono visualizzati numeri in cifre decimali o esadecimali. I numeri esadecimali sono sempre senza segno e i numeri decimali sono con segno. <br/> |
| [**UDM \_ SETBUDDY**](udm-setbuddy.md)                 | Imposta la finestra degli amici per un controllo verso l'alto. <br/>                                                                                                                                                                              |
| [**UDM \_ SETPOS**](udm-setpos.md)                     | Imposta la posizione corrente per un controllo verso l'alto con precisione a 16 bit. <br/>                                                                                                                                                    |
| [**UDM \_ SETPOS32**](udm-setpos32.md)                 | Imposta la posizione di un controllo verso l'alto con precisione a 32 bit.<br/>                                                                                                                                                              |
| [**UDM \_ SETRANGE**](udm-setrange.md)                 | Imposta le posizioni minima e massima (intervallo) per un controllo up-down.<br/>                                                                                                                                                      |
| [**UDM \_ SETRANGE32**](udm-setrange32.md)             | Imposta l'intervallo a 32 bit di un controllo up-down. <br/>                                                                                                                                                                               |
| [**UDM \_ SETUNICODEFORMAT**](udm-setunicodeformat.md) | Imposta il flag di formato carattere Unicode per il controllo. Questo messaggio consente di modificare il set di caratteri utilizzato dal controllo in fase di esecuzione anziché dover creare nuovamente il controllo. <br/>                                   |



 

### <a name="notifications"></a>Notifiche



| Argomento                                                            | Contenuto                                                                                                                                                                                                                                                                                                                                                       |
|------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [NM \_ RELEASEDCAPTURE (up-down)](nm-releasedcapture-up-down-.md) | Notifica alla finestra padre di un controllo verso l'alto che il controllo sta rilasciando mouse capture. Questa notifica viene inviata sotto forma di [**messaggio WM \_ NOTIFY.**](wm-notify.md) <br/>                                                                                                                                                                       |
| [UDN \_ DELTAPOS](udn-deltapos.md)                                | Inviato dal sistema operativo alla finestra padre di un controllo up-down quando la posizione del controllo sta per cambiare. Ciò si verifica quando l'utente richiede una modifica del valore premendo la freccia su o giù del controllo. Il [messaggio UDN \_ DELTAPOS](udn-deltapos.md) viene inviato sotto forma di [**messaggio WM \_ NOTIFY.**](wm-notify.md) <br/> |



 

### <a name="structures"></a>Strutture



| Argomento                        | Contenuto                                                                                                                                          |
|------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| [**NMUPDOWN**](/windows/win32/api/commctrl/ns-commctrl-nmupdown) | Contiene informazioni specifiche per i messaggi di notifica del controllo up-down. È identico a e sostituisce la **struttura NM \_ UPDOWN.** <br/> |
| [**UDACCEL**](/windows/desktop/api/Commctrl/ns-commctrl-udaccel)   | Contiene informazioni sull'accelerazione per un controllo up-down. <br/>                                                                             |



 

### <a name="constants"></a>Costanti



| Argomento                                                | Contenuto                                                                      |
|------------------------------------------------------|-------------------------------------------------------------------------------|
| [Stili dei controlli up-down](up-down-control-styles.md) | Questa sezione elenca gli stili usati durante la creazione di controlli up-down.<br/> |



 

 

 






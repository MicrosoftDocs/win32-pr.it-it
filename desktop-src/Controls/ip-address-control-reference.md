---
title: Controllo indirizzo IP
description: Questa sezione contiene informazioni sugli elementi di programmazione usati con i controlli degli indirizzi IP.
ms.assetid: vs|controls|~\controls\ipaddress\reflist.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c80fc87a12ce49038f4c1836e684fa0f8895bd0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104471070"
---
# <a name="ip-address-control"></a>Controllo indirizzo IP

Questa sezione contiene informazioni sugli elementi di programmazione usati con i controlli degli indirizzi IP.

### <a name="overviews"></a>Cenni preliminari



| Argomento                                          | Contenuto                                                                                                                    |
|------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| [Controlli degli indirizzi IP](ip-address-controls.md) | Un controllo degli indirizzi IP (Internet Protocol) consente all'utente di immettere un indirizzo IP in un formato facilmente comprensibile.<br/> |



 

### <a name="macros"></a>Macro



| Argomento                                         | Contenuto                                                                                                                              |
|-----------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [**PRIMA \_ IPAddress**](/windows/desktop/api/Commctrl/nf-commctrl-first_ipaddress)   | Estrae il valore del campo 0 da un indirizzo IP compresso recuperato con il messaggio [**IPM \_ GetAddress**](ipm-getaddress.md) . <br/> |
| [**QUARTO \_ indirizzo IP**](/windows/desktop/api/Commctrl/nf-commctrl-fourth_ipaddress) | Estrae il valore del campo 3 da un indirizzo IP compresso recuperato con il messaggio [**IPM \_ GetAddress**](ipm-getaddress.md) . <br/> |
| [**MAKEIPADDRESS**](/windows/desktop/api/Commctrl/nf-commctrl-makeipaddress)        | Comprime quattro valori di byte in un singolo LPARAM adatto per l'utilizzo con il messaggio di [**\_ Indirizzo IPM**](ipm-setaddress.md) . <br/>  |
| [**MAKEIPRANGE**](/windows/desktop/api/Commctrl/nf-commctrl-makeiprange)            | Comprime due valori di byte in un singolo LPARAM adatto per l'uso con il messaggio di [**\_ SetRange IPM**](ipm-setrange.md) . <br/>       |
| [**SECONDO \_ indirizzo IP**](/windows/desktop/api/Commctrl/nf-commctrl-second_ipaddress) | Estrae il valore del campo 1 da un indirizzo IP compresso recuperato con il messaggio [**IPM \_ GetAddress**](ipm-getaddress.md) . <br/> |
| [**TERZO \_ indirizzo IP**](/windows/desktop/api/Commctrl/nf-commctrl-third_ipaddress)   | Estrae il valore del campo 2 da un indirizzo IP compresso recuperato con il messaggio [**IPM \_ GetAddress**](ipm-getaddress.md) . <br/> |



 

### <a name="messages"></a>Messaggi



| Argomento                                         | Contenuto                                                                                                                              |
|-----------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [**\_CLEARADDRESS IPM**](ipm-clearaddress.md) | Cancella il contenuto del controllo degli indirizzi IP. <br/>                                                                            |
| [**IPM \_ GETaddress**](ipm-getaddress.md)     | Ottiene i valori di indirizzo per tutti e quattro i campi nel controllo degli indirizzi IP. <br/>                                                    |
| [**IPM \_ vuoto**](ipm-isblank.md)           | Determina se tutti i campi nel controllo indirizzo IP sono vuoti. <br/>                                                             |
| [**\_Indirizzo IPM**](ipm-setaddress.md)     | Imposta i valori di indirizzo per tutti e quattro i campi nel controllo degli indirizzi IP. <br/>                                                    |
| [**\_SetFocus**](ipm-setfocus.md)         | Imposta lo stato attivo della tastiera sul campo specificato nel controllo degli indirizzi IP. Tutto il testo in tale campo verrà selezionato. <br/> |
| [**\_SEtrange IPM**](ipm-setrange.md)         | Imposta l'intervallo valido per il campo specificato nel controllo degli indirizzi IP. <br/>                                                   |



 

### <a name="notifications"></a>Notifiche



| Argomento                                     | Contenuto                                                                                                                                                                                   |
|-------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [IPN \_ FIELDCHANGED](ipn-fieldchanged.md) | Inviato quando l'utente modifica un campo nel controllo o lo sposta da un campo all'altro. Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) . <br/> |



 

### <a name="structures"></a>Strutture



| Argomento                              | Contenuto                                                                                              |
|------------------------------------|-------------------------------------------------------------------------------------------------------|
| [**NMIPADDRESS**](/windows/win32/api/commctrl/ns-commctrl-nmipaddress) | Contiene informazioni per il codice di notifica di [IPN \_ FIELDCHANGED](ipn-fieldchanged.md) . <br/> |



 

 

 






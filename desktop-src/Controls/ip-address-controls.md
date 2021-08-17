---
title: Informazioni sui controlli degli indirizzi IP
description: Un controllo degli indirizzi IP (Internet Protocol) consente all'utente di immettere un indirizzo IP in un formato facilmente comprensibile.
ms.assetid: cf6a59fc-661c-420a-a67f-a42619946357
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce537b3b3a92846961e95321889d106a61a81e14bfa4cbc4edd93da5c8c033ae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119435596"
---
# <a name="about-ip-address-controls"></a>Informazioni sui controlli degli indirizzi IP

Un controllo degli indirizzi IP (Internet Protocol) consente all'utente di immettere un indirizzo IP in un formato facilmente comprensibile. Questo controllo consente inoltre all'applicazione di ottenere l'indirizzo in formato numerico anziché in formato testo.

-   [Informazioni sui controlli degli indirizzi IP](#about-ip-address-controls)
-   [Creazione di un controllo degli indirizzi IP](#creating-an-ip-address-control)
-   [Un controllo indirizzo IP è un controllo di modifica?](#is-an-ip-address-control-an-edit-control)

## <a name="about-ip-address-controls"></a>Informazioni sui controlli degli indirizzi IP

Windows Internet Explorer versione 4.0 introduce il controllo degli indirizzi IP, un nuovo controllo simile a un controllo di modifica che consente all'utente di immettere un indirizzo numerico in formato IP (Internet Protocol). Questo formato è costituito da quattro campi a tre cifre. Ogni campo viene trattato singolarmente. i numeri di campo sono in base zero e procedono da sinistra a destra, come illustrato in questa figura.

![diagramma che mostra i valori in ognuno dei quattro campi di un controllo degli indirizzi IP](images/ipa-scrn.png)

Il controllo consente di immettere solo testo numerico in ognuno dei campi. Dopo aver immesso tre cifre in un determinato campo, lo stato attivo della tastiera viene automaticamente spostato nel campo successivo. Se l'applicazione non deve compilare l'intero campo, l'utente può immettere meno di tre cifre. Ad esempio, se il campo deve contenere solo il numero 21, digitando "21" e premendo il tasto l'utente verrà visualizzato il campo successivo.

L'intervallo predefinito per ogni campo è compreso tra 0 e 255, ma l'applicazione può impostare l'intervallo su qualsiasi valore compreso tra questi limiti con il [**messaggio \_ IPM SETRANGE.**](ipm-setrange.md)

> [!Note]  
> Il controllo degli indirizzi IP viene implementato nella versione 4.71 e successive di Comctl32.dll.

 

## <a name="creating-an-ip-address-control"></a>Creazione di un controllo degli indirizzi IP

Prima di creare un controllo indirizzo IP, chiamare [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) con il flag **ICC \_ INTERNET \_ CLASSES** impostato nel membro **dwICC** della [**struttura INITCOMMONCONTROLSEX.**](/windows/win32/api/commctrl/ns-commctrl-initcommoncontrolsex)

Usare la [**funzione CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) o [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) per creare un controllo indirizzo IP. Il nome della classe per il controllo [**è WC \_ IPADDRESS,**](common-control-window-classes.md)definito in Commctrl.h. Non esistono stili specifici del controllo degli indirizzi IP. Tuttavia, poiché si tratta di un controllo figlio, usare lo [**stile \_ WS CHILD**](/windows/desktop/winmsg/window-styles) come minimo.

## <a name="is-an-ip-address-control-an-edit-control"></a>Un controllo indirizzo IP è un controllo di modifica?

Un controllo indirizzo IP non è un controllo di modifica e non risponde ai messaggi \_ EM. Tuttavia, invierà alla finestra del proprietario le notifiche di controllo di modifica seguenti tramite il [**messaggio WM \_ COMMAND.**](/windows/desktop/menurc/wm-command) Si noti che il controllo dell'indirizzo IP invierà anche notifiche IPN \_ private tramite il messaggio WM [**\_ NOTIFY.**](wm-notify.md)



|     Notifica                              |     Motivo della notifica                                                                                                                                                                                                    |
|-----------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [EN \_ SETFOCUS](en-setfocus.md)   | Inviato quando il controllo dell'indirizzo IP ottiene lo stato attivo della tastiera.                                                                                                                                              |
| [EN \_ KILLFOCUS](en-killfocus.md) | Inviato quando il controllo dell'indirizzo IP perde lo stato attivo della tastiera.                                                                                                                                              |
| [EN \_ CHANGE](en-change.md)       | Inviato quando viene modificato un campo nel controllo dell'indirizzo IP. Analogamente alla [notifica EN \_ CHANGE](en-change.md) da un controllo di modifica standard, questa notifica viene ricevuta dopo l'aggiornamento della schermata. |



 

 

 
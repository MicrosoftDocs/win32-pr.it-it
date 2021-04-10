---
title: Informazioni sui controlli degli indirizzi IP
description: Un controllo degli indirizzi IP (Internet Protocol) consente all'utente di immettere un indirizzo IP in un formato facilmente comprensibile.
ms.assetid: cf6a59fc-661c-420a-a67f-a42619946357
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb8cf39400c97d211d83b5496067fe6d4772e1e7
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "103963488"
---
# <a name="about-ip-address-controls"></a>Informazioni sui controlli degli indirizzi IP

Un controllo degli indirizzi IP (Internet Protocol) consente all'utente di immettere un indirizzo IP in un formato facilmente comprensibile. Questo controllo consente inoltre all'applicazione di ottenere l'indirizzo in formato numerico invece che in formato testo.

-   [Informazioni sui controlli degli indirizzi IP](#about-ip-address-controls)
-   [Creazione di un controllo degli indirizzi IP](#creating-an-ip-address-control)
-   [Un controllo degli indirizzi IP è un controllo di modifica?](#is-an-ip-address-control-an-edit-control)

## <a name="about-ip-address-controls"></a>Informazioni sui controlli degli indirizzi IP

Windows Internet Explorer versione 4,0 introduce il controllo degli indirizzi IP, un nuovo controllo simile a un controllo di modifica che consente all'utente di immettere un indirizzo numerico nel formato IP (Internet Protocol). Questo formato è costituito da campi a 4 3 cifre. Ogni campo viene considerato singolarmente; i numeri dei campi sono in base zero e procedono da sinistra a destra, come illustrato nella figura.

![diagramma che mostra i valori in ognuno dei quattro campi di un controllo degli indirizzi IP](images/ipa-scrn.png)

Il controllo consente di immettere solo testo numerico in ognuno dei campi. Una volta immesse tre cifre in un determinato campo, lo stato attivo viene spostato automaticamente sul campo successivo. Se il riempimento dell'intero campo non è necessario per l'applicazione, l'utente può immettere meno di tre cifre. Se, ad esempio, il campo deve contenere solo il numero ventuno, digitando "21" e premendo il tasto l'utente verrà portato al campo successivo.

L'intervallo predefinito per ogni campo è da 0 a 255, ma l'applicazione può impostare l'intervallo su qualsiasi valore compreso tra i limiti con il messaggio di [**\_ SetRange IPM**](ipm-setrange.md) .

> [!Note]  
> Il controllo degli indirizzi IP viene implementato nella versione 4,71 e successive di Comctl32.dll.

 

## <a name="creating-an-ip-address-control"></a>Creazione di un controllo degli indirizzi IP

Prima di creare un controllo degli indirizzi IP, chiamare [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) con il flag **ICC \_ Internet \_ classs** impostato nel membro **dwICC** della struttura [**InitCommonControlsEx**](/windows/win32/api/commctrl/ns-commctrl-initcommoncontrolsex) .

Usare la funzione [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) o [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) per creare un controllo degli indirizzi IP. Il nome della classe per il controllo è il [**WC \_ IPAddress**](common-control-window-classes.md), definito in commctrl. h. Non esistono stili specifici per il controllo degli indirizzi IP. Tuttavia, poiché si tratta di un controllo figlio, utilizzare come minimo lo stile [**WS \_ figlio**](/windows/desktop/winmsg/window-styles) .

## <a name="is-an-ip-address-control-an-edit-control"></a>Un controllo degli indirizzi IP è un controllo di modifica?

Un controllo degli indirizzi IP non è un controllo di modifica e non risponderà ai \_ messaggi em. Tuttavia, invierà alla finestra proprietaria le notifiche di controllo di modifica seguenti tramite il messaggio di [**\_ comando WM**](/windows/desktop/menurc/wm-command) . Si noti che il controllo degli indirizzi IP invierà notifiche IPN private anche \_ tramite il messaggio di [**\_ notifica WM**](wm-notify.md) .



|                                   |                                                                                                                                                                                                         |
|-----------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Notifica**                  | **Motivo della notifica**                                                                                                                                                                             |
| [IT \_ SetFocus](en-setfocus.md)   | Inviato quando il controllo dell'indirizzo IP ottiene lo stato attivo della tastiera.                                                                                                                                              |
| [EN \_ KILLFOCUS](en-killfocus.md) | Inviato quando il controllo dell'indirizzo IP perde lo stato attivo della tastiera.                                                                                                                                              |
| [\_modifica en](en-change.md)       | Inviato quando viene modificato un campo nel controllo degli indirizzi IP. Analogamente alla notifica di [ \_ modifica en](en-change.md) da un controllo di modifica standard, questa notifica viene ricevuta dopo l'aggiornamento dello schermo. |



 

 

 
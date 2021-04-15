---
description: Un'applicazione può usare un tipo di carattere per creare testo solo se il tipo di carattere è residente in un dispositivo specificato o installato nella tabella dei tipi di carattere di sistema.
ms.assetid: b422b981-8760-4484-9965-f212287c421e
title: Installazione ed eliminazione dei tipi di carattere
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0184054973c769462ed8c1620e5534ff909576ca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104994021"
---
# <a name="font-installation-and-deletion"></a>Installazione ed eliminazione dei tipi di carattere

Un'applicazione può usare un tipo di carattere per creare testo solo se il tipo di carattere è residente in un dispositivo specificato o installato nella tabella dei tipi di carattere di sistema. La tabella font è una matrice interna che identifica tutti i tipi di carattere non dispositivo disponibili per un'applicazione. Un'applicazione può recuperare i nomi dei tipi di carattere attualmente installati in un dispositivo o archiviati nella tabella dei tipi di carattere interna chiamando le funzioni [**EnumFontFamilies**](/windows/desktop/api/Wingdi/nf-wingdi-enumfontfamiliesa) o [**ChooseFont**](/previous-versions/windows/desktop/legacy/ms646914(v=vs.85)) .

Per installare temporaneamente un tipo di carattere, chiamare [**AddFontResource**](/windows/desktop/api/Wingdi/nf-wingdi-addfontresourcea) o [**AddFontResourceEx**](/windows/desktop/api/Wingdi/nf-wingdi-addfontresourceexa). Queste funzioni caricano un tipo di carattere archiviato in un file di risorse del tipo di carattere. Tuttavia, si tratta di un'installazione temporanea perché, dopo un riavvio, il tipo di carattere non sarà presente.

Per installare un tipo di carattere che resterà dopo il riavvio del sistema, usare uno dei metodi seguenti:

-   Passare al pannello di controllo, fare clic sull'icona dei **tipi di carattere** e selezionare **Installa nuovi tipi di carattere** dal menu **file** . Il tipo di carattere è disponibile per un'applicazione anche prima del riavvio. In una situazione di Terminal Server, tuttavia, il tipo di carattere è disponibile per la sessione corrente, ma non è disponibile per altre sessioni fino al riavvio.
-   Copiare il tipo di carattere nella cartella% windir% \\ fonts. Quindi, passare al pannello di controllo e fare clic sull'icona dei **tipi di carattere** oppure chiamare [**AddFontResource**](/windows/win32/api/wingdi/nf-wingdi-addfontresourcea) o [**AddFontResourceEx**](/windows/win32/api/wingdi/nf-wingdi-addfontresourceexa). Il tipo di carattere è disponibile per un'applicazione anche prima del riavvio. In una situazione di Terminal Server, tuttavia, il tipo di carattere è disponibile per la sessione corrente, ma non è disponibile per altre sessioni fino al riavvio. Se si copia solo il tipo di carattere nella cartella% windir% \\ Fonts, il tipo di carattere sarà disponibile solo dopo il riavvio del sistema.

Quando un'applicazione termina usando un tipo di carattere installato, deve rimuovere tale tipo di carattere chiamando la funzione [**RemoveFontResource**](/windows/desktop/api/Wingdi/nf-wingdi-removefontresourcea) .

Non è possibile modificare un tipo di carattere installato da una posizione diversa dalla cartella% windir% \\ Fonts quando viene caricato in una sessione attiva, inclusa la sessione 0. Qualsiasi tentativo di modificare, sostituire o eliminare sarà pertanto bloccato. Se è necessaria una modifica a un tipo di carattere:

-   I *tipi di carattere temporanei* vengono caricati solo nella sessione corrente. Prima di provare le modifiche ai tipi di carattere, chiamare [**RemoveFontResource**](/windows/desktop/api/Wingdi/nf-wingdi-removefontresourcea) per forzare la sessione corrente a scaricare il tipo di carattere.
-   I *tipi di carattere permanenti* rimangono installati dopo il riavvio e vengono caricati da tutte le sessioni create. Chiamare [**RemoveFontResource**](/windows/desktop/api/Wingdi/nf-wingdi-removefontresourcea) per forzare la sessione corrente a scaricare il tipo di carattere. Quindi, nella chiave del registro di sistema Font (**HKEY \_ Local \_ Machine \\ software \\ Microsoft \\ Windows NT \\ CurrentVersion \\ Fonts**) trovare e rimuovere il valore del registro di sistema associato al tipo di carattere. Infine, riavviare il computer per assicurarsi che il tipo di carattere non venga caricato in nessuna sessione. Dopo il riavvio, procedere con la modifica o l'eliminazione dei tipi di carattere.

Ogni volta che un'applicazione chiama le funzioni che aggiungono ed eliminano le risorse del tipo di carattere, deve chiamare anche la funzione [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage) e inviare un messaggio [**WM \_ FONTCHANGE**](wm-fontchange.md) a tutte le finestre di primo livello del sistema. Questo messaggio notifica ad altre applicazioni che la tabella dei tipi di carattere interna è stata modificata da un'applicazione che ha aggiunto o rimosso un tipo di carattere.

 

 

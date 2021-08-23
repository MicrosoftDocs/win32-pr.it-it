---
description: Un'applicazione può usare un tipo di carattere per disegnare testo solo se tale tipo di carattere è residente in un dispositivo specificato o è installato nella tabella dei tipi di carattere di sistema.
ms.assetid: b422b981-8760-4484-9965-f212287c421e
title: Installazione ed eliminazione dei tipi di carattere
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 112cfbff6bebdfc2fa4d46993f1fa60dcc19285bc3e16ebc2fd929e3a43ba679
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119037929"
---
# <a name="font-installation-and-deletion"></a>Installazione ed eliminazione dei tipi di carattere

Un'applicazione può usare un tipo di carattere per disegnare testo solo se tale tipo di carattere è residente in un dispositivo specificato o è installato nella tabella dei tipi di carattere di sistema. La tabella dei tipi di carattere è una matrice interna che identifica tutti i tipi di carattere non dispositivo disponibili per un'applicazione. Un'applicazione può recuperare i nomi dei tipi di carattere attualmente installati in un dispositivo o archiviati nella tabella dei tipi di carattere interna chiamando le funzioni [**EnumFontFamilies**](/windows/desktop/api/Wingdi/nf-wingdi-enumfontfamiliesa) [**o ChooseFont.**](/previous-versions/windows/desktop/legacy/ms646914(v=vs.85))

Per installare temporaneamente un tipo di carattere, chiamare [**AddFontResource**](/windows/desktop/api/Wingdi/nf-wingdi-addfontresourcea) o [**AddFontResourceEx**](/windows/desktop/api/Wingdi/nf-wingdi-addfontresourceexa). Queste funzioni caricano un tipo di carattere archiviato in un file di risorse del tipo di carattere. Si tratta tuttavia di un'installazione temporanea perché dopo un riavvio il tipo di carattere non sarà presente.

Per installare un tipo di carattere che rimarrà dopo il riavvio del sistema, usare uno dei metodi seguenti:

-   Passare al Pannello di controllo, fare clic **sull'icona Tipi di** carattere e selezionare Installa nuovi tipi **di** carattere dal menu **File.** Il tipo di carattere è disponibile per un'applicazione anche prima del riavvio. Tuttavia, in una situazione di terminal server il tipo di carattere è disponibile per la sessione corrente, ma non è disponibile per altre sessioni fino a dopo un riavvio.
-   Copiare il tipo di carattere nella cartella %windir% \\ fonts. Passare quindi al Pannello di controllo fare clic sull'icona Tipi di carattere oppure chiamare [**AddFontResource**](/windows/win32/api/wingdi/nf-wingdi-addfontresourcea) [**o AddFontResourceEx**](/windows/win32/api/wingdi/nf-wingdi-addfontresourceexa).  Il tipo di carattere è disponibile per un'applicazione anche prima del riavvio. Tuttavia, in una situazione di terminal server il tipo di carattere è disponibile per la sessione corrente, ma non è disponibile per altre sessioni fino a dopo un riavvio. Se si copia solo il tipo di carattere nella cartella %windir% fonts, il tipo di carattere sarà disponibile solo dopo il \\ riavvio del sistema.

Quando un'applicazione termina di usare un tipo di carattere installato, deve rimuoverlo chiamando la [**funzione RemoveFontResource.**](/windows/desktop/api/Wingdi/nf-wingdi-removefontresourcea)

Un tipo di carattere installato da un percorso diverso dalla cartella %windir% fonts non può essere modificato quando viene caricato in una sessione attiva, inclusa \\ la sessione 0. Qualsiasi tentativo di modifica, sostituzione o eliminazione verrà pertanto bloccato. Se è necessario apportare modifiche a un tipo di carattere:

-   *I tipi* di carattere temporanei vengono caricati solo nella sessione corrente. Prima di provare a apportare modifiche al tipo di carattere, chiamare [**RemoveFontResource**](/windows/desktop/api/Wingdi/nf-wingdi-removefontresourcea) per forzare la sessione corrente a scaricare il tipo di carattere.
-   *I tipi di* carattere permanenti rimangono installati dopo il riavvio e vengono caricati da tutte le sessioni create. Chiamare [**RemoveFontResource**](/windows/desktop/api/Wingdi/nf-wingdi-removefontresourcea) per forzare la sessione corrente a scaricare il tipo di carattere. Quindi, nella chiave del Registro di sistema del tipo di carattere (**HKEY \_ LOCAL MACHINE SOFTWARE Microsoft Windows NT \_ \\ \\ \\ \\ CurrentVersion \\ Fonts**) trovare e rimuovere il valore del Registro di sistema associato al tipo di carattere. Infine, riavviare il computer per assicurarsi che il tipo di carattere non sia caricato in alcuna sessione. Dopo il riavvio, procedere con la modifica o l'eliminazione del tipo di carattere.

Ogni volta che un'applicazione chiama le funzioni che aggiungono ed eliminano risorse del tipo di carattere, deve chiamare anche la funzione [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage) e inviare un [**messaggio WM \_ FONTCHANGE**](wm-fontchange.md) a tutte le finestre di primo livello del sistema. Questo messaggio notifica ad altre applicazioni che la tabella dei tipi di carattere interna è stata modificata da un'applicazione che ha aggiunto o rimosso un tipo di carattere.

 

 

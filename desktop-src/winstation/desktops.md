---
title: Desktop
description: Un desktop ha una superficie di visualizzazione logica e contiene oggetti dell'interfaccia utente, ad esempio Windows, menu e hook; può essere usato per creare e gestire Windows.
ms.assetid: c56cd63b-c260-40d0-9a62-1dee1eb18679
keywords:
- oggetti desktop
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44ca0b390ec4d34cc943c9d18d958cdea6466634
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106300114"
---
# <a name="desktops"></a>Desktop

Un *Desktop* ha una superficie di visualizzazione logica e contiene oggetti dell'interfaccia utente, ad esempio Windows, menu e hook; può essere usato per creare e gestire Windows. Ogni oggetto desktop è un oggetto a protezione diretta. Quando viene creato un desktop, questo viene associato alla stazione della [finestra](window-stations.md) corrente del processo chiamante e assegnato al thread chiamante.

I messaggi della finestra possono essere inviati solo tra processi presenti sullo stesso desktop. Inoltre, la procedura di hook di un processo in esecuzione su un particolare desktop può ricevere solo messaggi destinati a Windows creati nello stesso desktop.

È possibile usare i desktop associati alla stazione interattiva della finestra, WinSta0, per visualizzare un'interfaccia utente e ricevere l'input dell'utente, ma solo uno di questi desktop alla volta è attivo. Questo desktop attivo, noto anche come *desktop di input*, è quello attualmente visibile all'utente e riceve l'input dell'utente. Le applicazioni possono utilizzare la funzione [**OpenInputDesktop**](/windows/win32/api/winuser/nf-winuser-openinputdesktop) per ottenere un handle per il desktop di input. Le applicazioni che dispongono dell'accesso richiesto possono utilizzare la funzione [**SwitchDesktop**](/windows/win32/api/winuser/nf-winuser-switchdesktop) per specificare un desktop di input diverso.

Per impostazione predefinita, nella finestra interattiva sono disponibili tre desktop: default, ScreenSaver e Winlogon.

Il desktop predefinito viene creato quando Winlogon avvia il processo iniziale come utente connesso. A questo punto, il desktop predefinito diventa attivo e viene usato per interagire con l'utente.

Ogni volta che un screen saver protetto viene attivato, il sistema passa automaticamente al desktop dello ScreenSaver, che protegge i processi sul desktop predefinito da utenti non autorizzati. Gli screen saver non protetti vengono eseguiti in WinSta0 \\ predefinito.

Il desktop Winlogon è attivo mentre un utente esegue l'accesso. Il sistema passa al desktop predefinito quando la shell indica che è pronta per la visualizzazione di qualcosa o dopo trenta secondi, a seconda di quale si verifichi per primo. Durante la sessione dell'utente, il sistema passa al desktop di Winlogon quando l'utente preme la sequenza di tasti CTRL + ALT + CANC o quando la finestra di dialogo controllo dell'account utente (UAC) è aperta.

**Windows Server 2003 e Windows XP/2000:** La finestra di dialogo controllo dell'account utente non è supportata.

Il descrittore di sicurezza del desktop di Winlogon consente l'accesso a un set di account molto limitato, incluso l' [account LocalSystem](/windows/desktop/Services/localsystem-account). Le applicazioni in genere non contengono i SID di questi account nei token e pertanto non possono accedere al desktop di Winlogon oppure passano a un desktop diverso mentre il desktop Winlogon è attivo.

Per altre informazioni, vedere i seguenti argomenti:

-   [Creazione di finestre e desktop](window-station-and-desktop-creation.md)
-   [Connessione thread a un desktop](thread-connection-to-a-desktop.md)
-   [Diritti di accesso e sicurezza desktop](desktop-security-and-access-rights.md)

 

 
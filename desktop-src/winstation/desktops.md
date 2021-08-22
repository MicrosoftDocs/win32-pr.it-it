---
title: Desktop
description: Un desktop ha una superficie di visualizzazione logica e contiene oggetti dell'interfaccia utente, ad esempio finestre, menu e hook. può essere usato per creare e gestire finestre.
ms.assetid: c56cd63b-c260-40d0-9a62-1dee1eb18679
keywords:
- oggetti desktop
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b763c05c3d45c701da0bdd606fa906dec3f8af07ce72d256b402e7df5d9319b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119587351"
---
# <a name="desktops"></a>Desktop

Un *desktop ha* una superficie di visualizzazione logica e contiene oggetti dell'interfaccia utente, ad esempio finestre, menu e hook. può essere usato per creare e gestire finestre. Ogni oggetto desktop è un oggetto a protezione diretta. Quando viene creato, un desktop viene associato alla stazione della finestra [corrente](window-stations.md) del processo chiamante e assegnato al thread chiamante.

I messaggi della finestra possono essere inviati solo tra processi che siede sullo stesso desktop. Inoltre, la procedura hook di un processo in esecuzione su un determinato desktop può ricevere solo messaggi destinati alle finestre create nello stesso desktop.

I desktop associati alla stazione finestra interattiva, Winsta0, possono essere resi disponibili per visualizzare un'interfaccia utente e ricevere l'input dell'utente, ma solo uno di questi desktop alla volta è attivo. Questo desktop attivo, noto anche come *desktop di input,* è quello attualmente visibile all'utente e che riceve l'input dell'utente. Le applicazioni possono usare [**la funzione OpenInputDesktop**](/windows/win32/api/winuser/nf-winuser-openinputdesktop) per ottenere un handle per il desktop di input. Le applicazioni con l'accesso richiesto possono usare la [**funzione SwitchDesktop**](/windows/win32/api/winuser/nf-winuser-switchdesktop) per specificare un desktop di input diverso.

Per impostazione predefinita, nella stazione della finestra interattiva sono presenti tre desktop: Predefinito, ScreenSaver e Winlogon.

Il desktop predefinito viene creato quando Winlogon avvia il processo iniziale come utente connesso. A questo punto, il desktop predefinito diventa attivo e viene usato per interagire con l'utente.

Ogni volta che viene attivato un screen saver, il sistema passa automaticamente al desktop ScreenSaver, che protegge i processi nel desktop predefinito da utenti non autorizzati. Gli screen saver non protetti vengono eseguiti in Winsta0 \\ Default.

Il desktop winlogon è attivo durante l'accesso di un utente. Il sistema passa al desktop predefinito quando la shell indica che è pronto per visualizzare qualcosa o dopo trenta secondi, a seconda di quale sia il primo. Durante la sessione dell'utente, il sistema passa al desktop Winlogon quando l'utente preme la sequenza di tasti CTRL+ALT+CANC o quando è aperta la finestra di dialogo Controllo dell'account utente .

**Windows Server 2003 e Windows XP/2000:** La finestra di dialogo Controllo dell'account utente non è supportata.

Il descrittore di sicurezza del desktop Winlogon consente l'accesso a un set molto limitato di account, incluso [l'account LocalSystem](/windows/desktop/Services/localsystem-account). Le applicazioni in genere non trasportano i SID di questi account nei token e pertanto non possono accedere al desktop Winlogon o passare a un desktop diverso mentre il desktop Winlogon è attivo.

Per altre informazioni, vedere i seguenti argomenti:

-   [Creazione di window station e desktop](window-station-and-desktop-creation.md)
-   [Connessione thread a un desktop](thread-connection-to-a-desktop.md)
-   [Desktop Security and Access Rights](desktop-security-and-access-rights.md)

 

 
---
description: Finestra di dialogo Comune ChooseFont() Win32
ms.assetid: ee1df9f2-585f-4208-ad49-a0f6ba76f53a
title: Finestra di dialogo Comune ChooseFont() Win32
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95edc873d6984b5db312d3a86fc926f72817a5170672ad315d07e209d98c4398
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120098531"
---
# <a name="choosefont-win32-common-dialog"></a>Finestra di dialogo Comune ChooseFont() Win32

## <a name="affected-platforms"></a>Piattaforme interessate

**Client** - Windows 7  
**Server** - Windows Server 2008 R2  









## <a name="feature-impact"></a>Impatto sulle funzionalità

**Gravità** - Bassa  
**Frequenza** - Media  




## <a name="description"></a>Descrizione

Windows 7 include diversi aggiornamenti alla finestra di dialogo comune ChooseFont() Win32. Queste sono suddivise in due categorie:

-   Aggiornamento visivo della finestra di dialogo
-   Supporto per la nuova funzionalità mostra/nascondi tipi di carattere

**L'aggiornamento della** finestra di dialogo aggiorna il modello standard per allineare la finestra di dialogo con altri layout di dialogo Windows. Introduce WYSIWYG agli elenchi di visualizzazione dei tipi di carattere per consentire agli utenti di scegliere i tipi di carattere. Include anche un collegamento alla libreria CPL Fonts per fornire un facile accesso agli utenti che vogliono personalizzare gli elenchi di tipi di carattere.

**Mostra/Nascondi** tipi di carattere è una nuova funzionalità della piattaforma Windows 7 in base alla quale i tipi di carattere non appropriati per le impostazioni della lingua dell'utente corrente (metodi di input) non vengono presentati per impostazione predefinita negli elenchi di selezione dei tipi di carattere. Gli utenti possono personalizzare i tipi di carattere che desiderano visualizzare nella libreria di tipi di carattere O disabilitare questa funzionalità.

## <a name="manifestation-of-impact"></a>Manifestazione di impatto

**Aggiornamento dell'oggetto visivo della finestra di dialogo**

Sono stati introdotti due nuovi modelli in Windows 7 (uno per le applicazioni che caricano la versione 6 o successiva di comctl32.dll e l'altro per le applicazioni che caricano versioni precedenti).

-   Per motivi di compatibilità delle applicazioni, questi nuovi modelli verranno caricati solo per le applicazioni che non esegano la coda di messaggi ChooseFont. Le applicazioni che eseguono l'hook della coda di messaggi continueranno a visualizzare il layout della finestra di dialogo precedente.
-   Le applicazioni che forniscono i propri modelli continueranno a essere in grado di usarli.

Le applicazioni che non ottengono i nuovi modelli non noteranno modifiche al layout della finestra di dialogo da Vista. Dovrebbero comunque ottenere la nuova anteprima del tipo di carattere WYSIWYG.

**Mostra/Nascondi tipi di carattere**

Per tutte le versioni di ChooseFont, la finestra di dialogo userà le impostazioni del tipo di carattere show/hide dell'utente corrente per determinare l'elenco dei tipi di carattere da visualizzare. Ciò comporta la visualizzazione di un numero inferiore di elenchi di tipi di carattere nella maggior parte dei casi.

## <a name="end-user-mitigation"></a>Mitigazione dell'utente finale

**Mostra/Nascondi tipi di carattere:** Per disabilitare l'nascondiglio dei tipi di carattere, gli utenti devono passare alla pagina Impostazioni carattere in Fonts CPL (Tipi di carattere) e deselezionare l'opzione "

Casella di controllo "Nascondi tipi di carattere in base alle impostazioni della lingua"

## <a name="developer-mitigation"></a>Mitigazione degli sviluppatori

-   **Aggiornamento visivo:** Gli sviluppatori di applicazioni che forniscono i propri modelli possono voler aggiornare questo modello in modo che sia in linea con il nuovo modello Windows 7 appropriato. I nuovi modelli sono disponibili nel file di modello Font.dlg.

    **Nota:** Il nuovo modello pubblicato contiene un controllo SysLink aggiuntivo che fornisce un collegamento che consente agli utenti di avviare la libreria CPL Tipi di carattere per visualizzare altri tipi di carattere. Il controllo collegamento richiede la versione 6 della libreria Windows di controllo comune (comctl32.dll). Gli sviluppatori devono fornire un manifesto o una direttiva che specifica l'uso della versione 6 della DLL, se disponibile. Quando un'applicazione usa una versione precedente della libreria di controlli comuni, usare invece il tipo di controllo "PUSHBUTTON".

-   **Mostra/Nascondi tipi di carattere:** Gli sviluppatori possono disabilitare questa funzionalità fornendo un flag aggiuntivo (CF \_ INACTIVEFONTS) nel membro flags della struttura CHOOSEFONT. L'impostazione di questo flag determina la visualizzazione di tutti i tipi di carattere installati nell'elenco dei tipi di carattere.
-   **Mostra/Nascondi tipi di carattere:** Le applicazioni che forniscono contenuto della Guida chooseFont possono voler aggiungere contenuto per spiegare perché l'elenco dei tipi di carattere è ridotto e indirizzare gli utenti alla libreria CPL Tipi di carattere per personalizzare gli elenchi di tipi di carattere.

## <a name="compatibility-performance-reliability-and-usability-testing"></a>Test di compatibilità, prestazioni, affidabilità e usabilità

Gli sviluppatori le cui applicazioni collegano la coda di messaggi ChooseFont per personalizzare la finestra di dialogo devono verificare che le applicazioni mantenino tutte le funzionalità esistenti.

Le applicazioni che tagliano notevolmente l'elenco dei tipi di carattere usando flag devono garantire che l'elenco dei tipi di carattere presentato rimanga accettabile.

 

 




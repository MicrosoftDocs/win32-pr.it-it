---
description: .
ms.assetid: ee1df9f2-585f-4208-ad49-a0f6ba76f53a
title: ChooseFont () finestra di dialogo comune Win32
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e55a31d1f4d5530e04fe455135952eb94cc4bda
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318889"
---
# <a name="choosefont-win32-common-dialog"></a>ChooseFont () finestra di dialogo comune Win32

## <a name="affected-platforms"></a>Piattaforme interessate

**Client** -Windows 7  
**Server** -Windows Server 2008 R2  









## <a name="feature-impact"></a>Effetto sulle funzionalità

**Gravità** -bassa  
**Frequenza** -media  




## <a name="description"></a>Descrizione

Windows 7 include diversi aggiornamenti alla finestra di dialogo comune di ChooseFont () Win32. Questi rientrano in due categorie:

-   Aggiornamento visivo della finestra di dialogo
-   Supporto per la nuova funzionalità Mostra/Nascondi tipi di carattere

L' **aggiornamento della finestra di dialogo** aggiorna il modello standard per rendere la finestra di dialogo più in linea con altri layout di finestra di dialogo di Windows. Introduce gli elenchi di visualizzazione del tipo di carattere WYSIWYG per consentire agli utenti di scegliere i tipi di carattere. Include anche un collegamento al CPL dei tipi di carattere per facilitare l'accesso agli utenti che desiderano personalizzare gli elenchi di tipi di carattere.

**Mostra/Nascondi tipi di carattere** è una nuova funzionalità della piattaforma Windows 7 in cui i tipi di carattere non appropriati per le impostazioni della lingua dell'utente corrente (metodi di input) non vengono visualizzati per impostazione predefinita negli elenchi di selezione dei caratteri. Gli utenti possono personalizzare i tipi di carattere che desiderano visualizzare nel CPL dei tipi di carattere o possono disabilitare questa funzionalità.

## <a name="manifestation-of-impact"></a>Manifesto di effetto

**Aggiornamento visivo finestra di dialogo**

In Windows 7 sono stati introdotti due nuovi modelli (uno per le applicazioni che caricano la versione 6 o successiva di comctl32.dll e un'altra per le applicazioni che caricano versioni precedenti).

-   Per motivi di compatibilità delle applicazioni, questi nuovi modelli verranno caricati solo per le applicazioni che non eseguono l'hook della coda di messaggi ChooseFont. Le applicazioni che collegano la coda di messaggi continueranno a visualizzare il vecchio layout della finestra di dialogo.
-   Le applicazioni che forniscono modelli personalizzati continueranno a utilizzarle.

Le applicazioni che non ottengono i nuovi modelli non vedranno modifiche al layout della finestra di dialogo da vista. Dovrebbero comunque ottenere la nuova anteprima del tipo di carattere WYSIWYG.

**Mostra/Nascondi tipi di carattere**

Per tutte le versioni di ChooseFont, nella finestra di dialogo vengono usate le impostazioni del tipo di carattere Mostra/Nascondi dell'utente corrente per determinare l'elenco dei tipi di carattere da visualizzare. Questo comporterà la visualizzazione di un numero inferiore di elenchi di tipi di carattere nella maggior parte delle istanze.

## <a name="end-user-mitigation"></a>Attenuazione dell'utente finale

**Mostra/Nascondi tipi di carattere:** Per disabilitare il nascondimento dei tipi di carattere, gli utenti devono passare alla pagina delle impostazioni del tipo di carattere nel CPL dei tipi di carattere e deselezionare l'

Casella di controllo "Nascondi tipi di carattere basati su Impostazioni lingua"

## <a name="developer-mitigation"></a>Mitigazione degli sviluppatori

-   **Aggiornamento visivo:** Gli sviluppatori di applicazioni che forniscono i propri modelli potrebbero voler aggiornare questo oggetto in linea con il nuovo modello di Windows 7 appropriato. I nuovi modelli sono disponibili nel file di modello font. dlg.

    **Nota:** Il nuovo modello pubblicato contiene un controllo SysLink aggiuntivo che fornisce un collegamento che consente agli utenti di avviare il CPL dei tipi di carattere per visualizzare più tipi di carattere. Il controllo collegamento richiede la versione 6 della libreria di controlli comuni di Windows (comctl32.dll). Gli sviluppatori devono fornire un manifesto o una direttiva che specifichi l'uso della versione 6 della DLL, se disponibile. Se un'applicazione usa una versione precedente della libreria di controlli comuni, usare invece il tipo di controllo "pulsante".

-   **Mostra/Nascondi tipi di carattere:** Gli sviluppatori possono disabilitare questa funzionalità fornendo un flag aggiuntivo (CF \_ INACTIVEFONTS) nel membro Flags della struttura ChooseFont. L'impostazione di questo flag causa la visualizzazione di tutti i tipi di carattere installati nell'elenco dei tipi di carattere.
-   **Mostra/Nascondi tipi di carattere:** Le applicazioni che forniscono contenuto della Guida ChooseFont possono voler aggiungere contenuto per spiegare il motivo per cui l'elenco dei tipi di carattere viene ridotto e indirizzare gli utenti al CPL dei tipi di carattere per personalizzare gli elenchi di tipi di carattere

## <a name="compatibility-performance-reliability-and-usability-testing"></a>Compatibilità, prestazioni, affidabilità e test di usabilità

Gli sviluppatori le cui applicazioni collegano la coda di messaggi ChooseFont per personalizzare la finestra di dialogo devono verificare che le applicazioni mantengano tutte le funzionalità esistenti.

Le applicazioni che tagliano fortemente l'elenco dei tipi di carattere usando i flag devono assicurarsi che l'elenco dei tipi di carattere rimanga accettabile.

 

 




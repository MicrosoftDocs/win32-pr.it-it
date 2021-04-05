---
title: Utilizzo del ripristino dell'applicazione e riavvio
description: Un'applicazione può usare il ripristino e il riavvio dell'applicazione (ARR) per salvare i dati e le informazioni sullo stato prima che l'applicazione venga chiusa a causa di un'eccezione non gestita o quando l'applicazione smette di rispondere. Se richiesto, viene riavviata anche l'applicazione.
ms.assetid: 28cbb4c0-a287-4302-b3a9-daddc69adb40
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0d5bf0b9bd0e0f6cc257ee785ab5df6febc8fef
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103872593"
---
# <a name="using-application-recovery-and-restart"></a>Utilizzo del ripristino dell'applicazione e riavvio

Un'applicazione può usare il ripristino e il riavvio dell'applicazione (ARR) per salvare i dati e le informazioni sullo stato prima che l'applicazione venga chiusa a causa di un'eccezione non gestita o quando l'applicazione smette di rispondere. Se richiesto, viene riavviata anche l'applicazione.

Quando si esegue la registrazione per il ripristino o il riavvio, le informazioni di registrazione vengono aggiunte al processo. [Segnalazione errori Windows (WER)](/windows/desktop/wer/windows-error-reporting) usa le informazioni di registrazione per chiamare il callback di ripristino e riavviare l'applicazione. Se ad esempio si esegue la registrazione per il ripristino e l'applicazione rileva un'eccezione non gestita, WER Visualizza una finestra di dialogo per l'utente che consente all'utente di verificare la presenza di una soluzione online, chiudere il programma o eseguire il debug del programma. Se l'utente sceglie di verificare la presenza di una soluzione o di chiudere il programma, WER chiama il callback registrato e fornisce all'applicazione la possibilità di salvare i dati e le informazioni sullo stato. Al termine del ripristino, l'applicazione viene terminata.

Se si esegue la registrazione per il riavvio e l'applicazione rileva un'eccezione non gestita, WER Visualizza la stessa finestra di dialogo per l'utente, ma consente di riavviare il programma anziché chiudere il programma. Se si esegue la registrazione per il ripristino e il riavvio, viene eseguito prima il ripristino; l'applicazione viene quindi terminata e riavviata.

Un'applicazione che non risponde viene gestita in modo analogo. Un'applicazione è considerata non risponde se non risponde ai messaggi di Windows per cinque secondi e l'utente tenta di interagire con l'applicazione. l'utente visualizzerà (non risponde) nella barra del titolo. WER viene attivato quando l'utente fa clic sul pulsante Chiudi sistema.

È necessario eseguire la registrazione per il ripristino o il riavvio oppure rimuovere la registrazione prima che l'applicazione non risponda o riscontri un'eccezione non gestita. Tuttavia, nel callback di ripristino, è possibile modificare la riga di comando di riavvio.

Per informazioni dettagliate sulla registrazione per il ripristino o il riavvio, vedere gli argomenti seguenti:

-   [Registrazione per il ripristino dell'applicazione](registering-for-application-recovery.md)
-   [Registrazione per il riavvio dell'applicazione](registering-for-application-restart.md)

Per esempi che implementano le funzionalità di ripristino e riavvio, vedere gli esempi di AppRecovery e AppRestart nel Windows SDK che si trova nella \\ cartella winbase WindowsErrorReporting.

 

 
---
description: Quando si inizializza Winlogon, viene registrata la firma di accesso condiviso (SAS, Secure Attention Sequence) CTRL + ALT + CANC con il sistema, quindi vengono creati tre desktop all'interno della WinSta0 Window Station.
ms.assetid: 874aa12b-e213-4857-9600-698c28dfda37
title: Inizializzazione di Winlogon
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 768983d308228e73316c797fb67b035d491a1582
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233273"
---
# <a name="initializing-winlogon"></a>Inizializzazione di Winlogon

Quando si inizializza [Winlogon](winlogon.md) , viene registrata la firma di accesso condiviso (SAS, [*Secure Attention Sequence*](../secgloss/s-gly.md) ) CTRL + ALT + CANC con il sistema, quindi vengono creati tre desktop all'interno della WinSta0 Window Station.

La registrazione di CTRL + ALT + CANC rende questa inizializzazione il primo processo, assicurando così che nessun'altra applicazione abbia collegato la sequenza di chiavi.

WinSta0 è il nome dell'oggetto Window Station che rappresenta lo schermo fisico, la tastiera e il mouse. Winlogon crea i seguenti desktop nell'oggetto WinSta0.



| Desktop              | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Desktop Winlogon     | Questo è il desktop usato da Winlogon e [*Gina*](../secgloss/g-gly.md) per l'identificazione e l'autenticazione interattive e altre finestre di dialogo protette. Winlogon passa automaticamente a questo desktop quando riceve la notifica degli eventi SAS.                                                                                                                                                                                                                                                                                                                                                                          |
| Desktop applicazione  | Ogni volta che un utente accede correttamente, viene creato un desktop dell'applicazione per la [*sessione di accesso*](../secgloss/l-gly.md). Il desktop dell'applicazione è noto anche come desktop utente o predefinito. Questo desktop è il punto in cui si verificano tutte le attività degli utenti. Il desktop dell'applicazione è protetto; solo il sistema e la sessione di accesso interattivo possono accedervi. Si noti che solo una particolare istanza dell'utente connesso può accedere al desktop. Se l'utente interattivo attiva un processo con il controller del servizio, l'applicazione del servizio non avrà accesso al desktop dell'applicazione. |
| Desktop screen saver | Si tratta del desktop corrente quando viene eseguito un screen saver. Se un utente è connesso, sia il sistema che la sessione di accesso interattivo hanno accesso al desktop. In caso contrario, solo il sistema può accedere al desktop.                                                                                                                                                                                                                                                                                                                                                                                                                                      |



 

Poiché il proprietario di questi desktop, Winlogon può passare il desktop corrente o visibile a uno dei tre desktop e consentire a GINA di accedere a questa funzionalità. In generale, gli sviluppatori GINA non modificheranno il desktop corrente perché Winlogon imposta il desktop in modo appropriato prima di comunicare con GINA. La descrizione di ogni funzione GINA indica il desktop corrente per la chiamata.



| Per informazioni su                                    | Vedere                                                                                                      |
|----------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| Diversi stati in cui è possibile eseguire Winlogon           | [Stati di Winlogon](winlogon-states.md)                                                                   |
| Operazioni di timeout                                      | [Operazioni di Tempo di servizio della finestra di dialogo supportate](supported-dialog-box-service-time-out-operations.md) |
| Invio di messaggi a GINA durante la visualizzazione di una finestra di dialogo | [Invio di messaggi a GINA](sending-messages-to-the-gina.md)                                         |
| Funzioni di supporto                                        | [Funzioni di supporto di Winlogon](authentication-functions.md)                    |



 

 

 

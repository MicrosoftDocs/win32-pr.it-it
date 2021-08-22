---
description: Quando Winlogon viene inizializzato, registra la sequenza di attenzione sicura (SAS) CTRL+ALT+CANC con il sistema e quindi crea tre desktop all'interno della stazione della finestra WinSta0.
ms.assetid: 874aa12b-e213-4857-9600-698c28dfda37
title: Inizializzazione di Winlogon
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fff33740b77b23577cd7749b8cc745cd06a55e18675e35b817e405a71679b482
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119482393"
---
# <a name="initializing-winlogon"></a>Inizializzazione di Winlogon

Quando [Winlogon](winlogon.md) viene inizializzato, registra la [](../secgloss/s-gly.md) sequenza di attenzione sicura (SAS) CTRL+ALT+CANC con il sistema e quindi crea tre desktop all'interno della stazione della finestra WinSta0.

La registrazione di CTRL+ALT+CANC rende questa inizializzazione il primo processo, assicurando così che nessuna altra applicazione abbia collegato la sequenza di tasti.

WinSta0 è il nome dell'oggetto stazione finestra che rappresenta lo schermo fisico, la tastiera e il mouse. Winlogon crea i desktop seguenti nell'oggetto WinSta0.



| Desktop              | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Desktop winlogon     | Questo è il desktop che Winlogon e [*GINA*](../secgloss/g-gly.md) usano per l'identificazione e l'autenticazione interattive e altre finestre di dialogo sicure. Winlogon passa automaticamente a questo desktop quando riceve la notifica degli eventi di firma di accesso condiviso.                                                                                                                                                                                                                                                                                                                                                                          |
| Desktop dell'applicazione  | Ogni volta che un utente accede correttamente, viene creato un desktop applicazione per la [*sessione di accesso.*](../secgloss/l-gly.md) Il desktop dell'applicazione è noto anche come desktop predefinito o utente. Questo desktop è il punto in cui si svolge l'attività dell'utente. Il desktop dell'applicazione è protetto. solo il sistema e la sessione di accesso interattiva hanno accesso ad esso. Si noti che solo una particolare istanza dell'utente connesso ha accesso al desktop. Se l'utente interattivo attiva un processo usando il controller del servizio, tale applicazione di servizio non avrà accesso al desktop dell'applicazione. |
| Desktop dello screen saver | Questo è il desktop corrente quando un screen saver è in esecuzione. Se un utente è connesso, sia il sistema che la sessione di accesso interattiva hanno accesso al desktop. In caso contrario, solo il sistema può accedere al desktop.                                                                                                                                                                                                                                                                                                                                                                                                                                      |



 

In qualità di proprietario di questi desktop, Winlogon può passare il desktop corrente o visibile a uno dei tre desktop e consentire l'accesso a questa funzionalità da parte di GINA. In generale, gli sviluppatori DI GINA non modificheranno il desktop corrente perché Winlogon imposta il desktop in modo appropriato prima di comunicare con l'applicazione GINA. La descrizione di ogni funzione GINA indica quale desktop è corrente per la chiamata.



| Per informazioni su                                    | Vedere                                                                                                      |
|----------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| I diversi stati in cui è possibile eseguire Winlogon           | [Stati di Winlogon](winlogon-states.md)                                                                   |
| Operazioni di timeout                                      | [Operazioni di timeout del servizio Della finestra di dialogo supportate](supported-dialog-box-service-time-out-operations.md) |
| Invio di messaggi a GINA mentre viene visualizzata una finestra di dialogo | [Invio di messaggi all'applicazione GINA](sending-messages-to-the-gina.md)                                         |
| Funzioni di supporto                                        | [Funzioni di supporto di Winlogon](authentication-functions.md)                    |



 

 

 

---
description: Le specifiche di esempio includono l'invio di messaggi ActionData quando un'azione personalizzata crea o rimuove un account utente e segnalano un errore se non è possibile creare un account.
ms.assetid: ee90fe3d-51f4-433b-a5ce-950a03e1d8fb
title: Creazione delle tabelle ActionText ed Error
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a7b89c8150e3767841fe914cf55fc7be8c92e8cecf8f54f8486993d955349be
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120045401"
---
# <a name="authoring-the-actiontext-and-error-tables"></a>Creazione delle tabelle ActionText ed Error

Le specifiche di esempio includono l'invio di messaggi ActionData quando un'azione personalizzata crea o rimuove un account utente e segnalano un errore se non è possibile creare un account.

Immettere le voci seguenti nella tabella ActionText per specificare le informazioni usate dai messaggi ActionText.

[Tabella ActionText](actiontext-table.md)



| Azione            | Descrizione                                                       | Modello                          |
|-------------------|-------------------------------------------------------------------|-----------------------------------|
| ProcessAccounts   | Generazione di azioni per creare account utente nel computer locale. | Account: \[ 1 \] , Attributi: \[ 2\] |
| CreateAccount     | Creazione dell'account utente nel computer locale.                      | Account: \[ 1\]                    |
| RemoveAccount     | Rimozione dell'account utente dal computer locale.                    | Account: \[ 1\]                    |
| RollbackAccount   | Rollback della creazione di account utente nel computer locale. | Account: \[ 1\]                    |
| UninstallAccounts | Generazione di azioni per rimuovere gli account utente nel computer locale. | Account: \[ 1\]                    |



 

Immettere le voci seguenti nella tabella Errore per specificare le informazioni usate dalla segnalazione errori.

[Tabella degli errori](error-table.md)



| Errore | Message                                                                        |
|-------|--------------------------------------------------------------------------------|
| 25001 | Impossibile creare l'account utente ' \[ 2 \] ' nel computer locale. Codice errore: \[ 3 \] . |
| 25002 | L'account utente ' \[ 2 \] ' esiste già nel computer locale.                      |
| 25003 | Impossibile rimuovere l'account utente ' \[ 2 \] ' nel computer locale. Codice errore: \[ 3 \] . |
| 25004 | L'account \[ utente ' 2 ' non esiste nel \] computer locale.                      |



 

Continuare a [creare la tabella InstallExecuteSequence](authoring-the-installexecutesequence-table.md).

 

 




---
description: Le specifiche di esempio includono l'invio di messaggi ActionData quando un'azione personalizzata crea o rimuove un account utente e segnala un errore se non è possibile creare un account.
ms.assetid: ee90fe3d-51f4-433b-a5ce-950a03e1d8fb
title: Creazione di tabelle ActionText e Error
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e20646a90ca76c159a88bdd8a6d026ff10845da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103881097"
---
# <a name="authoring-the-actiontext-and-error-tables"></a>Creazione di tabelle ActionText e Error

Le specifiche di esempio includono l'invio di messaggi ActionData quando un'azione personalizzata crea o rimuove un account utente e segnala un errore se non è possibile creare un account.

Immettere le voci seguenti nella tabella ActionText per fornire le informazioni usate dai messaggi di ActionText.

[Tabella ActionText](actiontext-table.md)



| Azione            | Descrizione                                                       | Modello                          |
|-------------------|-------------------------------------------------------------------|-----------------------------------|
| ProcessAccounts   | Generazione di azioni per la creazione di account utente nel computer locale. | Account: \[ 1 \] , attributi: \[ 2\] |
| CreateAccount     | Creazione dell'account utente nel computer locale.                      | Account: \[ 1\]                    |
| RemoveAccount     | Rimozione dell'account utente dal computer locale.                    | Account: \[ 1\]                    |
| RollbackAccount   | Rollback della creazione degli account utente nel computer locale. | Account: \[ 1\]                    |
| UninstallAccounts | Generazione di azioni per la rimozione di account utente nel computer locale. | Account: \[ 1\]                    |



 

Immettere le voci seguenti nella tabella degli errori per fornire informazioni utilizzate da segnalazione errori.

[Tabella degli errori](error-table.md)



| Errore | Message                                                                        |
|-------|--------------------------------------------------------------------------------|
| 25001 | Non è possibile creare l'account utente ' \[ 2 \] ' nel computer locale. Codice di errore: \[ 3 \] . |
| 25002 | L'account utente ' \[ 2 \] ' esiste già nel computer locale.                      |
| 25003 | Non è possibile rimuovere l'account utente ' \[ 2 \] ' nel computer locale. Codice di errore: \[ 3 \] . |
| 25004 | L'account utente ' \[ 2 \] ' non esiste nel computer locale.                      |



 

Continuare con [la creazione della tabella InstallExecuteSequence](authoring-the-installexecutesequence-table.md).

 

 




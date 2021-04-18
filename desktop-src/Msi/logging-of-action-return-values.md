---
description: Il programma di installazione scrive i valori seguenti nel log quando un'azione restituisce questi codici di errore. Per l'elenco completo dei codici di errore restituiti dal Windows Installer funzione chiama MsiExec.exe e InstMsi.exe, vedere codici di errore.
ms.assetid: 653bbf45-ac2c-4f8a-a978-960e0c42e6e4
title: Registrazione dei valori restituiti dell'azione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aaaa203fee1fbb02bef070d065a9838383ea588b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319018"
---
# <a name="logging-of-action-return-values"></a>Registrazione dei valori restituiti dell'azione

Il programma di installazione scrive i valori seguenti nel log quando un'azione restituisce questi codici di errore. Per l'elenco completo dei codici di errore restituiti dal Windows Installer funzione chiama MsiExec.exe e InstMsi.exe, vedere [codici di errore](error-codes.md).



| Codice di errore                       | I valori restituiti dalle chiamate di funzione MsiExec.exe e InstMsi.exe | Valori visualizzati nel log. | Descrizione                                                                                                                                                                                                                                                                     |
|----------------------------------|----------------------------------------------------------------|--------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| funzione di errore \_ \_ non \_ chiamata     | 1626                                                           | 0                              | Impossibile eseguire una funzione.                                                                                                                                                                                                                                               |
| ERRORE \_ riuscito                   | 0                                                              | 1                              | Un'azione è stata completata correttamente.                                                                                                                                                                                                                                               |
| ERRORE di \_ installazione di \_ USEREXIT         | 1602                                                           | 2                              | Installazione annullata dall'utente.                                                                                                                                                                                                                                                   |
| ERRORE di \_ installazione \_          | 1603                                                           | 3                              | Errore irreversibile.                                                                                                                                                                                                                                                                  |
| ERRORE \_ installazione \_ sospensione          | 1604                                                           | 4                              | Installazione sospesa, incompleta.                                                                                                                                                                                                                                         |
| ERRORE \_ riuscito                   | 0                                                              | 5                              | L'azione è stata completata correttamente.                                                                                                                                                                                                                                              |
| ERRORE \_ di \_ handle non valido \_    | 1609                                                           | 6                              | Lo stato dell'handle non è valido.                                                                                                                                                                                                                                              |
| ERRORE \_ dati non validi \_             | 1626                                                           | 7                              | I dati non sono validi.                                                                                                                                                                                                                                                            |
| ERRORE di \_ installazione \_ già \_ in esecuzione | 1618                                                           | 8                              | È in corso un'altra installazione. Una sola installazione alla volta può eseguire azioni nelle tabelle [InstallExecuteSequence](installexecutesequence-table.md), [AdminExecuteSequence](adminexecutesequence-table.md)o [AdvtExecuteSequence](advtexecutesequence-table.md) . |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Registrazione Windows Installer](windows-installer-logging.md)
</dt> </dl>

 

 




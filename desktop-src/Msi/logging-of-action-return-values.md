---
description: Il programma di installazione scrive i valori seguenti nel log quando un'azione restituisce questi codici di errore. Per l'elenco completo dei codici di errore restituiti dalla funzione Windows Installer MsiExec.exe e InstMsi.exe, vedere Codici di errore.
ms.assetid: 653bbf45-ac2c-4f8a-a978-960e0c42e6e4
title: Registrazione dei valori restituiti dell'azione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 756fa633ef486c3dae4b689acf439f8dbf7786c20f740fb4784de30e764dc9fc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118945896"
---
# <a name="logging-of-action-return-values"></a>Registrazione dei valori restituiti dell'azione

Il programma di installazione scrive i valori seguenti nel log quando un'azione restituisce questi codici di errore. Per l'elenco completo dei codici di errore restituiti dalla funzione Windows Installer MsiExec.exe e InstMsi.exe, vedere [Codici di errore.](error-codes.md)



| Codice di errore                       | I valori restituiti dalle chiamate di MsiExec.exe e InstMsi.exe | Valori visualizzati nel log. | Descrizione                                                                                                                                                                                                                                                                     |
|----------------------------------|----------------------------------------------------------------|--------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| FUNZIONE \_ ERROR \_ NON \_ CHIAMATA     | 1626                                                           | 0                              | Non è stato possibile eseguire una funzione.                                                                                                                                                                                                                                               |
| ERRORE \_ RIUSCITO                   | 0                                                              | 1                              | Un'azione è stata completata correttamente.                                                                                                                                                                                                                                               |
| ERRORE \_ DURANTE \_ L'INSTALLAZIONE DI USEREXIT         | 1602                                                           | 2                              | Un'installazione annullata dall'utente.                                                                                                                                                                                                                                                   |
| ERRORE DURANTE \_ \_ L'INSTALLAZIONE          | 1603                                                           | 3                              | Errore irreversibile.                                                                                                                                                                                                                                                                  |
| ERRORE DURANTE \_ L'INSTALLAZIONE \_ DI SUSPEND          | 1604                                                           | 4                              | Installazione sospesa, incompleta.                                                                                                                                                                                                                                         |
| ERRORE \_ RIUSCITO                   | 0                                                              | 5                              | L'azione è stata completata correttamente.                                                                                                                                                                                                                                              |
| ERRORE STATO \_ \_ HANDLE NON \_ VALIDO    | 1609                                                           | 6                              | L'handle è in uno stato non valido.                                                                                                                                                                                                                                              |
| ERRORE \_ DATI NON \_ VALIDI             | 1626                                                           | 7                              | I dati non sono validi.                                                                                                                                                                                                                                                            |
| ERRORE DURANTE \_ \_ L'INSTALLAZIONE GIÀ \_ IN ESECUZIONE | 1618                                                           | 8                              | È in corso un'altra installazione. Solo un'installazione alla volta può eseguire azioni nelle tabelle [InstallExecuteSequence](installexecutesequence-table.md), [AdminExecuteSequence](adminexecutesequence-table.md)o [AdvtExecuteSequence](advtexecutesequence-table.md) . |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Windows Registrazione del programma di installazione](windows-installer-logging.md)
</dt> </dl>

 

 




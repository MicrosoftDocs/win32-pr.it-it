---
description: Immettere i record per le cinque azioni personalizzate di esempio create nella sezione precedente nella tabella CustomAction. Per ulteriori informazioni su come popolare la tabella CustomAction per questo tipo di azione personalizzata, vedere azione personalizzata di tipo 1.
ms.assetid: 56828105-bd72-426d-833f-f756c577c77f
title: Creazione della tabella CustomAction
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56fb7d8cf99a30200e6a5525e3516e2b888c1129
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967261"
---
# <a name="authoring-the-customaction-table"></a>Creazione della tabella CustomAction

Immettere i record per le cinque azioni personalizzate di esempio create nella sezione precedente nella [tabella CustomAction](customaction-table.md). Per ulteriori informazioni su come popolare la tabella CustomAction per questo tipo di azione personalizzata, vedere [azione personalizzata di tipo 1](custom-action-type-1.md).

[Tabella CustomAction](customaction-table.md)



| Azione            | Tipo  | Source (Sorgente)      | Destinazione                |
|-------------------|-------|-------------|-----------------------|
| ProcessAccounts   | 1     | Process.dll | ProcessUserAccounts   |
| UninstallAccounts | 1     | Process.dll | UninstallUserAccounts |
| CreateAccount     | 11265 | Create.dll  | CreateUserAccount     |
| RemoveAccount     | 11265 | Remove.dll  | RemoveUserAccount     |
| RollbackAccount   | 9473  | Remove.dll  | RemoveUserAccount     |



 

Il codice sorgente C++ per le librerie a collegamento dinamico è disponibile in Windows Installer SDK. Usare Process. cpp per creare il file Process.dll. Usare create. cpp per creare il file Create.dll. Usare Remove. cpp per creare Remove.dll. Aggiungere i file di libreria a collegamento dinamico alla tabella binaria.

[Tabella binaria](binary-table.md)



| Nome        | Data            |
|-------------|-----------------|
| Process.dll | {*dati binari*} |
| Create.dll  | {*dati binari*} |
| Remove.dll  | {*dati binari*} |



 

Continuare ad [aggiungere una tabella CustomUserAccounts personalizzata](adding-a-custom-customuseraccounts-table.md).

 

 




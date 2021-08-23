---
description: Immettere i record per le cinque azioni personalizzate di esempio create nella sezione precedente nella tabella CustomAction. Per altre informazioni su come popolare la tabella CustomAction per questo tipo di azione personalizzata, vedere Tipo di azione personalizzata 1.
ms.assetid: 56828105-bd72-426d-833f-f756c577c77f
title: Creazione della tabella CustomAction
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b618da6e88718aa59483b3b25c007ff0b41eb89f6e1dc18a7eb31563632dc54
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119066081"
---
# <a name="authoring-the-customaction-table"></a>Creazione della tabella CustomAction

Immettere i record per le cinque azioni personalizzate di esempio create nella sezione precedente nella [tabella CustomAction](customaction-table.md). Per altre informazioni su come popolare la tabella CustomAction per questo tipo di azione personalizzata, vedere [Tipo di azione personalizzata 1.](custom-action-type-1.md)

[Tabella CustomAction](customaction-table.md)



| Azione            | Tipo  | Source (Sorgente)      | Destinazione                |
|-------------------|-------|-------------|-----------------------|
| Account processo   | 1     | Process.dll | ProcessUserAccounts   |
| UninstallAccounts | 1     | Process.dll | UninstallUserAccounts |
| CreateAccount     | 11265 | Create.dll  | CreateUserAccount     |
| RemoveAccount     | 11265 | Remove.dll  | RemoveUserAccount     |
| RollbackAccount   | 9473  | Remove.dll  | RemoveUserAccount     |



 

Il codice sorgente C++ per le librerie a collegamento dinamico è disponibile in Windows Installer SDK. Usare Process.cpp per creare il file Process.dll. Usare Create.cpp per creare il file Create.dll. Usare Remove.cpp per creare Remove.dll. Aggiungere questi file di libreria a collegamento dinamico alla tabella Binaria.

[Tabella binaria](binary-table.md)



| Nome        | Dati            |
|-------------|-----------------|
| Process.dll | {*dati binari*} |
| Create.dll  | {*dati binari*} |
| Remove.dll  | {*dati binari*} |



 

Continuare con [l'aggiunta di una tabella CustomUserAccounts personalizzata.](adding-a-custom-customuseraccounts-table.md)

 

 




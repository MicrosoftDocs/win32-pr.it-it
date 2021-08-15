---
description: 'La tabella seguente elenca le cinque azioni personalizzate usate per soddisfare le specifiche di esempio: ProcessAccounts, UninstallAccounts, CreateAccounts, RemoveAccounts e RollbackAccounts.'
ms.assetid: 389ec652-243e-4392-aec9-3a7eb90e6c68
title: Creazione di azioni personalizzate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb6880f95b0468a495653057a9a5802af671c55b18b025c38a3191a4792e7558
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118381176"
---
# <a name="authoring-the-custom-actions"></a>Creazione di azioni personalizzate

La tabella seguente elenca le cinque azioni personalizzate usate per soddisfare le specifiche di esempio: ProcessAccounts, UninstallAccounts, CreateAccounts, RemoveAccounts e RollbackAccounts. Tutte queste azioni personalizzate sono presenti in [librerie a collegamento dinamico](dynamic-link-libraries.md) archiviate nella [tabella binaria](binary-table.md). Il codice sorgente C++ per le librerie a collegamento dinamico contenenti le azioni personalizzate di esempio è disponibile in Windows Installer SDK. ProcessAccounts e UninstallAccounts sono nel file Process.cpp. CreateAccount si trova nel file Create.cpp. RemoveAccount e RollbackAccount sono nel file Remove.cpp. Questi file di origine possono essere usati per creare i file Process.dll, Create.dll e Remove.dll.

Poiché la creazione o la rimozione di un account utente richiede privilegi [elevati,](deferred-execution-custom-actions.md) è necessario utilizzare azioni personalizzate di esecuzione posticipata eseguite nel contesto del sistema per creare, rimuovere o eseguire il rollback degli account utente. Le azioni personalizzate di esecuzione immediata, ProcessAccounts e UninstallAccounts, generano le azioni personalizzate posticipate che creano, rimuovono o e rollback gli account utente: CreateAccount, RemoveAccount e RollbackAccount.

Poiché le azioni personalizzate posticipate non possono leggere informazioni nelle tabelle di database, ProcessAccounts e UninstallUserAccouts devono impostare una proprietà CustomActionData per passare le informazioni nella tabella UserAccounts alle azioni personalizzate posticipate, come descritto in Recupero di informazioni di contesto per le azioni personalizzate di esecuzione [posticipata.](obtaining-context-information-for-deferred-execution-custom-actions.md) Quando il programma di installazione esegue lo script di esecuzione, le azioni personalizzate posticipate gestiscono gli account utente in base alle informazioni nella proprietà CustomActionData.

Poiché tutte le azioni personalizzate sono incluse in librerie a collegamento dinamico archiviate nella tabella Binary, tutte includono le costanti msidbCustomActionTypeDll e msidbCustomActionTypeBinaryData nel tipo numerico di base. ProcessAccounts e UninstallAccounts sono esempi di azione [personalizzata pura di tipo 1.](custom-action-type-1.md) Per informazioni su altri tipi di azione personalizzata, vedere [l'elenco di riepilogo di tutti i tipi di azione personalizzata.](summary-list-of-all-custom-action-types.md)

CreateAccount e RemoveAccount sono azioni [personalizzate di esecuzione posticipata](deferred-execution-custom-actions.md) che non consentono ai servizi di rappresentare utenti specifici. Queste azioni personalizzate includono le costanti msidbCustomActionTypeInScript e msidbCustomActionTypeNoImpersonate per specificare queste opzioni di esecuzione [nello script dell'azione personalizzata.](custom-action-in-script-execution-options.md)

RollbackAccount è [un'azione personalizzata di rollback che](rollback-custom-actions.md) rimuove solo gli account utente durante un'installazione di [rollback.](rollback-installation.md) RollbackAccount include le costanti msidbCustomActionTypeInScript e msidbCustomActionTypeRollback per specificare queste opzioni di esecuzione [nello script dell'azione personalizzata.](custom-action-in-script-execution-options.md)

Queste azioni personalizzate possono gestire dati sensibili, ad esempio le password utente, che non devono essere scritti nel file di log. Le azioni personalizzate posticipate devono pertanto includere msidbCustomActionTypeHideTarget nel tipo di azione personalizzata. I nomi delle azioni personalizzate posticipate devono essere aggiunti anche all'elenco delle proprietà [**MsiHiddenProperties**](msihiddenproperties.md) nella tabella [Property](property-table.md) a causa del modo in cui le azioni personalizzate immediate passano i dati alle azioni personalizzate posticipate usando la proprietà CustomActionData.



| Azione personalizzata     | Punto di ingresso DLL                       | Tipo di azione personalizzata                                                                                                                                                         |
|-------------------|---------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Account processo   | ProcessUserAccounts in Process.dll.   | msidbCustomActionTypeDll + msidbCustomActionTypeBinaryData = 1                                                                                                             |
| UninstallAccounts | UninstallUserAccounts in Process.dll. | msidbCustomActionTypeDll + msidbCustomActionTypeBinaryData = 1                                                                                                             |
| CreateAccount     | CreateUserAccount in Create.dll.      | msidbCustomActionTypeDll + msidbCustomActionTypeBinaryData + msidbCustomActionTypeInScript + msidbCustomActionTypeNoImpersonate + msidbCustomActionTypeHideTarget = 11265. |
| RemoveAccount     | RemoveUserAccount in Remove.dll.      | msidbCustomActionTypeDll + msidbCustomActionTypeBinaryData + msidbCustomActionTypeInScript + msidbCustomActionTypeNoImpersonate + msidbCustomActionTypeHideTarget = 11265. |
| RollbackAccount   | RemoveUserAccount in Remove.dll.      | msidbCustomActionTypeDll + msidbCustomActionTypeBinaryData + msidbCustomActionTypeInScript + msidbCustomActionTypeRollback + msidbCustomActionTypeHideTarget = 9473.       |



 

Passare alla [creazione della tabella CustomAction](authoring-the-customaction-table.md).

 

 




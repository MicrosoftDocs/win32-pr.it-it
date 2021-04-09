---
description: 'La tabella seguente elenca le cinque azioni personalizzate usate per soddisfare le specifiche di esempio: ProcessAccounts, UninstallAccounts, CreateAccounts, RemoveAccounts e RollbackAccounts.'
ms.assetid: 389ec652-243e-4392-aec9-3a7eb90e6c68
title: Creazione di azioni personalizzate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e09525490304762b98635bcbbe6c238ce3fe413f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967262"
---
# <a name="authoring-the-custom-actions"></a>Creazione di azioni personalizzate

La tabella seguente elenca le cinque azioni personalizzate usate per soddisfare le specifiche di esempio: ProcessAccounts, UninstallAccounts, CreateAccounts, RemoveAccounts e RollbackAccounts. Tutte queste azioni personalizzate si trovano nelle [librerie a collegamento dinamico](dynamic-link-libraries.md) archiviate nella [tabella binaria](binary-table.md). Il codice sorgente C++ per le librerie a collegamento dinamico che contiene le azioni personalizzate di esempio viene fornito in Windows Installer SDK. ProcessAccounts e UninstallAccounts sono nel file Process. cpp. CreateAccount si trova nel file create. cpp. RemoveAccount e RollbackAccount si trovano nel file Remove. cpp. Questi file di origine possono essere utilizzati per creare i file Process.dll, Create.dll e Remove.dll.

Poiché la creazione o la rimozione di un account utente richiede privilegi elevati, è necessario utilizzare le [azioni personalizzate di esecuzione posticipata](deferred-execution-custom-actions.md) eseguite nel contesto del sistema per creare, rimuovere o eseguire il rollback degli account utente. Le azioni personalizzate di esecuzione immediata, ProcessAccounts e UninstallAccounts, generano le azioni personalizzate posticipate per la creazione, la rimozione o il rollback degli account utente: CreateAccount, RemoveAccount e RollbackAccount.

Poiché le azioni personalizzate posticipate non possono leggere informazioni nelle tabelle di database, ProcessAccounts e UninstallUserAccouts devono impostare una proprietà CustomActionData per passare le informazioni nella tabella UserAccounts alle azioni personalizzate posticipate, come descritto in [ottenere informazioni sul contesto per le azioni personalizzate di esecuzione posticipata](obtaining-context-information-for-deferred-execution-custom-actions.md). Quando il programma di installazione esegue lo script di esecuzione, le azioni personalizzate posticipate gestiscono gli account utente in base alle informazioni contenute nella proprietà CustomActionData.

Poiché tutte le azioni personalizzate si trovano in librerie a collegamento dinamico archiviate nella tabella binaria, includono tutte le costanti msidbCustomActionTypeDll e msidbCustomActionTypeBinaryData nel tipo numerico di base. ProcessAccounts e UninstallAccounts sono esempi di [azione personalizzata pure di tipo 1](custom-action-type-1.md). Per informazioni sugli altri tipi di azione personalizzati, vedere l' [elenco riepilogativo di tutti i tipi di azione personalizzati](summary-list-of-all-custom-action-types.md).

CreateAccount e RemoveAccount sono [azioni personalizzate di esecuzione posticipata](deferred-execution-custom-actions.md) che non consentono ai servizi di rappresentare utenti specifici. Queste azioni personalizzate includono le costanti msidbCustomActionTypeInScript e msidbCustomActionTypeNoImpersonate per specificare le [Opzioni di esecuzione in-script di un'azione personalizzata](custom-action-in-script-execution-options.md).

RollbackAccount è un' [azione personalizzata di rollback](rollback-custom-actions.md) che rimuove solo gli account utente durante un' [installazione di rollback](rollback-installation.md). RollbackAccount include le costanti msidbCustomActionTypeInScript e msidbCustomActionTypeRollback per specificare le [Opzioni di esecuzione di un'azione personalizzata in-script](custom-action-in-script-execution-options.md).

Queste azioni personalizzate possono gestire dati sensibili, ad esempio password utente, che non devono essere scritte nel file di log. Le azioni personalizzate posticipate dovrebbero pertanto includere msidbCustomActionTypeHideTarget nel tipo di azione personalizzato. I nomi delle azioni personalizzate posticipate devono anche essere aggiunti all'elenco di proprietà [**MsiHiddenProperties**](msihiddenproperties.md) nella [tabella delle proprietà](property-table.md) a causa del modo in cui le azioni personalizzate immediate passano i dati alle azioni personalizzate posticipate usando la proprietà CustomActionData.



| Azione personalizzata     | Punto di ingresso DLL                       | Tipo di azione personalizzata                                                                                                                                                         |
|-------------------|---------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ProcessAccounts   | ProcessUserAccounts in Process.dll.   | msidbCustomActionTypeDll + msidbCustomActionTypeBinaryData = 1                                                                                                             |
| UninstallAccounts | UninstallUserAccounts in Process.dll. | msidbCustomActionTypeDll + msidbCustomActionTypeBinaryData = 1                                                                                                             |
| CreateAccount     | CreateUserAccount in Create.dll.      | msidbCustomActionTypeDll + msidbCustomActionTypeBinaryData + msidbCustomActionTypeInScript + msidbCustomActionTypeNoImpersonate + msidbCustomActionTypeHideTarget = 11265. |
| RemoveAccount     | RemoveUserAccount in Remove.dll.      | msidbCustomActionTypeDll + msidbCustomActionTypeBinaryData + msidbCustomActionTypeInScript + msidbCustomActionTypeNoImpersonate + msidbCustomActionTypeHideTarget = 11265. |
| RollbackAccount   | RemoveUserAccount in Remove.dll.      | msidbCustomActionTypeDll + msidbCustomActionTypeBinaryData + msidbCustomActionTypeInScript + msidbCustomActionTypeRollback + msidbCustomActionTypeHideTarget = 9473.       |



 

Continuare con [la creazione della tabella CustomAction](authoring-the-customaction-table.md).

 

 




---
description: Le azioni personalizzate ProcessAccounts e UninstallAccounts generano le azioni personalizzate posticipate che creano, rimuovono o rollback degli account utente.
ms.assetid: 245b576b-96cc-4eab-8848-5ff78ba32873
title: Creazione della tabella InstallExecuteSequence
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57ff6b8a551b141b5fc3f4d15318f2a6d98ff834cd33a572d542563adf55447b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118639172"
---
# <a name="authoring-the-installexecutesequence-table"></a>Creazione della tabella InstallExecuteSequence

Le azioni personalizzate ProcessAccounts e UninstallAccounts generano le azioni personalizzate posticipate che creano, rimuovono o rollback degli account utente. Le azioni personalizzate ProcessAccounts e UninstallAccounts devono essere immesse nella [tabella InstallExecuteSequence](installexecutesequence-table.md) da eseguire. Aggiungere le voci seguenti alla [tabella InstallExecuteSequence](installexecutesequence-table.md). Poiché queste azioni personalizzate devono far parte della generazione di script, è necessario sequenziare entrambe le azioni personalizzate dopo [l'azione InstallInitialize](installinitialize-action.md).

La condizione in ProcessAccounts garantisce quanto segue. Vedere [Sintassi di istruzioni condizionali](conditional-statement-syntax.md).

-   ProcessAccounts viene eseguito solo se il componente TestAccount viene installato in locale nel computer.
-   L'account di test del componente non è attualmente installato o è installato per l'esecuzione dall'origine.

La condizione in UninstallAccount garantisce quanto segue:

-   UninstallAccounts viene eseguito solo se il componente TestAccount è installato in locale nel computer.
-   È in corso la rimozione o l'installazione dell'account di test del componente per l'esecuzione dall'origine.

[Tabella InstallExecuteSequence](installexecutesequence-table.md)



| Azione            | Condition                                                           | Sequenza |
|-------------------|---------------------------------------------------------------------|----------|
| ProcessAccounts   | VersionNT AND (? TestAccount=2 OR ? TestAccount=4) AND $TestAccount=3 | 1550     |
| UninstallAccounts | VersionNT E ? TestAccount=3 AND ($TestAccount=4 OR $TestAccount=2) | 1560     |



 

Continuare a [Creare l'interfaccia utente per l'input della password.](authoring-the-user-interface-for-password-input.md)

 

 




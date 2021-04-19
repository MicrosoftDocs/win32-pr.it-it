---
description: Le azioni personalizzate ProcessAccounts e UninstallAccounts generano le azioni personalizzate posticipate che creano, rimuovono o ripristinano gli account utente.
ms.assetid: 245b576b-96cc-4eab-8848-5ff78ba32873
title: Creazione della tabella InstallExecuteSequence
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7aa09895d5e5d2543b5594f4795734d26163a4f1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311032"
---
# <a name="authoring-the-installexecutesequence-table"></a>Creazione della tabella InstallExecuteSequence

Le azioni personalizzate ProcessAccounts e UninstallAccounts generano le azioni personalizzate posticipate che creano, rimuovono o ripristinano gli account utente. È necessario immettere le azioni personalizzate ProcessAccounts e UninstallAccounts nella [tabella InstallExecuteSequence](installexecutesequence-table.md) da eseguire. Aggiungere le voci seguenti alla [tabella InstallExecuteSequence](installexecutesequence-table.md). Poiché queste azioni personalizzate devono far parte della generazione di script, entrambe le azioni personalizzate devono essere sequenziate dopo l' [azione InstallInitialize](installinitialize-action.md).

La condizione in ProcessAccounts garantisce quanto segue. Vedere [sintassi dell'istruzione condizionale](conditional-statement-syntax.md).

-   ProcessAccounts viene eseguito solo se il componente TestAccount viene installato localmente nel computer.
-   L'account di test del componente non è attualmente installato o è installato per l'esecuzione dall'origine.

La condizione in UninstallAccount garantisce quanto segue:

-   UninstallAccounts viene eseguito solo se il componente TestAccount è installato localmente nel computer.
-   L'account di test del componente verrà rimosso o installato per l'esecuzione dall'origine.

[Tabella InstallExecuteSequence](installexecutesequence-table.md)



| Azione            | Condizione                                                           | Sequenza |
|-------------------|---------------------------------------------------------------------|----------|
| ProcessAccounts   | VersionNT e (? TestAccount = 2 o? TestAccount = 4) e $TestAccount = 3 | 1550     |
| UninstallAccounts | VersionNT e? TestAccount = 3 e ($TestAccount = 4 o $TestAccount = 2) | 1560     |



 

Continuare a [creare l'interfaccia utente per l'input della password](authoring-the-user-interface-for-password-input.md).

 

 




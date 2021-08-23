---
description: Poiché controllo dell'account utente (UAC) in Windows Vista limita i privilegi durante un'installazione, gli sviluppatori di pacchetti del programma di installazione di Windows non devono presupporre che l'installazione abbia sempre accesso a tutte le parti del sistema.
ms.assetid: 8e3b4ad8-b978-4e27-b060-1d023846718f
title: Linee guida per i pacchetti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 930cb97cd2bb01a2bd69c5950a7e054c73d355e534ab67c812bcde44b7495b7b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119649321"
---
# <a name="guidelines-for-packages"></a>Linee guida per i pacchetti

Poiché controllo [*dell'account*](u-gly.md) utente (UAC) in Windows Vista limita i privilegi durante un'installazione, gli sviluppatori di pacchetti del programma di installazione di Windows non devono presupporre che l'installazione abbia sempre accesso a tutte le parti del sistema.

Un pacchetto del programma di installazione che può essere distribuito correttamente agli utenti standard [tramite](/previous-versions/windows/desktop/Policy/group-policy-start-page) Criteri di gruppo nella maggior parte dei casi dovrebbe funzionare anche con controllo dell'account utente in Windows Vista. Le eccezioni possono verificarsi se la tabella [InstallUISequence](installuisequence-table.md) contiene l'azione [LaunchConditions](launchconditions-action.md) o se la tabella [LaunchCondition](launchcondition-table.md) contiene una condizione basata sulla [proprietà Privileged](privileged.md). Windows Gli sviluppatori di pacchetti del programma di installazione devono pertanto rispettare le linee guida seguenti per garantire che il pacchetto funzioni con controllo dell'account utente e Windows Vista.

-   Quando si include [*una condizione di*](i-gly.md) contesto di installazione con un'azione nella tabella [InstallUISequence](installuisequence-table.md), usare un'istruzione condizionale basata sulla [proprietà Privileged](privileged.md). Non usare una condizione basata sulla [**proprietà AdminUser.**](adminuser.md)
-   Quando si include il contesto di installazione con le condizioni di avvio dell'installazione, usare un tipo di azione personalizzata [19](custom-action-type-19.md) nella tabella [InstallExecuteSequence](installexecutesequence-table.md) e rendere l'azione personalizzata condizionale sulla proprietà [Privileged](privileged.md). Non usare un'azione nella [tabella LaunchCondition](launchcondition-table.md) con una condizione basata sulla [proprietà AdminUser](adminuser.md) o Privileged.
-   Per leggere o modificare la [](deferred-execution-custom-actions.md) configurazione di sistema, usare un'azione personalizzata di esecuzione posticipata nella [tabella InstallExecuteSequence](installexecutesequence-table.md). Non usare azioni personalizzate di esecuzione immediata nella [tabella InstallUISequence](installuisequence-table.md) per modificare la configurazione di sistema.
-   Per modificare parti del sistema non specifiche dell'utente, usare un'azione personalizzata posticipata nella [tabella InstallExecuteSequence](installexecutesequence-table.md). È necessario includere il bit msidbCustomActionTypeNoImpersonate nel tipo di azione personalizzata.
-   Omettere il bit 3 dal valore della proprietà [**Riepilogo**](word-count-summary.md) conteggio parole per indicare che è possibile che sia necessario elevare il pacchetto. Non includere questo bit a meno che non siano necessari privilegi elevati per installare questo pacchetto.
-   Includere un manifesto con il livello di esecuzione richiesto dell'applicazione.
-   Includere un certificato nella [tabella MsiPatchCertificate](msipatchcertificate-table.md) del pacchetto originale e firmare tutte le patch con lo stesso certificato.
-   Se sono necessari privilegi elevati per installare un pacchetto del programma di installazione di Windows, l'autore del pacchetto deve includere l'attributo [ElevationShield](elevationshield-attribute.md) per il [controllo PushButton](pushbutton-control.md) usato per avviare l'installazione. Verrà visualizzato un avviso per l'utente che facendo clic sul pulsante verrà visualizzata la finestra di dialogo Controllo dell'account utente che richiede l'autorizzazione dell'amministratore per continuare l'installazione.
-   Impostare la [**proprietà MSIDEPLOYMENTCOMPLIANT**](msideploymentcompliant.md) su 1 per indicare al programma di installazione di Windows che il pacchetto è stato creato e testato per essere conforme al controllo dell'account utente in Windows Vista. Se questa proprietà non è impostata, il programma di installazione determina se il pacchetto è conforme al controllo dell'account utente.

Al di [Criteri di gruppo,](/previous-versions/windows/desktop/Policy/group-policy-start-page)è possibile usare il controllo seguente per la conformità del controllo dell'account utente Windows XP.

**Per verificare la conformità del controllo dell'account utente al di fuori Criteri di gruppo**

1.  Accedere al computer come amministratore.
2.  Annunciare il pacchetto per un'installazione per computer:

    **msiexec /jm** *package.msi*

3.  Disconnettersi dal computer.
4.  Accedere al computer come utente standard.
5.  Provare a installare il pacchetto annunciato:

    **msiexec /i** *package.msi*

6.  Nella maggior parte dei casi, se l'installazione ha esito positivo, il pacchetto è conforme al controllo dell'account utente.
7.  Impostare la [**proprietà MSIDEPLOYMENTCOMPLIANT**](msideploymentcompliant.md) nel pacchetto su 1.
8.  Testare la corretta installazione del pacchetto usando Windows Vista.

 

 

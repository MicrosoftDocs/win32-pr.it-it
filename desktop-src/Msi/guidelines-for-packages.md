---
description: Dato che il controllo dell'account utente in Windows Vista limita i privilegi durante un'installazione, gli sviluppatori di Windows Installer pacchetti non devono presupporre che l'installazione abbia sempre accesso a tutte le parti del sistema.
ms.assetid: 8e3b4ad8-b978-4e27-b060-1d023846718f
title: Linee guida per i pacchetti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db228c2dff443d421ddc089074f0fcce6ae93e2f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103882966"
---
# <a name="guidelines-for-packages"></a>Linee guida per i pacchetti

Dato che il [*controllo dell'account utente*](u-gly.md) in Windows Vista limita i privilegi durante un'installazione, gli sviluppatori di Windows Installer pacchetti non devono presupporre che l'installazione abbia sempre accesso a tutte le parti del sistema.

Nella maggior parte dei casi, un pacchetto di installazione che è possibile distribuire correttamente agli utenti standard tramite [criteri di gruppo](/previous-versions/windows/desktop/Policy/group-policy-start-page) dovrebbe funzionare anche con UAC in Windows Vista. È possibile che si verifichino eccezioni se la [tabella InstallUISequence](installuisequence-table.md) contiene l' [azione LaunchConditions](launchconditions-action.md) o la [tabella LaunchCondition](launchcondition-table.md) contiene una condizione basata sulla [Proprietà Privileged](privileged.md). Gli sviluppatori di pacchetti Windows Installer devono pertanto attenersi alle linee guida seguenti per assicurarsi che il pacchetto funzioni con UAC e Windows Vista.

-   Quando si include una condizione del [*contesto di installazione*](i-gly.md) con un'azione nella [tabella InstallUISequence](installuisequence-table.md), utilizzare un'istruzione condizionale basata sulla [Proprietà Privileged](privileged.md). Non usare una condizione basata sulla proprietà [**AdminUser**](adminuser.md) .
-   Quando si include il contesto di installazione con le condizioni di avvio dell'installazione, usare un' [azione personalizzata di tipo 19](custom-action-type-19.md) nella [tabella InstallExecuteSequence](installexecutesequence-table.md) e fare in modo che l'azione personalizzata sia condizionale sulla [Proprietà Privileged](privileged.md). Non usare un'azione nella [tabella LaunchCondition](launchcondition-table.md) con una condizione basata sulla [proprietà AdminUser](adminuser.md) o sulla proprietà privileged.
-   Per leggere o modificare la configurazione di sistema, usare un' [azione personalizzata di esecuzione posticipata](deferred-execution-custom-actions.md) nella [tabella InstallExecuteSequence](installexecutesequence-table.md). Non usare azioni personalizzate di esecuzione immediata nella [tabella InstallUISequence](installuisequence-table.md) per modificare la configurazione di sistema.
-   Per modificare parti del sistema che non sono specifiche dell'utente, utilizzare un'azione personalizzata rinviata nella [tabella InstallExecuteSequence](installexecutesequence-table.md). È necessario includere il bit msidbCustomActionTypeNoImpersonate nel tipo di azione personalizzata.
-   Omettere il bit 3 dal valore della proprietà riepilogo [**conteggio parole**](word-count-summary.md) per indicare che è possibile richiedere l'elevazione del pacchetto. Non includere questo bit a meno che non siano necessari privilegi elevati per installare il pacchetto.
-   Includere un manifesto con il livello di esecuzione richiesto dell'applicazione.
-   Includere un certificato nella tabella [MsiPatchCertificate](msipatchcertificate-table.md) del pacchetto originale e firmare tutte le patch con lo stesso certificato.
-   Se sono necessari privilegi elevati per installare un pacchetto di Windows Installer, l'autore del pacchetto deve includere l'attributo [ElevationShield](elevationshield-attribute.md) per il [controllo pulsante](pushbutton-control.md) utilizzato per avviare l'installazione. Verrà visualizzato un avviso per informare l'utente che facendo clic sul pulsante verrà visualizzata la finestra di dialogo controllo dell'account utente che richiede l'autorizzazione di amministratore per continuare l'installazione.
-   Impostare la proprietà [**MSIDEPLOYMENTCOMPLIANT**](msideploymentcompliant.md) su 1 per indicare al Windows Installer che il pacchetto è stato creato e testato per conformarsi a UAC in Windows Vista. Se questa proprietà non è impostata, il programma di installazione determina se il pacchetto è conforme a UAC.

Al di fuori di [criteri di gruppo](/previous-versions/windows/desktop/Policy/group-policy-start-page), è possibile utilizzare il controllo seguente per la conformità del controllo dell'account utente in Windows XP.

**Per verificare la conformità del controllo dell'account utente al di fuori di Criteri di gruppo**

1.  Accedere al computer come amministratore.
2.  Annunciare il pacchetto per un'installazione per computer:

    *package.msi* **msiexec/JM**

3.  Disconnettersi dal computer.
4.  Accedere al computer come utente standard.
5.  Tentativo di installare il pacchetto annunciato:

    **msiexec/i** *package.msi*

6.  Nella maggior parte dei casi, se l'installazione ha esito positivo, il pacchetto è conforme a controllo dell'account utente.
7.  Impostare la proprietà [**MSIDEPLOYMENTCOMPLIANT**](msideploymentcompliant.md) del pacchetto su 1.
8.  Verificare la corretta installazione del pacchetto utilizzando Windows Vista.

 

 

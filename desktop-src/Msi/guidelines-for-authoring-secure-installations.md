---
description: Per mantenere un ambiente protetto durante l'installazione del software, attenersi a queste linee guida durante la creazione del pacchetto Windows Installer.
ms.assetid: 04d91a9b-0528-4acb-8e11-fc817009db1f
title: Linee guida per la creazione di installazioni sicure
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9d18e66c38480149ddad9e381c6461ffe50cf0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314262"
---
# <a name="guidelines-for-authoring-secure-installations"></a>Linee guida per la creazione di installazioni sicure

Quando la creazione di un pacchetto di Windows Installer consente di mantenere un ambiente protetto durante l'installazione di, attenersi alle linee guida seguenti:

-   Gli amministratori devono installare le applicazioni gestite in una cartella di installazione di destinazione per cui gli utenti non amministratori non dispongono di privilegi di modifica o modifica.
-   Impostare una proprietà pubblica per qualsiasi proprietà dall'utente. Le proprietà private non possono essere modificate dall'utente che interagisce con l'interfaccia utente. Per informazioni, vedere informazioni [sulle proprietà](about-properties.md).
-   Non usare le proprietà per le password o altre informazioni che devono rimanere sicure. Il programma di installazione può scrivere in un log o nel registro di sistema il valore di una proprietà creata nella [tabella delle proprietà](property-table.md)o creato in fase di esecuzione. Per ulteriori informazioni, vedere [impedire che le informazioni riservate vengano scritte nel file di log](preventing-confidential-information-from-being-written-into-the-log-file.md).
-   Quando l'installazione richiede che il programma di installazione utilizzi privilegi [*elevati*](e-gly.md) , utilizzare [proprietà pubbliche limitate](restricted-public-properties.md) per limitare le proprietà pubbliche che un utente può modificare. Alcune restrizioni sono in genere necessarie per mantenere un ambiente protetto quando l'installazione richiede che il programma di installazione utilizzi privilegi *elevati* .
-   Evitare di installare servizi che impersonano i privilegi di un determinato utente, perché possono scrivere dati di sicurezza in un log o nel registro di sistema. Ciò consente di creare potenziali problemi di sicurezza, conflitti di password o la perdita di dati di configurazione al riavvio del sistema. Per informazioni dettagliate, vedere [tabella ServiceInstall](serviceinstall-table.md).
-   Usare la tabella [LockPermissions](lockpermissions-table.md) e la [tabella MsiLockPermissionsEx](msilockpermissionsex-table.md) per proteggere servizi, file, chiavi del registro di sistema e cartelle create in un ambiente bloccato.
-   Aggiungere una firma digitale all'installazione di per garantire l'integrità dei file. Per informazioni dettagliate, vedere [firme digitali e Windows Installer](digital-signatures-and-windows-installer.md) e [creazione di un'installazione con firma completamente verificata](authoring-a-fully-verified-signed-installation.md).
-   Creare il pacchetto di Windows Installer in modo che, se all'utente viene negato l'accesso alle risorse, l'installazione non riesce in modo da mantenere un ambiente protetto. Controllare i privilegi di accesso dell'utente e determinare se lo spazio su disco è sufficiente prima che inizi l'installazione. In genere, il programma di installazione deve visualizzare solo una finestra di dialogo Sfoglia se l'utente corrente è un amministratore o se l'installazione non richiede privilegi [*elevati*](e-gly.md) . Per informazioni dettagliate, vedere [resilienza del codice sorgente](source-resiliency.md).
-   Usare le [trasformazioni protette](secured-transforms.md) per archiviare le trasformazioni in un file system protetto localmente nel computer dell'utente. In questo modo si impedisce all'utente di disporre dell'accesso in scrittura alla trasformazione.
-   Per informazioni su come proteggere le origini multimediali di applicazioni gestite, vedere [resilienza dell'origine](source-resiliency.md).
-   Utilizzare la proprietà [**Riepilogo sicurezza**](security-summary.md) per indicare se il pacchetto deve essere aperto in sola lettura. Questa proprietà deve essere impostata su sola lettura consigliata per un database di installazione e per l'applicazione di sola lettura per una trasformazione o una patch.
-   Per impostazione predefinita, il programma di installazione esegue azioni personalizzate con privilegi utente per limitare l'accesso alle azioni personalizzate al sistema. Il programma di installazione può eseguire azioni personalizzate con privilegi [*elevati*](e-gly.md) se è in corso l'installazione di un'applicazione gestita o se i criteri di sistema sono stati specificati per privilegi elevati. Per informazioni dettagliate, vedere [sicurezza dell'azione personalizzata](custom-action-security.md).
-   Usare i criteri [DisablePatch](disablepatch.md) per fornire sicurezza negli ambienti in cui è necessario limitare l'applicazione di patch.
-   Utilizzare la [tabella AppID](appid-table.md) per registrare le impostazioni di configurazione e sicurezza comuni per gli oggetti DCOM.
-   Per informazioni correlate, vedere [linee guida per la protezione di azioni personalizzate](guidelines-for-securing-custom-actions.md).
-   Per informazioni correlate, vedere [linee guida per la protezione dei pacchetti nei computer bloccati](guidelines-for-securing-packages-on-locked-down-computers.md).
-   A partire da Windows Installer 3,0, il [controllo dell'account utente (UAC)](user-account-control--uac--patching.md) consente agli utenti non amministratori di applicare patch alle applicazioni installate nel contesto per computer. L'applicazione di patch del controllo dell'account utente è abilitata fornendo un certificato di firma nella tabella [MsiPatchCertificate](msipatchcertificate-table.md) e firmando patch con lo stesso certificato.
-   Le funzionalità della Windows Installer 5,0 per impostare le autorizzazioni di accesso su servizi, file, cartelle create e voci del registro di sistema possono contribuire a rendere più sicure le applicazioni di installazione. Per informazioni, vedere [protezione delle risorse](securing-resources-.md).

 

 




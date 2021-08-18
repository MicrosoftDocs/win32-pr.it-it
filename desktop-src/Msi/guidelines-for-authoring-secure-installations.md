---
description: Per mantenere un ambiente protetto durante l'installazione del software, attenersi a queste linee guida durante la creazione del pacchetto Windows Installer.
ms.assetid: 04d91a9b-0528-4acb-8e11-fc817009db1f
title: Linee guida per la creazione di installazioni sicure
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f796594fe665875f63751d0da4cac5bd7cde621e04b4d1d35585c74755dd719
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118635799"
---
# <a name="guidelines-for-authoring-secure-installations"></a>Linee guida per la creazione di installazioni sicure

La conformità alle linee guida seguenti quando si crea un pacchetto Windows installer consente di mantenere un ambiente sicuro durante l'installazione:

-   Gli amministratori devono installare le applicazioni gestite in una cartella di installazione di destinazione per la quale gli utenti non amministratori non hanno privilegi di modifica o modifica.
-   Impostare qualsiasi proprietà impostata dall'utente come proprietà pubblica. Le proprietà private non possono essere modificate dall'utente che interagisce con l'interfaccia utente. Per informazioni, vedere [Informazioni sulle proprietà.](about-properties.md)
-   Non usare proprietà per le password o altre informazioni che devono rimanere protette. Il programma di installazione può scrivere il valore di una proprietà creata nella tabella [Property](property-table.md)o creata in fase di esecuzione in un log o nel Registro di sistema. Per altre informazioni, vedere [Preventing Confidential Information From Being Written into the Log File](preventing-confidential-information-from-being-written-into-the-log-file.md).
-   Quando l'installazione richiede [](e-gly.md) che il programma di installazione usi privilegi elevati, usare [proprietà](restricted-public-properties.md) pubbliche con restrizioni per limitare le proprietà pubbliche che un utente può modificare. Alcune restrizioni sono in genere necessarie per mantenere un ambiente sicuro quando l'installazione richiede che il programma di installazione usi *privilegi* elevati.
-   Evitare di installare servizi che rappresentano i privilegi di un utente specifico, perché ciò potrebbe scrivere dati di sicurezza in un registro o nel Registro di sistema. Ciò può creare un problema di sicurezza, un conflitto di password o la perdita di dati di configurazione quando il sistema viene riavviato. Per informazioni dettagliate, vedere [La tabella ServiceInstall](serviceinstall-table.md).
-   Usare la [tabella LockPermissions](lockpermissions-table.md) e la tabella [MsiLockPermissionsEx](msilockpermissionsex-table.md) per proteggere servizi, file, chiavi del Registro di sistema e cartelle create in un ambiente bloccato.
-   Aggiungere firme digitali all'installazione per garantire l'integrità dei file. Per informazioni dettagliate, [vedere Firme digitali e Windows e](digital-signatures-and-windows-installer.md) Creazione di [un'installazione firmata completamente verificata.](authoring-a-fully-verified-signed-installation.md)
-   Creare il pacchetto Windows Installer in modo che, se all'utente viene negato l'accesso alle risorse, l'installazione non riesce in modo da mantenere un ambiente sicuro. Controllare i privilegi di accesso dell'utente e determinare se lo spazio su disco disponibile è sufficiente prima dell'inizio dell'installazione. In genere, il programma di installazione deve visualizzare una finestra di dialogo Sfoglia solo se l'utente corrente è un amministratore o se l'installazione non richiede [*privilegi*](e-gly.md) elevati. Per informazioni dettagliate, vedere [Resilienza dell'origine.](source-resiliency.md)
-   Usare [le trasformazioni protette](secured-transforms.md) per archiviare le trasformazioni in file system in locale nel computer dell'utente. In questo modo si impedisce all'utente di avere accesso in scrittura alla trasformazione.
-   Per informazioni su come proteggere le origini multimediali delle applicazioni gestite, vedere [Resilienza dell'origine.](source-resiliency.md)
-   Usare la [**proprietà Riepilogo**](security-summary.md) sicurezza per indicare se il pacchetto deve essere aperto in sola lettura. Questa proprietà deve essere impostata su read-only recommended per un database di installazione e su read-only enforced per una trasformazione o una patch.
-   Il programma di installazione esegue azioni personalizzate con privilegi utente per impostazione predefinita per limitare l'accesso delle azioni personalizzate al sistema. Il programma di installazione [](e-gly.md) può eseguire azioni personalizzate con privilegi elevati se è in corso l'installazione di un'applicazione gestita o se i criteri di sistema sono stati specificati per privilegi elevati. Per informazioni dettagliate, vedere [Sicurezza delle azioni personalizzate.](custom-action-security.md)
-   Usare i [criteri DisablePatch](disablepatch.md) per garantire la sicurezza negli ambienti in cui è necessario applicare restrizioni per l'applicazione di patch.
-   Usare la [tabella AppId per](appid-table.md) registrare le impostazioni di sicurezza e configurazione comuni per gli oggetti DCOM.
-   Per informazioni correlate, vedere [Linee guida per la protezione delle azioni personalizzate.](guidelines-for-securing-custom-actions.md)
-   Per informazioni correlate, vedere [Linee guida per la protezione dei pacchetti nei computer bloccati.](guidelines-for-securing-packages-on-locked-down-computers.md)
-   A partire da Windows Installer 3.0, l'applicazione di [patch](user-account-control--uac--patching.md) a Controllo dell'account utente consente agli utenti non amministratori di applicare patch alle applicazioni installate nel contesto per computer. L'applicazione di patch di Controllo dell'account utente viene abilitata fornendo un certificato del firmatario nella tabella [MsiPatchCertificate](msipatchcertificate-table.md) e firmando le patch con lo stesso certificato.
-   La capacità di Windows Installer 5.0 di impostare le autorizzazioni di accesso per servizi, file, cartelle create e voci del Registro di sistema può contribuire a rendere più sicure le applicazioni di installazione. Per informazioni, vedere [Protezione delle risorse.](securing-resources-.md)

 

 




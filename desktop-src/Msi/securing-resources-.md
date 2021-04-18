---
description: Le funzionalità del Windows Installer di impostare le autorizzazioni di accesso per servizi, file, cartelle create e voci del registro di sistema consentono di rendere più sicure le applicazioni di installazione.
ms.assetid: a25fcecf-f15f-4772-8f41-d03864484cc9
title: Protezione delle risorse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 415fe7b2df343a54aa0819031f4fd22b05857618
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313333"
---
# <a name="securing-resources"></a>Protezione delle risorse

Le funzionalità del Windows Installer di impostare le autorizzazioni di accesso per servizi, file, cartelle create e voci del registro di sistema consentono di rendere più sicure le applicazioni di installazione. L'utilizzo delle tabelle [MsiLockPermissionsEx](msilockpermissionsex-table.md) o [LockPermissions](lockpermissions-table.md) per proteggere le risorse è una delle [linee guida consigliate per la creazione di installazioni protette](guidelines-for-authoring-secure-installations.md). La tabella MsiLockPermissionsEx può consentire a un autore di pacchetti di proteggere una risorsa senza dover scrivere un' [azione personalizzata](custom-actions.md).

A partire dai pacchetti sviluppati per Windows Installer 5,0, la tabella [MsiLockPermissionsEx](msilockpermissionsex-table.md) deve sostituire l'uso della tabella [LockPermissions](lockpermissions-table.md) . La funzionalità estesa fornita dalla tabella MsiLockPermissionsEx consente a un pacchetto di proteggere i [Servizi](../services/services.md), i file, le cartelle e le chiavi del registro di sistema di Windows. Un pacchetto non deve contenere le tabelle MsiLockPermissionsEx e LockPermissions.

Windows Installer 4,5 e versioni precedenti ignora la [tabella MsiLockPermissionsEx](msilockpermissionsex-table.md). A partire da Windows Installer 5,0, l'installazione non riesce con un messaggio di errore 1941 se il pacchetto contiene sia una [tabella LockPermissions](lockpermissions-table.md) che una tabella MsiLockPermissionsEx. I pacchetti di installazione esistenti che contengono solo la tabella LockPermissions possono essere ancora installati con Windows Installer 5,0.

Windows Installer 5,0 elabora le informazioni nella tabella [MsiLockPermissionsEx](msilockpermissionsex-table.md) quando esegue le azioni standard [InstallFiles](installfiles-action.md), [InstallServices](installservices-action.md), [WriteRegistryValori consente](writeregistryvalues-action.md) e [CreateFolders](createfolders-action.md) . Un oggetto a protezione diretta deve essere installato o reinstallato per essere protetto e non è possibile aggiungere un elenco di [controllo di accesso](../secauthz/access-control-lists.md) (ACL) a un oggetto esistente senza reinstallare tale oggetto.

Per specificare il servizio, il file, la directory o la chiave del registro di sistema da proteggere, immettere le informazioni di identificazione nei campi LockObject e Table della tabella [MsiLockPermissionsEx](msilockpermissionsex-table.md) . Un oggetto viene identificato dalla relativa chiave primaria nella tabella [ServiceInstall](serviceinstall-table.md), nella tabella [file](file-table.md), nella [tabella del registro di sistema](registry-table.md)o nella [tabella CreateFolder](createfolder-table.md).

Per richiedere che le autorizzazioni specificate si applichino a un oggetto, immettere una stringa del descrittore di sicurezza valida nel campo *SDDLText* della tabella [MsiLockPermissionsEx](msilockpermissionsex-table.md) utilizzando il linguaggio SDDL ( [Security Descriptor Definition Language](../secauthz/security-descriptor-definition-language.md) ) valido. La tabella **MsiLockPermissionsEx** può specificare un descrittore di sicurezza che nega le autorizzazioni, specifica l'ereditarietà delle autorizzazioni da una risorsa padre o specifica le autorizzazioni di un nuovo account. Per un elenco di tutte le autorizzazioni che possono essere concesse, negate o ereditate, vedere [stringhe ACE](../secauthz/ace-strings.md). Windows Installer 5,0 estende il set di identificatori di sicurezza (SID) disponibili. Per un elenco dei SID validi, vedere [stringhe SID](../secauthz/sid-strings.md).

> [!NOTE]
> Se si desidera configurare il descrittore di sicurezza di una risorsa padre per specificare che le autorizzazioni vengono ereditate dagli oggetti figlio, è necessario che il programma di installazione applichi le autorizzazioni alla risorsa padre prima di creare gli oggetti figlio. Se il programma di installazione crea gli oggetti figlio prima di applicare le autorizzazioni ereditabili alla risorsa padre, le autorizzazioni della risorsa padre non verranno propagate agli oggetti figlio.

A partire da Windows Installer 5,0, il tipo di dati [FormattedSDDLText](formattedsddltext.md) estende il tipo di dati [formattato](formatted.md) . Il Windows Installer verifica che la stringa FormattedSDDLText immessa nella colonna SDDLText della tabella [MsiLockPermissionsEx](msilockpermissionsex-table.md) sia conforme al [formato della stringa del descrittore di sicurezza](../secauthz/security-descriptor-string-format.md).

**[Windows Installer 4,5 o versioni precedenti](not-supported-in-windows-installer-4-5.md):** Non supportato. La tabella [MsiLockPermissionsEx](msilockpermissionsex-table.md) e il tipo di dati [FormattedSDDLText](formattedsddltext.md) sono disponibili a partire da Windows Installer 5,0.

 

 

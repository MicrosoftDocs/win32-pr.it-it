---
description: Di seguito viene descritto come creare un pacchetto di Windows Installer per installare un assembly Win32.
ms.assetid: 1234e904-fc7f-4eb7-8c50-0c959bbf5261
title: Installazione degli assembly Win32 per la condivisione side-by-side
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea72c9bcb7bd85ac38dfc8857030d6b9d6afbf23
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317760"
---
# <a name="installing-win32-assemblies-for-side-by-side-sharing"></a>Installazione degli assembly Win32 per la condivisione side-by-side

Di seguito viene descritto come creare un pacchetto di Windows Installer per installare un assembly Win32. Il pacchetto installa un assembly affiancato nella cartella WinSxS per l'uso condiviso dell'applicazione. Dopo l'installazione del pacchetto, l'assembly condiviso è disponibile a livello globale per tutte le applicazioni che specificano una dipendenza dall'assembly in un file manifesto dell'assembly. Il programma di installazione non registra globalmente l'assembly affiancato nel sistema.

Si noti che è possibile installare assembly side-by-side condivisi usando i [moduli merge](merge-modules.md).

Prima di continuare è necessario comprendere come creare un pacchetto di Windows Installer senza assembly. Per un esempio di come creare un'installazione semplice, vedere [un esempio di installazione](an-installation-example.md).

**Per installare un assembly condiviso side-by-side**

1.  Definire un componente Windows Installer che includa l'assembly Win32. Questo componente può contenere altre risorse che devono essere sempre installate o rimosse con l'assembly. Tutti gli altri componenti dell'applicazione possono essere creati come per un'installazione senza assembly. Aggiungere una riga alla [tabella dei componenti](component-table.md) per il componente contenente l'assembly Win32. Immettere un [GUID](guid.md) Windows Installer valido per questo codice componente. Non usare il file manifesto come percorso della chiave per questo componente.
2.  Aggiungere una riga alla [tabella FeatureComponents](featurecomponents-table.md) che lega il componente a una funzionalità Windows Installer. Per informazioni, vedere [componenti e funzionalità](components-and-features.md). Una funzionalità di Windows Installer deve essere una parte della funzionalità dell'applicazione riconoscibile per un utente. L'assembly viene attivato quando questa funzionalità viene selezionata da un utente o con errori in da un'applicazione. Se l'assembly definisce una funzionalità aggiuntiva, aggiungere una riga aggiuntiva alla [tabella delle funzionalità](feature-table.md) per gli attributi della funzionalità. Questo passaggio non è necessario per la creazione di un modulo merge.
3.  Per gli assembly affiancati, le informazioni sull'associazione e sull'attivazione, come le classi COM, le interfacce e le librerie dei tipi, vengono archiviate in file manifesto invece che nel registro di sistema. Gli assembly condivisi archiviano queste informazioni in un manifesto dell'assembly. Nei sistemi che supportano gli assembly affiancati, il programma di installazione ignora l'elaborazione di tutte le informazioni relative al componente immesso nella [tabella di estensione](extension-table.md), nella tabella dei [verbi](verb-table.md), nella [tabella TypeLib](typelib-table.md), nella tabella [MIME](mime-table.md), nella tabella delle [classi](class-table.md), nella [tabella ProgId](progid-table.md)e nella [tabella AppID](appid-table.md). Le informazioni sul binding e sull'attivazione possono essere immesse in queste tabelle per l'uso da parte di sistemi che non supportano la condivisione di assembly affiancati.
4.  L'installazione side-by-side non registra l'assembly a livello globale, il programma di installazione ignora la registrazione automatica del componente se sono state immesse eventuali informazioni di registrazione automatica nella [tabella SelfReg](selfreg-table.md). È possibile immettere le informazioni di registrazione automatica nella tabella SelfReg per la registrazione automatica del componente nei sistemi che non supportano la condivisione di assembly affiancati.
5.  Aggiungere qualsiasi altra informazione del registro di sistema, esclusa l'associazione e l'attivazione o la registrazione automatica del componente, per la tabella [del registro di sistema](registry-table.md), la [tabella RemoveRegistry](removeregistry-table.md)e la [tabella dell'ambiente](environment-table.md).
6.  Poiché si tratta di un assembly condiviso, non viene generato un file. local. Non includere informazioni per questo componente nella [tabella IsolatedComponent](isolatedcomponent-table.md). Il programma di installazione ignora la tabella IsolatedComponent per questo componente nei sistemi operativi che supportano la condivisione side-by-side. Aggiungere informazioni alla tabella IsolatedComponent se si desidera che l'assembly sia privato nei sistemi che supportano i file con estensione local.
7.  Per abilitare la condivisione side-by-Side, è necessario che l'assembly Win32 sia installato nella cartella WinSxS. Questa operazione viene eseguita lasciando la \_ colonna applicazione file della [tabella MsiAssembly](msiassembly-table.md) null per l'assembly. Indica al programma di installazione di installare l'assembly nella cartella WinSxS, anziché nella cartella del componente. Aggiungere una riga alla [tabella MsiAssembly](msiassembly-table.md) per il componente che contiene l'assembly Win32. Immettere il valore 1 nel campo attributi della tabella MsiAssembly per specificare che si tratta di un assembly Win32. Per un assembly condiviso, lasciare vuoto il \_ campo applicazione file. Aggiungere l' [azione MsiPublishAssemblies](msipublishassemblies-action.md) alla tabella [InstallExecuteSequence](installexecutesequence-table.md) o [AdvtExecuteSequence](advtexecutesequence-table.md). Aggiungere l' [azione MsiUnpublishAssemblies](msiunpublishassemblies-action.md) alla tabella InstallExecuteSequence.
8.  Aggiungere righe alla [tabella MsiAssemblyName](msiassemblyname-table.md) per il componente. Aggiungere una riga per ogni coppia di nome e valore specificata nella sezione assemblyIdentity del manifesto. Per un esempio, vedere [tabella MsiAssemblyName](msiassemblyname-table.md).

 

 




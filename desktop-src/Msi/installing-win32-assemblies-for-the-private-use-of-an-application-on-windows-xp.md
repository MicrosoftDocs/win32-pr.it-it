---
description: Nella procedura descritta in questo argomento viene illustrato come creare un pacchetto di Windows Installer per installare un assembly Win32.
ms.assetid: 2d4bc2be-cce6-45e6-b6a7-7ff96d28eb96
title: Installazione di assembly Win32 per l'utilizzo privato di un'applicazione in Windows XP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e807e22c9c5dea67ece5ead0ded95f06ab203689
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307728"
---
# <a name="installing-win32-assemblies-for-the-private-use-of-an-application-on-windows-xp"></a>Installazione di assembly Win32 per l'utilizzo privato di un'applicazione in Windows XP

Nella procedura descritta in questo argomento viene illustrato come creare un pacchetto di Windows Installer per installare un assembly Win32. Il pacchetto installa l'assembly e un file manifesto dell'applicazione in una cartella creata che l'applicazione utilizza. Il manifesto dell'applicazione specifica la dipendenza dell'applicazione nell'assembly privato. Dopo l'installazione del pacchetto, l'assembly privato è disponibile per l'utilizzo esclusivo dell'applicazione. La dipendenza degli assembly specificata nel manifesto dell'applicazione sostituisce (per questa applicazione) qualsiasi altra dipendenza di assembly globale specificata nei file manifesto dell'assembly.

Prima di continuare, è consigliabile comprendere come creare un pacchetto di Windows Installer senza assembly. Per ulteriori informazioni, vedere [un esempio di installazione](an-installation-example.md).

**Per installare un assembly privato in Windows XP**

1.  Definire un componente Windows Installer che includa l'assembly Win32 e il file manifesto dell'applicazione. Questo componente può contenere altre risorse che devono essere sempre installate o rimosse con l'assembly. Nei passaggi rimanenti di questa procedura viene descritto come creare il database di installazione per installare questo componente.
2.  Aggiungere una riga alla [tabella dei componenti](component-table.md) per il componente che contiene l'assembly Win32 e il file manifesto dell'applicazione. Immettere un [GUID](guid.md) Windows Installer valido per questo codice componente. Per altre informazioni, vedere [modifica del codice del componente](changing-the-component-code.md) e [cosa accade se le regole dei componenti sono interrotte?](what-happens-if-the-component-rules-are-broken.md)
3.  Il programma di installazione copia il file manifesto dell'assembly nella cartella che contiene il file specificato nel \_ campo file Application della [tabella MsiAssembly](msiassembly-table.md).
4.  Aggiungere una riga alla [tabella FeatureComponents](featurecomponents-table.md) che lega il componente a una funzionalità Windows Installer. Per ulteriori informazioni, vedere [componenti e funzionalità](components-and-features.md). Una funzionalità di Windows Installer deve essere una parte della funzionalità dell'applicazione che un utente è in grado di riconoscere. L'assembly viene attivato quando questa funzionalità viene selezionata da un utente o con errori in da un'applicazione. Se l'assembly definisce una funzionalità aggiuntiva, aggiungere una riga aggiuntiva alla [tabella delle funzionalità](feature-table.md) per gli attributi della funzionalità. Questo passaggio non è necessario se si crea un modulo unione.
5.  Per gli assembly affiancati, le informazioni sull'associazione e sull'attivazione, ad esempio le classi COM, le interfacce e le librerie dei tipi, vengono archiviate in file manifesto invece che nel registro di sistema. Gli assembly privati archiviano queste informazioni in un manifesto dell'assembly. Nei sistemi che supportano gli assembly affiancati, il programma di installazione ignora l'elaborazione di tutte le informazioni sul componente immesso nella [tabella delle estensioni](extension-table.md), nella tabella dei [verbi](verb-table.md), nella [tabella TypeLib](typelib-table.md), nella tabella [MIME](mime-table.md), nella tabella delle [classi](class-table.md), nella [tabella ProgId](progid-table.md)e nella tabella [AppID](appid-table.md). Le informazioni di associazione e attivazione possono essere immesse nelle tabelle per l'uso da parte di sistemi che non supportano la condivisione di assembly affiancati.
6.  L'installazione side-by-side non registra l'assembly a livello globale. Il programma di installazione ignora la registrazione automatica del componente se nella [tabella SelfReg](selfreg-table.md)vengono immesse eventuali informazioni di registrazione automatica. È possibile immettere le informazioni di registrazione automatica nella tabella SelfReg per la registrazione automatica del componente nei sistemi che non supportano la condivisione di assembly affiancati.
7.  Aggiungere qualsiasi altra informazione del registro di sistema, esclusa l'associazione e l'attivazione o la registrazione automatica del componente, per la tabella [del registro di sistema](registry-table.md), la [tabella RemoveRegistry](removeregistry-table.md)e la [tabella dell'ambiente](environment-table.md).
8.  Il programma di installazione ignora la [tabella IsolatedComponent](isolatedcomponent-table.md) per questo componente nei sistemi operativi che supportano la condivisione side-by-side. Immettere le informazioni in questa tabella se si desidera che l'assembly sia privato nei sistemi che supportano i file locali.
9.  Aggiungere una riga alla [tabella MsiAssembly](msiassembly-table.md) per il componente che contiene l'assembly Win32. Immettere il valore 1 nel campo attributi della tabella MsiAssembly per specificare che si tratta di un assembly Win32. Immettere la chiave del file dell'assembly privato nel campo file \_ Application della [tabella MsiAssembly](msiassembly-table.md). Aggiungere l' [azione MsiPublishAssemblies](msipublishassemblies-action.md) alla tabella [InstallExecuteSequence](installexecutesequence-table.md) o [AdvtExecuteSequence](advtexecutesequence-table.md). Aggiungere l' [azione MsiUnpublishAssemblies](msiunpublishassemblies-action.md) alla tabella InstallExecuteSequence. Creare una cartella per l'assembly e il file manifesto nella [tabella directory](directory-table.md). Questa cartella deve trovarsi nella directory radice dell'applicazione e contenere il file specificato nel campo file \_ Application della [tabella MsiAssembly](msiassembly-table.md). Durante l'installazione dell'applicazione, il programma di installazione risolve la [tabella di directory](directory-table.md) per il percorso di questa cartella. Per ulteriori informazioni, vedere [utilizzo della tabella directory](using-the-directory-table.md).
10. Aggiungere righe alla [tabella MsiAssemblyName](msiassemblyname-table.md) per il componente. Aggiungere una riga per ogni coppia di nome e valore specificata nella sezione assemblyIdentity del manifesto. Per altre informazioni, vedere [tabella MsiAssemblyName](msiassemblyname-table.md).

 

 




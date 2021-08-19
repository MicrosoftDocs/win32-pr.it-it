---
description: La procedura descritta in questo argomento identifica come creare un pacchetto Windows Installer per installare un assembly Win32.
ms.assetid: 2d4bc2be-cce6-45e6-b6a7-7ff96d28eb96
title: Installazione di assembly Win32 per l'uso privato di un'applicazione in Windows XP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f478bddeb04ca9112610bd88338437002082204cc62078bde200539a8a18b6bb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119893811"
---
# <a name="installing-win32-assemblies-for-the-private-use-of-an-application-on-windows-xp"></a>Installazione di assembly Win32 per l'uso privato di un'applicazione in Windows XP

La procedura descritta in questo argomento identifica come creare un pacchetto Windows Installer per installare un assembly Win32. Il pacchetto installa l'assembly e un file manifesto dell'applicazione in una cartella di creazione utilizzata dall'applicazione. Il manifesto dell'applicazione specifica la dipendenza dell'applicazione dall'assembly privato. Dopo l'installazione del pacchetto, l'assembly privato è disponibile per l'uso esclusivo dell'applicazione. La dipendenza dell'assembly specificata nel manifesto dell'applicazione esegue l'override (per questa applicazione) di qualsiasi altra dipendenza di assembly globale specificata nei file manifesto dell'assembly.

Prima di continuare, è buona idea comprendere come creare un pacchetto Windows Installer senza assembly. Per altre informazioni, vedere [An Installation Example](an-installation-example.md).

**Per installare un assembly privato in Windows XP**

1.  Definire un Windows installer che includa l'assembly Win32 e il file manifesto dell'applicazione. Questo componente può contenere altre risorse che devono essere sempre installate o rimosse con l'assembly. I passaggi rimanenti di questa procedura descrivono come creare il database di installazione per installare questo componente.
2.  Aggiungere una riga alla tabella [Component per il](component-table.md) componente che contiene l'assembly Win32 e il file manifesto dell'applicazione. Immettere un GUID Windows programma [di installazione valido](guid.md) per questo codice componente. Per altre informazioni, vedere [Modifica del codice del componente](changing-the-component-code.md) e Cosa accade se le regole del componente vengono [interrotte?](what-happens-if-the-component-rules-are-broken.md)
3.  Il programma di installazione copia il file manifesto dell'assembly nella cartella che contiene il file specificato nel campo Applicazione file \_ della [tabella MsiAssembly](msiassembly-table.md).
4.  Aggiungere una riga alla tabella [FeatureComponents](featurecomponents-table.md) che consente di aggiungere il componente a una Windows programma di installazione. Per altre informazioni, vedere [Componenti e funzionalità.](components-and-features.md) Una Windows programma di installazione deve essere una parte della funzionalità dell'applicazione che un utente può riconoscere. L'assembly viene attivato quando questa funzionalità viene selezionata da un utente o in errore da un'applicazione. Se l'assembly definisce una funzionalità aggiuntiva, aggiungere un'altra riga alla [tabella Feature](feature-table.md) per gli attributi della funzionalità. Questo passaggio non è necessario se si crea un modulo unione.
5.  Per gli assembly side-by-side, le informazioni di associazione e attivazione, ad esempio classi COM, interfacce e librerie dei tipi, vengono archiviate nei file manifesto anziché nel Registro di sistema. Gli assembly privati archiviano queste informazioni in un manifesto dell'assembly. Nei sistemi che supportano assembly side-by-side, il programma di installazione ignora l'elaborazione delle informazioni sul componente immesso nella tabella [Extension](extension-table.md), nella tabella [Verbo](verb-table.md), nella tabella [TypeLib](typelib-table.md), nella tabella [MIME](mime-table.md) [,](class-table.md)nella tabella class , nella tabella [ProgId](progid-table.md)e nella tabella [AppId](appid-table.md). Le informazioni di associazione e attivazione possono essere immesse nelle tabelle per l'uso da parte di sistemi che non supportano la condivisione di assembly side-by-side.
6.  L'installazione side-by-side non registra l'assembly a livello globale. Il programma di installazione ignora la registrazione automatica del componente se vengono immesse informazioni di autoregistrazione nella [tabella SelfReg](selfreg-table.md). Le informazioni di auto-registrazione possono essere immesse nella tabella SelfReg per la registrazione automatica del componente nei sistemi che non supportano la condivisione di assembly side-by-side.
7.  Aggiungere eventuali altre informazioni del Registro di sistema, esclusive dell'associazione e dell'attivazione o della registrazione automatica del componente, alla tabella [Registry](registry-table.md), alla tabella [RemoveRegistry](removeregistry-table.md)e [alla tabella Environment](environment-table.md).
8.  Il programma di installazione ignora la [tabella IsolatedComponent](isolatedcomponent-table.md) per questo componente nei sistemi operativi che supportano la condivisione side-by-side. Immettere le informazioni in questa tabella se si vuole che l'assembly sia privato nei sistemi che supportano i file locali.
9.  Aggiungere una riga alla tabella [MsiAssembly per](msiassembly-table.md) il componente che contiene l'assembly Win32. Immettere il valore 1 nel campo Attributi della tabella MsiAssembly per specificare che si tratta di un assembly Win32. Immettere la chiave del file dell'assembly privato nel campo File \_ Application (Applicazione file) della [tabella MsiAssembly](msiassembly-table.md). Aggiungere [l'azione MsiPublishAssemblies](msipublishassemblies-action.md) alla [tabella InstallExecuteSequence](installexecutesequence-table.md) [o alla tabella AdvtExecuteSequence](advtexecutesequence-table.md). Aggiungere [l'azione MsiUnpublishAssemblies](msiunpublishassemblies-action.md) alla tabella InstallExecuteSequence. Creare una cartella per l'assembly e il file manifesto nella [tabella Directory](directory-table.md). Questa cartella deve essere nella directory radice dell'applicazione e contenere il file specificato nel campo File Application (Applicazione file) \_ della [tabella MsiAssembly](msiassembly-table.md). Durante l'installazione dell'applicazione, il programma di installazione risolve la [tabella Directory](directory-table.md) per il percorso di questa cartella. Per altre informazioni, vedere [Uso della tabella directory.](using-the-directory-table.md)
10. Aggiungere righe alla [tabella MsiAssemblyName per](msiassemblyname-table.md) il componente. Aggiungere una riga per ogni coppia nome/valore specificata nella sezione assemblyIdentity del manifesto. Per altre informazioni, vedere [Tabella MsiAssemblyName](msiassemblyname-table.md).

 

 




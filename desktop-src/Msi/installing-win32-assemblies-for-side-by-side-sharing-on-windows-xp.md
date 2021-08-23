---
description: Di seguito viene descritto come creare un pacchetto Windows Installer per installare un assembly Win32.
ms.assetid: 1234e904-fc7f-4eb7-8c50-0c959bbf5261
title: Installazione di assembly Win32 per la condivisione side-by-side
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c62607b37a9abd26ce031d922e67fa3f48963193af054e1d71c6903474220e82
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119500701"
---
# <a name="installing-win32-assemblies-for-side-by-side-sharing"></a>Installazione di assembly Win32 per la condivisione side-by-side

Di seguito viene descritto come creare un pacchetto Windows Installer per installare un assembly Win32. Il pacchetto installa un assembly side-by-side nella cartella Winsxs per l'uso condiviso dell'applicazione. Dopo l'installazione del pacchetto, l'assembly condiviso è disponibile a livello globale per qualsiasi applicazione che specifica una dipendenza dall'assembly in un file manifesto dell'assembly. Il programma di installazione non registra globalmente l'assembly side-by-side nel sistema.

Si noti che è possibile installare assembly side-by-side condivisi usando [i moduli unione.](merge-modules.md)

Prima di continuare, è necessario comprendere come creare un pacchetto Windows Installer senza assembly. Per un esempio di creazione di un'installazione semplice, vedere [An Installation Example](an-installation-example.md).

**Per installare un assembly condiviso side-by-side**

1.  Definire un Windows installer che include l'assembly Win32. Questo componente può contenere altre risorse che devono essere sempre installate o rimosse con l'assembly. Tutti gli altri componenti dell'applicazione possono essere creati come per un'installazione senza assembly. Aggiungere una riga alla tabella [Component per il](component-table.md) componente contenente l'assembly Win32. Immettere un GUID Windows programma [di installazione valido](guid.md) per questo codice componente. Non usare il file manifesto come percorso della chiave per questo componente.
2.  Aggiungere una riga alla tabella [FeatureComponents](featurecomponents-table.md) che consente di aggiungere il componente a una Windows programma di installazione. Per informazioni, vedere [Componenti e funzionalità.](components-and-features.md) Una Windows programma di installazione deve essere una parte della funzionalità dell'applicazione riconoscibile da un utente. L'assembly viene attivato quando questa funzionalità viene selezionata da un utente o in errore da un'applicazione. Se l'assembly definisce una funzionalità aggiuntiva, aggiungere un'altra riga alla [tabella Feature](feature-table.md) per gli attributi della funzionalità. Questo passaggio non è necessario quando si crea un modulo unione.
3.  Per gli assembly side-by-side, le informazioni di associazione e attivazione, ad esempio classi COM, interfacce e librerie dei tipi, vengono archiviate nei file manifesto anziché nel Registro di sistema. Gli assembly condivisi archiviano queste informazioni in un manifesto dell'assembly. Nei sistemi che supportano assembly side-by-side, il programma di installazione ignora l'elaborazione delle informazioni sul componente immesso nella tabella [Extension](extension-table.md), nella tabella [Verbo](verb-table.md), nella tabella [TypeLib](typelib-table.md), nella tabella [MIME](mime-table.md) [,](class-table.md)nella tabella class , nella tabella [ProgId](progid-table.md)e nella tabella [AppId](appid-table.md). Le informazioni di associazione e attivazione possono essere immesse in queste tabelle per l'uso da parte di sistemi che non supportano la condivisione di assembly side-by-side.
4.  L'installazione side-by-side non registra a livello globale l'assembly. Il programma di installazione ignora la registrazione automatica del componente se sono state immesse informazioni di autoregistrazione nella [tabella SelfReg](selfreg-table.md). Le informazioni di auto-registrazione possono essere immesse nella tabella SelfReg per la registrazione automatica del componente nei sistemi che non supportano la condivisione di assembly side-by-side.
5.  Aggiungere eventuali altre informazioni del Registro di sistema, esclusive dell'associazione e dell'attivazione o della registrazione automatica del componente, alla tabella [Registry](registry-table.md), alla tabella [RemoveRegistry](removeregistry-table.md)e [alla tabella Environment](environment-table.md).
6.  Poiché si tratta di un assembly condiviso, non viene generato un file con estensione local. Non includere informazioni per questo componente nella [tabella IsolatedComponent](isolatedcomponent-table.md). Il programma di installazione ignora la tabella IsolatedComponent per questo componente nei sistemi operativi che supportano la condivisione side-by-side. Aggiungere informazioni alla tabella IsolatedComponent se si vuole che l'assembly sia privato nei sistemi che supportano i file con estensione local.
7.  Per abilitare la condivisione side-by-side, l'assembly Win32 deve essere installato nella cartella Winsxs. A tale scopo, lasciare null la colonna File Application (Applicazione file) della tabella \_ [MsiAssembly](msiassembly-table.md) per l'assembly. Questo indica al programma di installazione di installare l'assembly nella cartella WinSxS anziché nella cartella del componente. Aggiungere una riga alla tabella [MsiAssembly per](msiassembly-table.md) il componente che contiene l'assembly Win32. Immettere il valore 1 nel campo Attributi della tabella MsiAssembly per specificare che si tratta di un assembly Win32. Per un assembly condiviso, lasciare vuoto il campo \_ Applicazione file. Aggiungere [l'azione MsiPublishAssemblies](msipublishassemblies-action.md) alla [tabella InstallExecuteSequence](installexecutesequence-table.md) [o alla tabella AdvtExecuteSequence](advtexecutesequence-table.md). Aggiungere [l'azione MsiUnpublishAssemblies](msiunpublishassemblies-action.md) alla tabella InstallExecuteSequence.
8.  Aggiungere righe alla [tabella MsiAssemblyName per](msiassemblyname-table.md) il componente. Aggiungere una riga per ogni coppia nome/valore specificata nella sezione assemblyIdentity del manifesto. Per un esempio, vedere [la tabella MsiAssemblyName](msiassemblyname-table.md).

 

 




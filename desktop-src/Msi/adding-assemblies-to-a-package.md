---
description: Windows Installer gli sviluppatori possono utilizzare le linee guida in questo argomento per creare Windows Installer pacchetti contenenti assembly.
ms.assetid: 60687a4f-aaa4-4264-a3f7-0a16eb1fb336
title: Aggiunta di assembly a un pacchetto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ded0795003ae8faf1b7bb945671990767d3eefb7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104227221"
---
# <a name="adding-assemblies-to-a-package"></a>Aggiunta di assembly a un pacchetto

Windows Installer gli sviluppatori possono utilizzare le linee guida in questo argomento per creare Windows Installer pacchetti contenenti assembly.

Le linee guida seguenti si applicano agli assembly Win32 e agli assembly utilizzati dal Common Language Runtime del Microsoft .NET Framework.

-   Un componente Windows Installer non deve contenere più di un assembly.
-   Tutti i file nell'assembly devono trovarsi in un singolo componente.
-   Ogni componente che contiene un assembly deve includere una voce nella tabella [MsiAssembly](msiassembly-table.md) .
-   Il nome di Assembly Cache forte di ogni assembly deve essere creato nella tabella [MsiAssemblyName](msiassemblyname-table.md) .
-   Utilizzare la tabella del [Registro di sistema](registry-table.md) anziché la tabella della [classe](class-table.md) quando si registra l'interoperabilità COM per un assembly.
-   Gli assembly con lo stesso nome sicuro sono lo stesso assembly. Quando lo stesso assembly viene installato da diverse applicazioni, i componenti che contengono l'assembly devono utilizzare lo stesso valore per ComponentId nelle tabelle dei [componenti](component-table.md) .

> [!Note]  
> Gli annunci di prodotto identificano gli assembly che possono essere installati e usati da applicazioni diverse. Gli annunci di prodotto non identificano gli assembly privati.

 

## <a name="adding-win32-assemblies"></a>Aggiunta di assembly Win32

Usare le linee guida seguenti quando si includono assembly Win32:

-   Il valore del percorso [della tabella dei componenti per](component-table.md) un componente che contiene un assembly Win32 non può essere null.
-   Il valore del percorso [della tabella dei componenti per](component-table.md) un componente che contiene un assembly dei criteri Win32 deve essere il file manifesto.
-   Il valore del percorso di un [componente che](component-table.md) contiene un assembly Win32, che non è un assembly dei criteri, non deve essere il file manifesto o il file di catalogo. Deve essere un file diverso nell'assembly.
-   Aggiungere una riga alla tabella [MsiAssemblyName](msiassemblyname-table.md) per ogni coppia di nome e valore elencate nella sezione **assemblyIdentity** del manifesto dell'assembly Win32.

## <a name="adding-assemblies-used-with-the-net-framework"></a>Aggiunta di assembly utilizzati con la .NET Framework

Usare le linee guida seguenti quando si includono assembly usati dal Common Language Runtime del .NET Framework.

-   Il valore del percorso [della tabella dei componenti per](component-table.md) un componente che contiene l'assembly non deve essere null.
-   Quando si installa un assembly utilizzato dal Common Language Runtime al Global Assembly Cache, il valore nella \_ colonna applicazione file della tabella MsiAssembly deve essere null.
-   Aggiungere una riga alla tabella [MsiAssemblyName](msiassemblyname-table.md) per ogni attributo del nome sicuro dell'assembly. Tutti gli assembly devono avere gli attributi Name, Version e culture specificati nella tabella MsiAssemblyName. Un attributo publicKeyToken è obbligatorio per un assembly globale. La tabella seguente è un esempio della tabella MsiAssemblyName per un assembly globale per l'uso da parte del Common Language Runtime.

[Tabella MsiAssemblyName](msiassemblyname-table.md)



| Componente  | Nome           | Valore            |
|------------|----------------|------------------|
| ComponentA | Nome           | simple           |
| ComponentA | version        | 1.0.0.0          |
| ComponentA | culture        | neutrale          |
| ComponentA | publicKeyToken | 9d1ec8380f483f5a |



 

 

 




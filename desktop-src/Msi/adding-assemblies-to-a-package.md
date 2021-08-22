---
description: Windows Gli sviluppatori del programma di installazione possono usare le linee guida in questo argomento per creare Windows di installazione che contengono assembly.
ms.assetid: 60687a4f-aaa4-4264-a3f7-0a16eb1fb336
title: Aggiunta di assembly a un pacchetto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68a96c1b8c8d9b73fedf03fceeb82be62b8457556da02334ed7a224aefc2202a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119534871"
---
# <a name="adding-assemblies-to-a-package"></a>Aggiunta di assembly a un pacchetto

Windows Gli sviluppatori del programma di installazione possono usare le linee guida in questo argomento per creare Windows di installazione che contengono assembly.

Le linee guida seguenti si applicano agli assembly Win32 e agli assembly utilizzati da Common Language Runtime .NET Framework Microsoft.

-   Un Windows installer non deve contenere più di un assembly.
-   Tutti i file nell'assembly devono essere in un singolo componente.
-   Ogni componente che contiene un assembly deve avere una voce nella [tabella MsiAssembly.](msiassembly-table.md)
-   Il nome sicuro della Cache assembly di ogni assembly deve essere creato nella [tabella MsiAssemblyName.](msiassemblyname-table.md)
-   Utilizzare la [tabella Registro](registry-table.md) di sistema anziché la [tabella Class](class-table.md) quando si registra l'interoperabilità COM per un assembly.
-   Gli assembly con lo stesso nome sicuro sono lo stesso assembly. Quando lo stesso assembly viene installato da applicazioni diverse, i componenti che contengono l'assembly devono usare lo stesso valore per ComponentId nelle tabelle [Component.](component-table.md)

> [!Note]  
> Gli annunci di prodotto identificano gli assembly che possono essere installati e usati da applicazioni diverse. Gli annunci di prodotto non identificano assembly privati.

 

## <a name="adding-win32-assemblies"></a>Aggiunta di assembly Win32

Quando si includono assembly Win32, usare le linee guida seguenti:

-   Il valore KeyPath nella [tabella Component](component-table.md) per un componente che contiene un assembly Win32 non deve essere Null.
-   Il valore KeyPath nella [tabella Component](component-table.md) per un componente che contiene un assembly di criteri Win32 deve essere il file manifesto.
-   Il valore KeyPath nella tabella [Component](component-table.md) per un componente che contiene un assembly Win32, che non è un assembly di criteri, non deve essere il file manifesto o il file di catalogo. Deve essere un file diverso nell'assembly.
-   Aggiungere una riga alla [tabella MsiAssemblyName](msiassemblyname-table.md) per ogni coppia nome/valore elencata nella **sezione assemblyIdentity** del manifesto dell'assembly Win32.

## <a name="adding-assemblies-used-with-the-net-framework"></a>Aggiunta di assembly usati con l'.NET Framework

Usare le linee guida seguenti quando si includono assembly utilizzati da Common Language Runtime .NET Framework.

-   Il valore KeyPath nella [tabella Component](component-table.md) per un componente che contiene l'assembly non deve essere Null.
-   Quando si installa un assembly usato da Common Language Runtime nella Global Assembly Cache, il valore nella colonna Applicazione file della tabella MsiAssembly deve \_ essere Null.
-   Aggiungere una riga alla [tabella MsiAssemblyName](msiassemblyname-table.md) per ogni attributo del nome sicuro dell'assembly. Tutti gli assembly devono avere gli attributi Name, Version e Culture specificati nella tabella MsiAssemblyName. Per un assembly globale è necessario un attributo publicKeyToken. La tabella seguente è un esempio della tabella MsiAssemblyName per un assembly globale che verrà utilizzata da Common Language Runtime.

[Tabella MsiAssemblyName](msiassemblyname-table.md)



| Componente  | Nome           | Valore            |
|------------|----------------|------------------|
| Componenta | Nome           | simple           |
| Componenta | version        | 1.0.0.0          |
| Componenta | culture        | neutrale          |
| Componenta | Publickeytoken | 9d1ec8380f483f5a |



 

 

 




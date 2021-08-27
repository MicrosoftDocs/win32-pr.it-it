---
description: La tabella MsiAssembly e la tabella MsiAssemblyName specificano Windows programma di installazione per gli assembly Common Language Runtime e gli assembly Win32.
ms.assetid: cfe9a0a3-e40f-4c59-b2e4-ad7654528e3b
title: Tabella MsiAssemblyName
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b62c494f9669ad2c119606f3950a0ec34b6bfd6ba78ad7a965c45398a71ebafe
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120129251"
---
# <a name="msiassemblyname-table"></a>Tabella MsiAssemblyName

Le [tabelle MsiAssembly e](msiassembly-table.md) MsiAssemblyName specificano le Windows del programma di installazione per gli assembly Common Language Runtime e gli assembly Win32. Per informazioni, vedere [Installazione di assembly nella Global Assembly Cache](installation-of-assemblies-to-the-global-assembly-cache.md) e Installazione di assembly [Win32.](installation-of-win32-assemblies.md)

La tabella MsiAssemblyName specifica lo schema per gli elementi di un nome di Assembly Cache sicuro per un assembly .NET Framework o Win32. Il nome viene costruito aggiungendo tutti gli elementi con la stessa chiave \_ Component. Vedere l'esempio seguente.

Windows Il programma di installazione può installare assembly Win32 [come assembly side-by-side.](side-by-side-assemblies.md) Per altre informazioni, vedere [l'API assembly side-by-side.](../sbscs/side-by-side-assembly-api.md)

La tabella MsiAssemblyName contiene le colonne seguenti.



| Colonna      | Tipo                         | Chiave | Nullable |
|-------------|------------------------------|-----|----------|
| Componente\_ | [Identificatore](identifier.md) | S   | N        |
| Nome        | [Text](text.md)             | S   | N        |
| Valore       | [Text](text.md)             | N   | N        |



 

## <a name="columns"></a>Colonne

<dl> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Componente\_
</dt> <dd>

Chiave nella tabella [dei componenti che](component-table.md) specifica il componente Windows Installer che contiene l'assembly.

</dd> <dt>

<span id="Name"></span><span id="name"></span><span id="NAME"></span>Nome
</dt> <dd>

Nome dell'attributo associato al valore specificato nella colonna Valore .

</dd> <dt>

<span id="Value"></span><span id="value"></span><span id="VALUE"></span>Valore
</dt> <dd>

Valore associato al nome specificato nella colonna Nome .

</dd> </dl>

## <a name="remarks"></a>Commenti

Le informazioni scritte nella tabella MsiAssemblyName devono corrispondere alle informazioni nel file manifesto dell'assembly. Se le informazioni nel manifesto e nella tabella MsiAssemblyName non corrispondono, la rimozione dell'applicazione può lasciare l'assembly nel computer.

Per gli assembly Win32 deve essere presente una riga nella tabella MsiAssemblyName per ognuna delle voci seguenti nel campo Nome: tipo, nome, versione, lingua, publicKeyToken e processorArchitecture. Il valore corrispondente per ogni nome può essere immesso nel campo Valore. Le coppie nome-valore nella tabella MsiAssemblyName devono corrispondere agli attributi type, name, version, language, publicKeyToken e processorArchitecture nel manifesto dell'assembly.

Per gli assembly Common Language Runtime privati (.NET Frameworkversioni 1.0 e 1.1), la tabella MsiAssemblyName deve includere una riga per ognuna delle voci seguenti nel campo Nome: Nome, Versione e Impostazioni cultura. Il valore corrispondente per ogni Nome può essere immesso nel campo Valore.

Per gli assembly Common Language Runtime globali (versioni .NET Framework 1.0 e 1.1), la tabella MsiAssemblyName deve includere una riga per ognuna delle voci seguenti nel campo Nome: Nome, Versione, Impostazioni cultura e PublicKeyToken. Il valore corrispondente per ogni Nome può essere immesso nel campo Valore.

La .NET Framework versione 1.1 è la versione minima che può essere usata per eseguire un aggiornamento sul posto di un assembly Common Language Runtime globale. È possibile controllare la [**proprietà MsiNetAssemblySupport**](msinetassemblysupport.md) per la versione. Anche la tabella MsiAssemblyName deve avere un campo FileVersion perché questo tipo di aggiornamento dell'assembly modifica solo FileVersion. Per altre informazioni, vedere [Aggiornamento degli assembly.](updating-assemblies.md)

Ad esempio, il manifesto dell'assembly per ComponentA potrebbe avere una sezione assemblyIdentity come indicato di seguito per un assembly Win32.

``` syntax
<assemblyIdentity type="win32" name="ms-sxstest-simple" version="1.0.0.0" language="en" publicKeyToken="1111111111222222" processorArchitecture="x86"/>
```

In questo caso, popolare la tabella MsiAssemblyName come indicato di seguito.



| Componente  | Nome                  | Valore             |
|------------|-----------------------|-------------------|
| Componenta | tipo                  | win32             |
| Componenta | name                  | ms-sxstest-simple |
| Componenta | version               | 1.0.0.0           |
| Componenta | Linguaggio              | en                |
| Componenta | Publickeytoken        | 1111111111222222  |
| Componenta | processorArchitecture | x86               |



 

## <a name="validation"></a>Convalida

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
[ICE66](ice66.md)  
[ICE83](ice83.md)  
</dl>

 

 

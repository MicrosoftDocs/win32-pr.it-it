---
description: La tabella MsiAssembly e la tabella MsiAssemblyName specificano Windows Installer impostazioni per assembly Common Language Runtime e assembly Win32.
ms.assetid: cfe9a0a3-e40f-4c59-b2e4-ad7654528e3b
title: Tabella MsiAssemblyName
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12008682c82d7be20ed8713d8dc1c416f9c7065c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319008"
---
# <a name="msiassemblyname-table"></a>Tabella MsiAssemblyName

La tabella [MsiAssembly](msiassembly-table.md) e la tabella MsiAssemblyName specificano Windows Installer impostazioni per assembly Common Language Runtime e assembly Win32. Per informazioni, vedere [installazione di assembly nella global assembly cache](installation-of-assemblies-to-the-global-assembly-cache.md) e [installazione di assembly Win32](installation-of-win32-assemblies.md).

La tabella MsiAssemblyName specifica lo schema per gli elementi di un nome di Assembly Cache forte per un .NET Framework o un assembly Win32. Il nome viene costruito accodando tutti gli elementi con la stessa chiave del componente \_ . Vedere l'esempio seguente.

Windows Installer possibile installare assembly Win32 come [assembly side-by-side](side-by-side-assemblies.md). Per ulteriori informazioni, vedere l' [API assembly side-by-side](../sbscs/side-by-side-assembly-api.md).

La tabella MsiAssemblyName include le colonne seguenti.



| Colonna      | Tipo                         | Chiave | Nullable |
|-------------|------------------------------|-----|----------|
| Componente\_ | [Identificatore](identifier.md) | S   | N        |
| Nome        | [Text](text.md)             | S   | N        |
| Valore       | [Text](text.md)             | N   | N        |



 

## <a name="columns"></a>Colonne

<dl> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Componente\_
</dt> <dd>

Chiave nella [tabella dei componenti](component-table.md) che specifica il componente Windows Installer che contiene l'assembly.

</dd> <dt>

<span id="Name"></span><span id="name"></span><span id="NAME"></span>Nome
</dt> <dd>

Nome dell'attributo associato al valore specificato nella colonna valore.

</dd> <dt>

<span id="Value"></span><span id="value"></span><span id="VALUE"></span>Valore
</dt> <dd>

Valore associato al nome specificato nella colonna Name.

</dd> </dl>

## <a name="remarks"></a>Commenti

Le informazioni create nella tabella MsiAssemblyName devono corrispondere a quelle contenute nel file manifesto dell'assembly. Se le informazioni contenute nella tabella manifest e MsiAssemblyName non corrispondono, la rimozione dell'applicazione può lasciare l'assembly nel computer.

Per gli assembly Win32 è necessario che nella tabella MsiAssemblyName sia presente una riga per ognuna delle voci seguenti nel campo Nome: tipo, nome, versione, lingua, publicKeyToken e processorArchitecture. Il valore corrispondente per ogni nome può essere immesso nel campo del valore. Le coppie nome-valore nella tabella MsiAssemblyName devono corrispondere agli attributi Type, Name, Version, language, publicKeyToken e processorArchitecture nel manifesto dell'assembly.

Per gli assembly di Common Language Runtime privati (.NET FrameworkVersions 1,0 e 1,1), la tabella MsiAssemblyName deve includere una riga per ognuna delle voci seguenti nel campo Nome: nome, versione e impostazioni cultura. Il valore corrispondente per ogni nome può essere immesso nel campo del valore.

Per gli assembly di Common Language Runtime globali (.NET Framework versioni 1,0 e 1,1), la tabella MsiAssemblyName deve includere una riga per ognuna delle voci seguenti nel campo Nome: nome, versione, lingua e PublicKeyToken. Il valore corrispondente per ogni nome può essere immesso nel campo del valore.

Il .NET Framework versione 1,1 è la versione minima che può essere usata per eseguire un aggiornamento sul posto di un assembly di Common Language Runtime globale. È possibile controllare la proprietà [**MsiNetAssemblySupport**](msinetassemblysupport.md) per la versione. La tabella MsiAssemblyName deve avere anche un campo FileVersion perché questo tipo di aggiornamento dell'assembly modifica solo la versione Fileversion. Per ulteriori informazioni, vedere [aggiornamento degli assembly](updating-assemblies.md).

Ad esempio, il manifesto dell'assembly per Componenta potrebbe avere una sezione assemblyIdentity come indicato di seguito per un assembly Win32.

``` syntax
<assemblyIdentity type="win32" name="ms-sxstest-simple" version="1.0.0.0" language="en" publicKeyToken="1111111111222222" processorArchitecture="x86"/>
```

In questo caso, popolare la tabella MsiAssemblyName come indicato di seguito.



| Componente  | Nome                  | Valore             |
|------------|-----------------------|-------------------|
| ComponentA | tipo                  | Win32             |
| ComponentA | name                  | MS-sxstest-semplice |
| ComponentA | version               | 1.0.0.0           |
| ComponentA | Linguaggio              | en                |
| ComponentA | publicKeyToken        | 1111111111222222  |
| ComponentA | processorArchitecture | x86               |



 

## <a name="validation"></a>Convalida

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
[ICE66](ice66.md)  
[ICE83](ice83.md)  
</dl>

 

 

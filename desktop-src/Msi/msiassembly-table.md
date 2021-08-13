---
description: La tabella MsiAssembly specifica le Windows del programma di installazione per gli assembly .NET Framework Microsoft e gli assembly Win32. Per altre informazioni, vedere Installazione di assembly nella Global Assembly Cache e Installazione di assembly Win32.
ms.assetid: 3a8cd206-0112-4840-8c9d-773483f5c771
title: Tabella MsiAssembly
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: acda246bd6baba75d0f7e8d53f515a25abb0c163c2d3ef0b1b9705c123b8e69e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119381381"
---
# <a name="msiassembly-table"></a>Tabella MsiAssembly

La tabella MsiAssembly specifica le Windows del programma di installazione per gli assembly .NET Framework Microsoft e gli assembly Win32. Per altre informazioni, vedere [Installazione di assembly nella Global Assembly Cache](installation-of-assemblies-to-the-global-assembly-cache.md) e Installazione di assembly [Win32.](installation-of-win32-assemblies.md)

In Windows XP, Windows programma di installazione può installare assembly Win32 come [assembly side-by-side.](side-by-side-assemblies.md) Per altre informazioni, vedere [l'API assembly side-by-side.](../sbscs/side-by-side-assembly-api.md)

**Windows 2000:** Questa funzionalità non è supportata.

La tabella MsiAssembly include le colonne seguenti.



| Colonna            | Tipo                         | Chiave | Nullable |
|-------------------|------------------------------|-----|----------|
| Componente\_       | [Identificatore](identifier.md) | S   | N        |
| Funzionalità\_         | [Identificatore](identifier.md) | N   | N        |
| Manifesto del \_ file    | [Identificatore](identifier.md) | N   | S        |
| Applicazione \_ file | [Identificatore](identifier.md) | N   | S        |
| Attributi        | [Integer](integer.md)       | N   | S        |



 

## <a name="columns"></a>Colonne

<dl> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Componente\_
</dt> <dd>

Chiave nella tabella dei [componenti che](component-table.md) specifica il componente Windows Installer che contiene l'assembly.

Il valore in questo campo non deve essere impostato su Null. Il campo KeyPath del componente nella [tabella dei componenti](component-table.md) non deve essere Null.

Per gli assembly Win32, il componente KeyPath non può essere il file manifesto specificato in Manifesto \_ file. Il manifesto può essere il percorso della chiave per un .NET Framework o un assembly di criteri.

</dd> <dt>

<span id="Feature_"></span><span id="feature_"></span><span id="FEATURE_"></span>Funzionalità\_
</dt> <dd>

Chiave nella tabella [delle funzionalità.](feature-table.md)

Quando l'assembly deve essere installato da un'installazione della funzionalità, Windows programma di installazione installa la funzionalità a cui fa riferimento questo campo.

</dd> <dt>

<span id="File_Manifest"></span><span id="file_manifest"></span><span id="FILE_MANIFEST"></span>Manifesto del \_ file
</dt> <dd>

Chiave esterna nella tabella [file che](file-table.md) specifica il file che contiene il manifesto per un assembly .NET Framework assembly Win32.

Per un assembly Win32, non specificare questo file come file di percorso della chiave del componente nel campo KeyPath di [Component Table](component-table.md).

</dd> <dt>

<span id="File_Application"></span><span id="file_application"></span><span id="FILE_APPLICATION"></span>Applicazione \_ file
</dt> <dd>

Per installare l'assembly in un percorso privato, immettere il file di percorso della chiave per il componente dell'assembly in questo campo.

Si tratta del valore visualizzato nel campo KeyPath della [tabella dei componenti.](component-table.md) Il programma di installazione può quindi installare l'assembly nella struttura di directory del componente specificato nella [tabella di directory](directory-table.md). Questo campo deve essere Null se l'assembly deve essere installato nella Global Assembly Cache.

</dd> <dt>

<span id="Attributes"></span><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributi
</dt> <dd>

Immettere il valore 1 (uno) per un assembly Win32. Immettere il valore 0 (zero) per un assembly .NET Framework assembly.

Se la colonna Attributi è NULL, il programma di installazione considera l'assembly come .NET Framework assembly.

</dd> </dl>

## <a name="remarks"></a>Commenti

Se è presente almeno una voce nella tabella MsiAssembly, la tabella [InstallExecuteSequence](installexecutesequence-table.md) deve contenere l'azione [MsiPublishAssemblies](msipublishassemblies-action.md)e [l'azione MsiUnpublishAssemblies](msiunpublishassemblies-action.md).

Poiché non è possibile eseguire il rollback degli assembly dopo il commit, Windows programma di installazione usa un processo di installazione in due passaggi. Le interfacce per gli assembly vengono create durante le operazioni di installazione generate [dall'azione MsiPublishAssemblies](msipublishassemblies-action.md).

Non viene eseguito il commit degli assembly fino alla corretta esecuzione [dell'azione InstallFinalize](installfinalize-action.md). Ciò significa che se si crea un'azione personalizzata o una risorsa basata sull'assembly, è necessario sequenziarla dopo [l'azione InstallFinalize](installfinalize-action.md). Ad esempio, se è necessario avviare un servizio che dipende da un assembly nella Global Assembly Cache (GAC), è necessario pianificare l'avvio del servizio dopo [l'azione InstallFinalize](installfinalize-action.md). Ciò significa che non è possibile usare la tabella [ServiceControl](servicecontrol-table.md) per avviare il servizio, ma è necessario usare un'azione personalizzata sequenziata dopo InstallFinalize.

## <a name="validation"></a>Convalida

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
[ICE66](ice66.md)  
[ICE83](ice83.md)  
[ICE94](ice94.md)  
</dl>

 

 

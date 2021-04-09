---
description: La tabella MsiAssembly specifica le impostazioni Windows Installer per gli assembly Microsoft .NET Framework e gli assembly Win32. Per ulteriori informazioni, vedere installazione di assembly nella global assembly cache e installazione di assembly Win32.
ms.assetid: 3a8cd206-0112-4840-8c9d-773483f5c771
title: Tabella MsiAssembly
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b54bd6e58e2ff6d12c582309c23856a7bb825b2d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968587"
---
# <a name="msiassembly-table"></a>Tabella MsiAssembly

La tabella MsiAssembly specifica le impostazioni Windows Installer per gli assembly Microsoft .NET Framework e gli assembly Win32. Per ulteriori informazioni, vedere [installazione di assembly nella global assembly cache](installation-of-assemblies-to-the-global-assembly-cache.md) e [installazione di assembly Win32](installation-of-win32-assemblies.md).

In Windows XP Windows Installer possibile installare assembly Win32 come [assembly side-by-side](side-by-side-assemblies.md). Per ulteriori informazioni, vedere l' [API assembly side-by-side](../sbscs/side-by-side-assembly-api.md).

**Windows 2000:** Questa funzionalità non è supportata.

La tabella MsiAssembly include le colonne seguenti.



| Colonna            | Tipo                         | Chiave | Nullable |
|-------------------|------------------------------|-----|----------|
| Componente\_       | [Identificatore](identifier.md) | S   | N        |
| Funzionalità\_         | [Identificatore](identifier.md) | N   | N        |
| \_Manifesto file    | [Identificatore](identifier.md) | N   | S        |
| \_Applicazione file | [Identificatore](identifier.md) | N   | S        |
| Attributi        | [Integer](integer.md)       | N   | S        |



 

## <a name="columns"></a>Colonne

<dl> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Componente\_
</dt> <dd>

Chiave nella tabella dei [componenti](component-table.md) che specifica il componente Windows Installer che contiene l'assembly.

Il valore in questo campo non deve essere impostato su null. Il campo del percorso di un componente della [tabella dei componenti](component-table.md) non può essere null.

Per gli assembly Win32, il percorso di un componente non può essere il file manifesto specificato nel file \_ manifesto. Il manifesto può essere il percorso di un .NET Framework o un assembly dei criteri.

</dd> <dt>

<span id="Feature_"></span><span id="feature_"></span><span id="FEATURE_"></span>Funzionalità\_
</dt> <dd>

Chiave nella [tabella delle funzionalità](feature-table.md).

Quando l'assembly deve essere installato da un'installazione di funzionalità, Windows Installer installa la funzionalità a cui fa riferimento questo campo.

</dd> <dt>

<span id="File_Manifest"></span><span id="file_manifest"></span><span id="FILE_MANIFEST"></span>\_Manifesto file
</dt> <dd>

Chiave esterna nella [tabella file](file-table.md) che specifica il file che contiene il manifesto per un assembly .NET Framework o un assembly Win32.

Per un assembly Win32, non specificare questo file come file del percorso della chiave del componente nel campo percorso chiave della [tabella dei componenti](component-table.md).

</dd> <dt>

<span id="File_Application"></span><span id="file_application"></span><span id="FILE_APPLICATION"></span>\_Applicazione file
</dt> <dd>

Per installare l'assembly in un percorso privato, immettere il file del percorso della chiave per il componente assembly in questo campo.

Si tratta del valore visualizzato nel campo del percorso della [tabella dei componenti](component-table.md). Il programma di installazione può quindi installare l'assembly nella struttura di directory del componente specificato nella [tabella directory](directory-table.md). Questo campo deve essere null se l'assembly deve essere installato nel Global Assembly Cache.

</dd> <dt>

<span id="Attributes"></span><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributi
</dt> <dd>

Immettere un valore 1 (uno) per un assembly Win32. Immettere un valore pari a 0 (zero) per un assembly .NET Framework.

Se la colonna Attributes è NULL, il programma di installazione considera l'assembly come un assembly .NET Framework.

</dd> </dl>

## <a name="remarks"></a>Commenti

Se è presente almeno una voce nella tabella MsiAssembly, la [tabella InstallExecuteSequence](installexecutesequence-table.md) deve contenere l' [azione MsiPublishAssemblies](msipublishassemblies-action.md)e l' [azione MsiUnpublishAssemblies](msiunpublishassemblies-action.md).

Poiché non è possibile eseguire il rollback degli assembly dopo che ne è stato eseguito il commit, Windows Installer utilizza un processo di installazione in due passaggi. Le interfacce per gli assembly vengono create durante le operazioni di installazione generate dall' [azione MsiPublishAssemblies](msipublishassemblies-action.md).

Il commit degli assembly non viene eseguito fino al completamento dell'esecuzione dell' [azione InstallFinalize](installfinalize-action.md). Ciò significa che se si crea un'azione personalizzata o una risorsa che si basa sull'assembly, è necessario sequenziarla dopo l' [azione InstallFinalize](installfinalize-action.md). Se, ad esempio, è necessario avviare un servizio che dipende da un assembly nella global assembly cache (GAC), è necessario pianificare l'avvio di tale servizio dopo l' [azione InstallFinalize](installfinalize-action.md). Ciò significa che non è possibile utilizzare la [tabella ServiceControl](servicecontrol-table.md) per avviare il servizio, ma è necessario utilizzare un'azione personalizzata sequenziata dopo InstallFinalize.

## <a name="validation"></a>Convalida

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
[ICE66](ice66.md)  
[ICE83](ice83.md)  
[ICE94](ice94.md)  
</dl>

 

 

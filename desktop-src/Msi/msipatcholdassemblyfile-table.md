---
description: La tabella MsiPatchOldAssemblyFile correla un file nella tabella file con un nome di assembly nella tabella MsiPatchOldAssemblyName. È possibile associare più nomi di assembly precedenti a un singolo file.
ms.assetid: a3c1e7fb-5f97-41db-bdc8-bd3ddb695c42
title: Tabella MsiPatchOldAssemblyFile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c995e4f6d6622dd3d7d1c96c9ef1297a787b66d6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319006"
---
# <a name="msipatcholdassemblyfile-table"></a>Tabella MsiPatchOldAssemblyFile

La tabella MsiPatchOldAssemblyFile correla un file nella tabella [file](file-table.md) con un nome di assembly nella [tabella MsiPatchOldAssemblyName](msipatcholdassemblyname-table.md). È possibile associare più nomi di assembly precedenti a un singolo file.

La tabella MsiPatchOldAssemblyFile include le colonne seguenti.



| Colonna     | Tipo                         | Chiave | Nullable |
|------------|------------------------------|-----|----------|
| file\_     | [Identificatore](identifier.md) | S   | N        |
| Assembly\_ | [Identificatore](identifier.md) | S   | N        |



 

## <a name="columns"></a>Colonne

<dl> <dt>

<span id="File_"></span><span id="file_"></span><span id="FILE_"></span>File\_
</dt> <dd>

Chiave esterna per la [tabella file](file-table.md) che specifica l'assembly di cui applicare la patch. Questa colonna fa parte della chiave primaria.

</dd> <dt>

<span id="Assembly_"></span><span id="assembly_"></span><span id="ASSEMBLY_"></span>Assembly\_
</dt> <dd>

Chiave esterna per la [tabella MsiPatchOldAssemblyName](msipatcholdassemblyname-table.md) che identifica uno dei nomi degli assembly precedenti per l'assembly. Questa colonna fa parte della chiave primaria.

</dd> </dl>

## <a name="remarks"></a>Commenti

Windows Installer utilizza la tabella MsiPatchOldAssemblyFile e la [tabella MsiPatchOldAssemblyName](msipatcholdassemblyname-table.md) durante l'applicazione di patch agli assembly installati nella global assembly cache (GAC). Quando si rilascia una versione più recente di un assembly, il nome sicuro dell'assembly viene modificato. Le due tabelle identificano il nome dell'assembly precedente per un assembly aggiornato. Ciò consente al programma di installazione di utilizzare il nome dell'assembly precedente per trovare il file originale nella GAC e applicare una patch binaria. Senza queste informazioni, il programma di installazione potrebbe dover accedere all'origine di installazione originale per applicare la patch a un assembly installato nella GAC.

La tabella MsiPatchOldAssemblyFile e la [tabella MsiPatchOldAssemblyName](msipatcholdassemblyname-table.md) non vengono generate automaticamente da [Patchwiz](patchwiz-dll.md). Il pacchetto di aggiornamento specificato nella [tabella UpgradedImages](upgradedimages-table-patchwiz-dll-.md) deve contenere le tabelle per la patch in modo che dispongano di queste informazioni.

## <a name="validation"></a>Convalida

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
</dl>

 

 




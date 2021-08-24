---
description: La tabella MsiPatchOldAssemblyFile mette in relazione un file nella tabella File con un nome di assembly nella tabella MsiPatchOldAssemblyName. È possibile associare più nomi di assembly vecchi a un singolo file.
ms.assetid: a3c1e7fb-5f97-41db-bdc8-bd3ddb695c42
title: Tabella MsiPatchOldAssemblyFile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4570b862773d2dc1d5b9c7458dbc1ccd8825ce77bf504d5e0fb2bf116d7a095
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119559081"
---
# <a name="msipatcholdassemblyfile-table"></a>Tabella MsiPatchOldAssemblyFile

La tabella MsiPatchOldAssemblyFile mette in relazione un file nella tabella [File](file-table.md) con un nome di assembly nella tabella [MsiPatchOldAssemblyName](msipatcholdassemblyname-table.md). È possibile associare più nomi di assembly vecchi a un singolo file.

La tabella MsiPatchOldAssemblyFile contiene le colonne seguenti.



| Colonna     | Tipo                         | Chiave | Nullable |
|------------|------------------------------|-----|----------|
| file\_     | [Identificatore](identifier.md) | S   | N        |
| Assembly\_ | [Identificatore](identifier.md) | S   | N        |



 

## <a name="columns"></a>Colonne

<dl> <dt>

<span id="File_"></span><span id="file_"></span><span id="FILE_"></span>File\_
</dt> <dd>

Chiave esterna della tabella [File che](file-table.md) specifica l'assembly a cui applicare patch. Questa colonna fa parte della chiave primaria.

</dd> <dt>

<span id="Assembly_"></span><span id="assembly_"></span><span id="ASSEMBLY_"></span>Assemblea\_
</dt> <dd>

Chiave esterna della tabella [MsiPatchOldAssemblyName che](msipatcholdassemblyname-table.md) identifica uno dei nomi di assembly precedente per l'assembly. Questa colonna fa parte della chiave primaria.

</dd> </dl>

## <a name="remarks"></a>Commenti

Windows Il programma di installazione usa la tabella MsiPatchOldAssemblyFile e la tabella [MsiPatchOldAssemblyName durante](msipatcholdassemblyname-table.md) l'applicazione di patch agli assembly installati nella Global Assembly Cache (GAC). Quando si rilascia una versione più recente di un assembly, il nome sicuro dell'assembly viene modificato. Le due tabelle identificano insieme il nome dell'assembly precedente per un assembly aggiornato. In questo modo il programma di installazione può usare il nome dell'assembly precedente per trovare il file originale nella GAC e applicare una patch binaria. Senza queste informazioni, il programma di installazione potrebbe dover accedere all'origine dell'installazione originale per applicare patch a un assembly installato nella GAC.

La tabella MsiPatchOldAssemblyFile e la tabella [MsiPatchOldAssemblyName](msipatcholdassemblyname-table.md) non vengono generate automaticamente da [PatchWiz.](patchwiz-dll.md) Il pacchetto di aggiornamento specificato nella [tabella UpgradedImages](upgradedimages-table-patchwiz-dll-.md) deve contenere queste tabelle perché la patch contenga queste informazioni.

## <a name="validation"></a>Convalida

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
</dl>

 

 




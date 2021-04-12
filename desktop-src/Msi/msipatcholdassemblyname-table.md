---
description: La tabella MsiPatchOldAssemblyName specifica il nome precedente di un assembly.
ms.assetid: e9f22ba1-6be4-4382-abe5-5cfdc68c0855
title: Tabella MsiPatchOldAssemblyName
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee301801efc1618f84794c48172aff47734b38d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104347346"
---
# <a name="msipatcholdassemblyname-table"></a>Tabella MsiPatchOldAssemblyName

La tabella MsiPatchOldAssemblyName specifica il nome precedente di un assembly.

La tabella MsiPatchOldAssemblyName include le colonne seguenti.



| Colonna   | Tipo                         | Chiave | Nullable |
|----------|------------------------------|-----|----------|
| Assembly | [Identificatore](identifier.md) | S   | N        |
| Nome     | [Text](text.md)             | S   | N        |
| Valore    | [Text](text.md)             | N   | N        |



 

## <a name="columns"></a>Colonne

<dl> <dt>

<span id="Assembly"></span><span id="assembly"></span><span id="ASSEMBLY"></span>Assembly
</dt> <dd>

Identificatore univoco per il vecchio nome dell'assembly. Questa chiave viene utilizzata come mapping tra questa e la [tabella MsiPatchOldAssemblyFile](msipatcholdassemblyfile-table.md).

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

Windows Installer utilizza la tabella [MsiPatchOldAssemblyFile](msipatcholdassemblyfile-table.md) e la tabella MsiPatchOldAssemblyName durante l'applicazione di patch agli assembly installati nella global assembly cache (GAC). Quando si rilascia una versione più recente di un assembly, il nome sicuro dell'assembly viene modificato. Le due tabelle identificano il nome dell'assembly precedente per un assembly aggiornato. Ciò consente al programma di installazione di utilizzare il nome dell'assembly precedente per trovare il file originale nella GAC e applicare una patch binaria. Senza queste informazioni, il programma di installazione potrebbe dover accedere all'origine di installazione originale per applicare la patch a un assembly installato nella GAC.

La [tabella MsiPatchOldAssemblyFile](msipatcholdassemblyfile-table.md) e la tabella MsiPatchOldAssemblyName non vengono generate automaticamente da [Patchwiz](patchwiz-dll.md). Il pacchetto di aggiornamento specificato nella [tabella UpgradedImages](upgradedimages-table-patchwiz-dll-.md) deve contenere le tabelle per la patch in modo che dispongano di queste informazioni.

## <a name="validation"></a>Convalida

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
</dl>

 

 




---
description: La tabella UpgradedFilesToIgnore impedisce l'aggiornamento di file specifici che sono in effetti modificati nell'immagine aggiornata rispetto alle immagini di destinazione.
ms.assetid: 3b5f4360-887a-4a21-8f16-faa84da34328
title: Tabella UpgradedFilesToIgnore (Patchwiz.dll)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f4a235759251ac3dadbe01b030c0d984d1f66b9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318272"
---
# <a name="upgradedfilestoignore-table-patchwizdll"></a>Tabella UpgradedFilesToIgnore (Patchwiz.dll)

La tabella UpgradedFilesToIgnore impedisce l'aggiornamento di file specifici che sono in effetti modificati nell'immagine aggiornata rispetto alle immagini di destinazione. In alcuni casi può essere utile eseguire questa operazione. Ad esempio, un pacchetto di patch progettato solo per l'utilizzo con installazioni non amministrative non deve includere file di patch che fanno parte solo di immagini amministrative. Escludendo tali file utilizzati solo nelle immagini amministrative è possibile ridurre le dimensioni del pacchetto di patch. Tuttavia, gli amministratori devono essere informati su come aggiornare i file separatamente. Questa tabella è facoltativa nel database di creazione della patch (file con estensione PCP) e viene usata dalla funzione [UiCreatePatchPackageEx](uicreatepatchpackageex--patchwiz-dll-.md) .

La tabella UpgradedFilesToIgnore include le colonne seguenti.



| Colonna   | Tipo | Chiave | Nullable |
|----------|------|-----|----------|
| Aggiornato | text | S   | N        |
| FTK      | text | S   | N        |



 

## <a name="columns"></a>Colonne

<dl> <dt>

<span id="Upgraded"></span><span id="upgraded"></span><span id="UPGRADED"></span>Aggiornato
</dt> <dd>

Chiave esterna per la colonna aggiornata della [tabella UpgradedImages (Patchwiz.dll)](upgradedimages-table-patchwiz-dll-.md). Lo strumento di creazione della patch esclude l'aggiornamento del file specificato nella colonna FTK della tabella UpgradedFilesToIgnore durante l'aggiornamento di una destinazione all'immagine specificata nel campo aggiornato. Immettere il valore " \* " nel campo aggiornato per escludere l'aggiornamento del file per tutte le immagini aggiornate.

</dd> <dt>

<span id="FTK"></span><span id="ftk"></span>FTK
</dt> <dd>

Chiave esterna nella [tabella file](file-table.md) dell'immagine aggiornata. Un valore nel formato " <prefix> \* " corrisponde a tutte le chiavi della tabella file nella tabella file che iniziano con tale prefisso. Nessun testo può seguire l'asterisco.

</dd> </dl>

 

 




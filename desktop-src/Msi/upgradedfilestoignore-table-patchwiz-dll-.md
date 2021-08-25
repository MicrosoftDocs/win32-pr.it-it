---
description: La tabella UpgradedFilesToIgnore impedisce l'aggiornamento di file specifici che vengono modificati nell'immagine aggiornata rispetto alle immagini di destinazione.
ms.assetid: 3b5f4360-887a-4a21-8f16-faa84da34328
title: Tabella UpgradedFilesToIgnore (Patchwiz.dll)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f51143fcf7db350d5ee8aa1e43d49984914bcf9f05a2f8f5f787834a69b7e1a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119809551"
---
# <a name="upgradedfilestoignore-table-patchwizdll"></a>Tabella UpgradedFilesToIgnore (Patchwiz.dll)

La tabella UpgradedFilesToIgnore impedisce l'aggiornamento di file specifici che vengono modificati nell'immagine aggiornata rispetto alle immagini di destinazione. Può essere utile eseguire questa operazione in determinati casi. Ad esempio, un pacchetto di patch destinato solo all'uso con installazioni non amministrative non deve includere file di patch che fanno solo parte di immagini amministrative. L'esclusione di tali file usati solo nelle immagini amministrative può ridurre le dimensioni del pacchetto patch. Tuttavia, gli amministratori devono essere informati su come aggiornare questi file separatamente. Questa tabella è facoltativa nel database di creazione delle patch (file con estensione pcp) e viene usata dalla [funzione UiCreatePatchPackageEx.](uicreatepatchpackageex--patchwiz-dll-.md)

La tabella UpgradedFilesToIgnore include le colonne seguenti.



| Colonna   | Tipo | Chiave | Nullable |
|----------|------|-----|----------|
| Aggiornato | text | S   | N        |
| FTK      | text | S   | N        |



 

## <a name="columns"></a>Colonne

<dl> <dt>

<span id="Upgraded"></span><span id="upgraded"></span><span id="UPGRADED"></span>Aggiornato
</dt> <dd>

Chiave esterna per la colonna Aggiornato della [tabella UpgradedImages (Patchwiz.dll)](upgradedimages-table-patchwiz-dll-.md). Lo strumento di creazione patch esclude l'aggiornamento del file specificato nella colonna FTK della tabella UpgradedFilesToIgnore quando si aggiorna una destinazione all'immagine specificata nel campo Aggiornato. Immettere il valore " " nel campo Aggiornato per escludere \* l'aggiornamento del file per tutte le immagini aggiornate.

</dd> <dt>

<span id="FTK"></span><span id="ftk"></span>FTK
</dt> <dd>

Chiave esterna nella tabella [File dell'immagine](file-table.md) aggiornata. Un valore nel formato " " corrisponde a tutte le chiavi della tabella <prefix> \* file nella tabella File che iniziano con tale prefisso. Nessun testo può seguire l'asterisco.

</dd> </dl>

 

 




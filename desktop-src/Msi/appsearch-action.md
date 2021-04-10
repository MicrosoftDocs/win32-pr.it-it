---
description: L'azione AppSearch usa le firme file per cercare le versioni esistenti dei prodotti.
ms.assetid: 56665876-2c74-476b-aa1a-158c6e86418d
title: Azione AppSearch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04187fb146af80839e135c99986dea1902ccb6b9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104227212"
---
# <a name="appsearch-action"></a>Azione AppSearch

L'azione AppSearch usa le firme file per cercare le versioni esistenti dei prodotti. L'azione AppSearch può utilizzare queste informazioni per determinare la posizione in cui installare gli aggiornamenti. L'azione AppSearch può essere utilizzata anche per impostare una proprietà sul valore esistente di una voce del registro di sistema o di un file ini.

## <a name="sequence-restrictions"></a>Restrizioni sequenza

AppSearch deve essere creato nella [tabella InstallUISequence](installuisequence-table.md) e nella [tabella InstallExecuteSequence](installexecutesequence-table.md). Il programma di installazione impedisce l'esecuzione dell'azione AppSearch nella sequenza InstallExecuteSequence se l'azione è già stata eseguita nella sequenza InstallUISequence.

## <a name="actiondata-messages"></a>Messaggi ActionData



| Campo | Descrizione dei dati dell'azione      |
|-------|---------------------------------|
| \[1\] | Proprietà che contiene il percorso del file. |
| \[2\] | Firma del file.                 |



 

## <a name="remarks"></a>Commenti

Per l'azione AppSearch è necessario che la tabella [Signature](signature-table.md) sia presente nel pacchetto di installazione. Le firme dei file sono elencate nella tabella della firma. Una firma che non è presente nella tabella delle firme indica una directory e l'azione imposta la proprietà sul percorso di directory per la firma.

L'azione AppSearch Cerca le firme dei file usando prima la tabella [CompLocator](complocator-table.md) , la tabella [RegLocator](reglocator-table.md) avanti, quindi la tabella [IniLocator](inilocator-table.md) e infine la tabella [DrLocator](drlocator-table.md) .

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[AppSearch](appsearch-table.md)
</dt> <dt>

[CompLocator](complocator-table.md)
</dt> <dt>

[IniLocator](inilocator-table.md)
</dt> <dt>

[RegLocator](reglocator-table.md)
</dt> <dt>

[DrLocator](drlocator-table.md)
</dt> </dl>

 

 




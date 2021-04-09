---
description: ICEM14 convalida la colonna valore della tabella ModuleSubstitution.
ms.assetid: e07ba63a-e748-4835-ae1b-9f7d30e46d39
title: ICEM14
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72223f27338fb08efe4ea95b817acebd6234063f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130447"
---
# <a name="icem14"></a>ICEM14

ICEM14 convalida la colonna valore della [tabella ModuleSubstitution](modulesubstitution-table.md).

## <a name="result"></a>Risultato

ICEM14 invia i seguenti errori.



| Errore                                                                                                                                                         | Significato                                                                                                                                                                                                                                                                                                                                              |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Stringa di sostituzione nella colonna ModuleSubstitution. Value nella riga \[ 1 \] . \[ 2 \] . \[ 3 \] non è stato trovato nella tabella ModuleConfiguration.                                 | \[1 \] . \[ 2 \] . \[ 3 \] fa riferimento a una chiave primaria *Table. Row. Column* per una riga nella tabella ModuleSubstitution. Il modello di formattazione nel campo valore di questa riga non corrisponde a una riga di attributi configurabili nella [tabella ModuleConfiguration](moduleconfiguration-table.md).                                                            |
| Nella tabella ModuleSubstitution nella riga \[ 1 \] . \[ 2 \] . \[ 3 \] , nella tabella '% s'è indicato un elemento configurabile. La tabella '% s'non deve contenere elementi configurabili. | Una delle tabelle seguenti è elencata nella colonna della tabella della tabella ModuleSubstitution: [ModuleSubstitution](modulesubstitution-table.md), [ModuleConfiguration](moduleconfiguration-table.md), [ModuleExclusion](moduleexclusion-table.md)o [ModuleSignature](modulesignature-table.md). Queste tabelle non possono contenere campi configurabili. |
| Nella tabella ModuleSubstitution nella riga \[ 1 \] . \[ 2 \] . \[ 3 \] , viene specificata una stringa di sostituzione vuota.                                                               | Il modello di formattazione nel campo valore di questa riga non corrisponde a una riga di attributi configurabili nella [tabella ModuleConfiguration](moduleconfiguration-table.md).                                                                                                                                                                    |



 

ICEM14 invia il seguente avviso.



| Avviso                                                                  | Significato                                  |
|--------------------------------------------------------------------------|------------------------------------------|
| La tabella ModuleSubstitution esiste ma manca la tabella ModuleConfiguration | La tabella ModuleConfiguration è assente. |



 

## <a name="table-used-during-execution"></a>Tabella utilizzata durante l'esecuzione

[Tabella ModuleSubstitution](modulesubstitution-table.md)

[Tabella ModuleConfiguration](moduleconfiguration-table.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Riferimento ghiaccio del modulo merge](merge-module-ice-reference.md)
</dt> </dl>

 

 




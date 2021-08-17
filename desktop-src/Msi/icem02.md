---
description: ICEM02 verifica che tutte le dipendenze e le esclusioni del modulo siano correlate al modulo corrente.
ms.assetid: c7d77cb6-0ee6-4857-a749-7908e1c5fcda
title: ICEM02
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 332ad83ba753984d752a78bebc19bc17e3b5d25ef8b580f9f105a9577d016318
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119430821"
---
# <a name="icem02"></a>ICEM02

ICEM02 verifica che tutte le dipendenze e le esclusioni del modulo siano correlate al modulo corrente.

Gli ICE del modulo unione vengono archiviati in un file CUB del modulo merge denominato Mergemod.cub e non nel file con estensione cub contenente gli ICO usati per la convalida dei pacchetti.

## <a name="result"></a>Risultato

ICEM02 invia messaggi di errore se il database del modulo tenta di specificare dipendenze o esclusioni non correlate al modulo corrente. ICEM02 invia un messaggio di errore se il database del modulo tenta di specificare il modulo corrente come dipendente o come escluso da se stesso.

## <a name="example"></a>Esempio

ICEM02 pubblica i messaggi di errore seguenti per un modulo contenente le voci di database illustrate di seguito.

``` syntax
The dependency OtherModule.GUID2.1033.OtherModule.GUID3.0 in the 
ModuleDependency table creates a dependency for an unrelated module. A 
module can only define dependencies for itself

This module is listed as depending on itself!

The exclusion OtherModule.GUID2.1033.OtherModule.GUID3.0 in the 
ModuleExclusion table creates an excluded module for an unrelated 
module. A module can only define exclusions for itself.

This module excludes itself from the target database!
```

[Tabella ModuleSignature](modulesignature-table.md)



| ModuleID         | Lingua | Versione |
|------------------|----------|---------|
| MyModule. *GUID1* | 1033     | 1.0     |



 

[Tabella ModuleDependency](moduledependency-table.md)



| ModuleID            | ModuleLanguage | Id obbligatorio          | RequiredLanguage | RequiredVersion |
|---------------------|----------------|---------------------|------------------|-----------------|
| OtherModule. *GUID2* | 1033           | OtherModule. *GUID3* | 0                | 1.0             |
| MyModule. *GUID1*    | 1033           | MyModule. *GUID1*    | 1033             | 1.2             |



 

[Tabella ModuleExclusion](moduleexclusion-table.md) (parziale)



| ModuleID            | ModuleLanguage | ExcludedID          | Lingua esclusa |
|---------------------|----------------|---------------------|------------------|
| OtherModule. *GUID2* | 1033           | OtherModule. *GUID3* | 0                |
| MyModule. *GUID1*    | 1033           | MyModule. *GUID1*    | 1033             |



 

Il modulo di merge ICE pubblica il primo errore perché della prima riga della tabella ModuleDependency, che non specifica una dipendenza necessaria per il modulo corrente specificato nella tabella ModuleSignature. Le dipendenze di un modulo possono essere specificate solo nella propria tabella ModuleDependency. Se OtherModule. *GUID3* è richiesto dal modulo corrente. Sostituire le prime due colonne della riga con i dati della tabella ModuleSignature. Se OtherModule. *GUID3* non è richiesto da questo modulo. Eliminare questa riga.

Il modulo unione ICE pubblica il secondo errore perché un modulo non può specificare una dipendenza su se stesso.

Il modulo unione ICE pubblica il terzo errore a causa della prima riga nella tabella ModuleExclusion, che non specifica un'esclusione obbligatoria per il modulo corrente specificato nella tabella ModuleSignature. Le esclusioni di un modulo possono essere specificate solo nella relativa tabella ModuleExclusion. Se il modulo corrente esclude OtherModule. *GUID3*, sostituire le prime due colonne della riga con i dati della tabella ModuleSignature. Se il modulo corrente non esclude OtherModule. *GUID3*, eliminare questa riga.

Il modulo di merge ICE pubblica il quarto errore perché un modulo non può specificare di escludersi.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni di riferimento su ICE del modulo merge](merge-module-ice-reference.md)
</dt> </dl>

 

 




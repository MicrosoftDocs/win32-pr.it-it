---
description: ICEM02 verifica che tutte le dipendenze ed esclusioni dei moduli siano correlate al modulo corrente.
ms.assetid: c7d77cb6-0ee6-4857-a749-7908e1c5fcda
title: ICEM02
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9a976132dbfad42e95f4141bc00adb48a544c1b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226448"
---
# <a name="icem02"></a>ICEM02

ICEM02 verifica che tutte le dipendenze ed esclusioni dei moduli siano correlate al modulo corrente.

I moduli CIEM di tipo merge vengono archiviati in un file con estensione cub del modulo merge denominato Mergemod. cub e non nel file con estensione cub contenente i ghiacci utilizzati per la convalida del pacchetto.

## <a name="result"></a>Risultato

ICEM02 invia messaggi di errore se il database del modulo tenta di specificare dipendenze o esclusioni che non sono correlate al modulo corrente. ICEM02 Invia un messaggio di errore se il database del modulo tenta di specificare il modulo corrente come dipendente o escluso da solo.

## <a name="example"></a>Esempio

ICEM02 invierà i messaggi di errore seguenti per un modulo contenente le voci di database indicate di seguito.

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



| ModuleID         | Linguaggio | Versione |
|------------------|----------|---------|
| MyModule. *Guid1* | 1033     | 1.0     |



 

[Tabella ModuleDependency](moduledependency-table.md)



| ModuleID            | ModuleLanguage | RequiredID          | RequiredLanguage | RequiredVersion |
|---------------------|----------------|---------------------|------------------|-----------------|
| OtherModule. *Guid2* | 1033           | OtherModule. *GUID3* | 0                | 1.0             |
| MyModule. *Guid1*    | 1033           | MyModule. *Guid1*    | 1033             | 1.2             |



 

[Tabella ModuleExclusion](moduleexclusion-table.md) (parziale)



| ModuleID            | ModuleLanguage | ExcludedID          | ExcludedLanguage |
|---------------------|----------------|---------------------|------------------|
| OtherModule. *Guid2* | 1033           | OtherModule. *GUID3* | 0                |
| MyModule. *Guid1*    | 1033           | MyModule. *Guid1*    | 1033             |



 

Il modulo merge ICE registra il primo errore perché la della prima riga nella tabella ModuleDependency, che non specifica una dipendenza obbligatoria per il modulo corrente specificato nella tabella ModuleSignature. Le dipendenze di un modulo possono essere specificate solo nella propria tabella ModuleDependency. Se OtherModule. *GUID3* è richiesto dal modulo corrente, sostituire le prime due colonne della riga con i dati della tabella ModuleSignature. Se OtherModule. *GUID3* non è richiesto da questo modulo, eliminare questa riga.

Il modulo merge ICE registra il secondo errore perché un modulo non può specificare una dipendenza su se stesso.

Il modulo merge ICE inserisce il terzo errore a causa della prima riga nella tabella ModuleExclusion, che non specifica un'esclusione obbligatoria per il modulo corrente specificato nella tabella ModuleSignature. Le esclusioni di un modulo possono essere specificate solo nella propria tabella ModuleExclusion. Se il modulo corrente esclude OtherModule. *GUID3*, sostituire le prime due colonne della riga con i dati della tabella ModuleSignature. Se il modulo corrente non esclude OtherModule. *GUID3*, eliminare questa riga.

Il modulo merge ICE inserisce il quarto errore perché un modulo non è in grado di specificare che escluda se stesso.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Riferimento ghiaccio del modulo merge](merge-module-ice-reference.md)
</dt> </dl>

 

 




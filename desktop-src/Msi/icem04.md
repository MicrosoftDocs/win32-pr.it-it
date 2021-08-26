---
description: ICEM04 verifica che le tabelle vuote necessarie del modulo di merge siano vuote. La mancata correzione di un errore restituito da ICEM04 può causare un'unione non corretta del modulo di unione.
ms.assetid: c6f64f5e-be65-485b-8831-e377535bd335
title: ICEM04
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8388cbccd576b89a70716dd7c2ca6c82ac49fb30c8c39776904753de00b68dba
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120050161"
---
# <a name="icem04"></a>ICEM04

ICEM04 verifica che le tabelle vuote necessarie del modulo di merge siano vuote. La mancata correzione di un errore restituito da ICEM04 può causare un'unione non corretta del modulo di unione.

## <a name="result"></a>Risultato

ICEM04 invia un errore quando le tabelle vuote obbligatorie del modulo di merge non sono vuote.

## <a name="example"></a>Esempio

ICEM04 pubblica i messaggi di errore seguenti per un modulo che contiene le voci di database visualizzate.

``` syntax
An empty FeatureComponents table is required in a Merge Module.

The Merge Module contains the 'ModuleInstallExecuteSequence' table. It 
must therefore have an empty 'InstallExecuteSequence' table.

Action 'CostInitialize' found in the AdvtExecuteSequence table. This 
table must be empty in a Merge Module
```

La tabella seguente illustra una tabella [AdvtExecuteSequence parziale.](advtexecutesequence-table.md)



| Azione         | Sequenza |
|----------------|----------|
| CostInitialize | 1        |



 

L'elenco seguente mostra il contenuto parziale di MergeModule:

-   ModuleInstallExecuteSequence
-   ModuleAdvtExecuteSequence
-   InstallUISequence

L'esempio seguente illustra un altro possibile errore.

``` syntax
Feature-Component '[1].[2]' found in the FeatureComponents table. The 
FeatureComponents table must be empty in a Merge Module.
```

Se un modulo di merge contiene una tabella di sequenze di moduli, deve contenere la tabella di sequenze vuota corrispondente, indipendentemente dal fatto che la tabella di sequenza del modulo sia vuota o meno. Ad esempio, se il modulo di merge contiene la tabella [ModuleAdminExecuteSequence](moduleadminexecutesequence-table.md), deve contenere anche una tabella AdminExecuteSequence vuota.

La [tabella FeatureComponents è](featurecomponents-table.md) obbligatoria in tutti i moduli unione e deve essere vuota.

La procedura seguente illustra come correggere gli errori.

**Per correggere gli errori**

1.  Aggiungere una tabella [FeatureComponents vuota](featurecomponents-table.md) al modulo di unione.
2.  Aggiungere una tabella [InstallExecuteSequence vuota](installexecutesequence-table.md) al modulo di merge.
3.  Rimuovere l'azione 'CostInitialize' [dalla tabella AdvtExecuteSequence](advtexecutesequence-table.md).
    > [!Note]  
    > Questa tabella deve essere vuota in un modulo unione. Le azioni devono essere visualizzate solo nella tabella ModuleAdvtExecuteSequence.

     

## <a name="tables-used-during-execution"></a>Tabelle utilizzate durante l'esecuzione

Nell'elenco seguente vengono identificate le tabelle utilizzate durante l'esecuzione:

-   [Tabella FeatureComponents](featurecomponents-table.md)
-   Tabelle \* Module Sequence e tabelle Sequence \* corrispondenti.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni sui moduli unione](about-merge-modules.md)
</dt> <dt>

[Informazioni di riferimento su ICE del modulo merge](merge-module-ice-reference.md)
</dt> </dl>

 

 




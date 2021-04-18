---
description: ICEM04 verifica che le tabelle vuote obbligatorie del modulo merge siano vuote. Impossibile correggere un errore per il quale i report di ICEM04 possono causare un merge errato del modulo merge.
ms.assetid: c6f64f5e-be65-485b-8831-e377535bd335
title: ICEM04
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2ef993690ae690e0651db1538196998c4dd28c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308686"
---
# <a name="icem04"></a>ICEM04

ICEM04 verifica che le tabelle vuote obbligatorie del modulo merge siano vuote. Impossibile correggere un errore per il quale i report di ICEM04 possono causare un merge errato del modulo merge.

## <a name="result"></a>Risultato

ICEM04 Invia un errore quando le tabelle vuote richieste del modulo merge non sono vuote.

## <a name="example"></a>Esempio

ICEM04 invia i messaggi di errore seguenti per un modulo che contiene le voci di database indicate.

``` syntax
An empty FeatureComponents table is required in a Merge Module.

The Merge Module contains the 'ModuleInstallExecuteSequence' table. It 
must therefore have an empty 'InstallExecuteSequence' table.

Action 'CostInitialize' found in the AdvtExecuteSequence table. This 
table must be empty in a Merge Module
```

Nella tabella seguente viene illustrata una [tabella AdvtExecuteSequence](advtexecutesequence-table.md)parziale.



| Azione         | Sequenza |
|----------------|----------|
| CostInitialize | 1        |



 

Nell'elenco seguente viene illustrato il contenuto parziale di MergeModule:

-   ModuleInstallExecuteSequence
-   ModuleAdvtExecuteSequence
-   InstallUISequence

Nell'esempio seguente viene illustrato un altro errore possibile.

``` syntax
Feature-Component '[1].[2]' found in the FeatureComponents table. The 
FeatureComponents table must be empty in a Merge Module.
```

Se un modulo merge contiene una tabella di sequenza dei moduli, deve contenere la tabella di sequenza vuota corrispondente, indipendentemente dal fatto che la tabella di sequenza dei moduli sia vuota o meno. Se, ad esempio, il modulo merge contiene la [tabella ModuleAdminExecuteSequence](moduleadminexecutesequence-table.md), è necessario che contenga anche una tabella AdminExecuteSequence vuota.

La [tabella FeatureComponents](featurecomponents-table.md) è obbligatoria in tutti i moduli merge e deve essere vuota.

Nella procedura riportata di seguito viene illustrato come correggere gli errori.

**Per correggere gli errori**

1.  Aggiungere una [tabella FeatureComponents](featurecomponents-table.md) vuota al modulo merge.
2.  Aggiungere una [tabella InstallExecuteSequence](installexecutesequence-table.md) vuota al modulo merge.
3.  Rimuovere l'azione ' CostInitialize ' dalla [tabella AdvtExecuteSequence](advtexecutesequence-table.md).
    > [!Note]  
    > Questa tabella deve essere vuota in un modulo merge. Le azioni devono essere visualizzate solo nella tabella ModuleAdvtExecuteSequence.

     

## <a name="tables-used-during-execution"></a>Tabelle utilizzate durante l'esecuzione

Nell'elenco seguente vengono identificate le tabelle utilizzate durante l'esecuzione:

-   [Tabella FeatureComponents](featurecomponents-table.md)
-   \*Tabelle di sequenza del modulo e \* tabelle di sequenza corrispondenti.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni sui moduli merge](about-merge-modules.md)
</dt> <dt>

[Riferimento ghiaccio del modulo merge](merge-module-ice-reference.md)
</dt> </dl>

 

 




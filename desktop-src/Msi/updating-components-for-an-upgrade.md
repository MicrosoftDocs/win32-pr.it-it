---
description: Per impostazione predefinita, gli utenti del prodotto fittizio MNP2000 non devono mai usare file aggiornati, ad esempio Baseba01.txt.
ms.assetid: 5aca7ff5-c09f-4d00-b319-2b89550686ab
title: Aggiornamento dei componenti per un aggiornamento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e725653acc7aadbeb3710d3cd6b1ee6dc2971e51d3583f2be279ddfed008d81
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120039241"
---
# <a name="updating-components-for-an-upgrade"></a>Aggiornamento dei componenti per un aggiornamento

Per impostazione predefinita, gli utenti del prodotto fittizio MNP2000 non devono mai usare file aggiornati, ad esempio Baseba01.txt. Pertanto, i file aggiornati sono per definizione incompatibili con il prodotto originale e i componenti del programma di installazione di Windows, ad esempio Baseball, che contengono questi file devono essere assegnati a nuovi codici componente. I nuovi file, ad esempio Opera01.txt, vengono introdotti come parte di un nuovo componente con un codice componente univoco. Poiché il prodotto originale e l'aggiornamento usano lo stesso Blocco note, il codice del componente di questo componente rimane invariato. Per altre informazioni su quando è necessario modificare il codice del componente, vedere [Modifica del codice del componente.](changing-the-component-code.md)

Usare Orca o un altro editor di database per immettere i dati seguenti nella [tabella Component](component-table.md) di MNP2001.msi. Non riutilizzare i GUID illustrati di seguito nella colonna ComponentId dell'esempio.

[Tabella dei componenti](component-table.md)



| Componente  | Componentid                            | Directory\_ | Attributi | Condition | Percorso chiave      |
|------------|----------------------------------------|-------------|------------|-----------|--------------|
| Baseball   | {2951190A-6AF8-4D7F-AA16-D256405C277A} | SPORTDIR    | 2          |           | Baseba01.txt |
| Basket | {E1AAB6B0-FEC6-4F18-B765-3B05A81CEACB} | SPORTDIR    | 2          |           | Basket01.txt |
| Concerto    | {C28C5064-AA84-4431-AC69-FC1321DF18AF} | DIRDIR     | 2          |           | Concer01.txt |
| Danza      | {1AC2B14D-D5F4-4642-9F7A-EE81BF59B3E2} | DIRDIR     | 2          |           | Dance01.txt  |
| Opera      | {C2DABF7E-1EF6-458D-84B1-AAC1127CED26} | DIRDIR     | 2          |           | Opera01.txt  |
| Calcio   | {92AA30F4-7AC5-4DFA-801E-988CF3DAA4DC} | SPORTDIR    | 2          |           | Footba01.txt |
| Help       | {AD10EB50-33C1-11D3-91D6-00C04FD70856} | NOTEPADDIR  | 2          |           | Help.txt     |
| January    | {E90CD0E6-ED8D-4F88-B000-27BD2B482C6C} | CHER      | 2          |           | Janua01.txt  |
| NewYears   | {1EEF8C53-F7C0-405C-8FE3-2B0FE54B0114} | HOLDIR      | 2          |           | NewYea01.txt |
| memoriale   | {BA81ACF7-4D43-424F-93B0-8845A2DF1C02} | HOLDIR      | 2          |           | Memori01.txt |
| Blocco note    | {19BED232-30AB-11D3-91D3-00C04FD70856} | NOTEPADDIR  | 2          |           | Redpark.exe  |



 

[Continua](updating-features-for-an-upgrade.md)

 

 




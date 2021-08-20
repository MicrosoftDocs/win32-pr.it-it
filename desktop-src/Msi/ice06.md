---
description: ICE06 controlla ogni tabella per verificare che tutte le colonne elencate nella tabella \_ Validation siano presenti nella tabella. Se una tabella non esiste, tutte \_ le voci di convalida per tale tabella vengono ignorate.
ms.assetid: 0c3f21ae-49ea-4cfe-b465-6fdc2b19cbb9
title: ICE06
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: febccd205b78e90d3dac49f88d0750f803c8cd575b6b76b46cab79a684deea90
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118142569"
---
# <a name="ice06"></a>ICE06

ICE06 controlla ogni tabella per verificare che tutte le colonne elencate nella tabella [ \_ Validation](-validation-table.md) siano presenti nella tabella. Se una tabella non esiste, tutte \_ le voci di convalida per tale tabella vengono ignorate.

Lo scopo di ICE06 è rilevare le istanze in cui un autore tenta di usare una nuova tabella di convalida che riflette una modifica dello schema con un database precedente che non \_ è stato aggiornato. ICE06 rileva anche il case inverso di una tabella di convalida precedente \_ usata con un database modificato.

Si noti che la convalida interna eseguita da [ICE03](ice03.md) rileva l'istanza di una colonna di tabella non definita nella tabella \_ validation elencata nel catalogo columns. L'uso di ICE03 e ICE06 garantisce pertanto che ogni colonna del database sia testata.

## <a name="result"></a>Risultato

ICE06 invia un errore quando nella tabella Validation è definita una colonna di tabella non \_ elencata nella \_ tabella Columns.

## <a name="example"></a>Esempio

Per l'esempio seguente ICE06 pubblica il messaggio

Colonna: Versione della tabella: ModuleSignature non è definito nel database.

[ \_ Tabella di convalida](-validation-table.md) (parziale)



| Tabella           | Colonna   |
|-----------------|----------|
| ModuleSignature | ModuleID |
| ModuleSignature | Versione  |



 

[ \_ Tabella Columns](-columns-table.md) (parziale)



| Tabella           | Numero | Nome     |
|-----------------|--------|----------|
| ModuleSignature | 1      | ModuleID |



 

La colonna Version della tabella ModuleSignature non è presente nel database o è elencata nella \_ tabella Columns.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni di riferimento su ICE](ice-reference.md)
</dt> </dl>

 

 




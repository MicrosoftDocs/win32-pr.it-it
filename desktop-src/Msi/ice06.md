---
description: ICE06 controlla ogni tabella per verificare che tutte le colonne elencate nella \_ tabella di convalida siano presenti nella tabella. Se una tabella non esiste, eventuali \_ voci di convalida per tale tabella verranno ignorate.
ms.assetid: 0c3f21ae-49ea-4cfe-b465-6fdc2b19cbb9
title: ICE06
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e9442d9b2c4089b88299106de875074bd7b0625
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103967796"
---
# <a name="ice06"></a>ICE06

ICE06 controlla ogni tabella per verificare che tutte le colonne elencate nella [ \_ tabella di convalida](-validation-table.md) siano presenti nella tabella. Se una tabella non esiste, eventuali \_ voci di convalida per tale tabella verranno ignorate.

Lo scopo di ICE06 consiste nel rilevare le istanze in cui un autore tenta di utilizzare una nuova \_ tabella di convalida che riflette una modifica dello schema con un database obsoleto che non è stato aggiornato. ICE06 rileva inoltre il caso inverso di una \_ tabella di convalida precedente utilizzata con un database modificato.

Si noti che la convalida interna eseguita da [ICE03](ice03.md) rileva l'istanza di una colonna di tabella non definita nella \_ tabella di convalida che viene elencata nel catalogo Columns. L'utilizzo di ICE03 e ICE06 garantisce pertanto la verifica di ogni colonna del database.

## <a name="result"></a>Risultato

ICE06 Invia un errore quando nella tabella di convalida è definita una colonna della tabella \_ che non è elencata nella \_ tabella Columns.

## <a name="example"></a>Esempio

Per l'esempio seguente ICE06 invia il messaggio

Column: versione della tabella: ModuleSignature non è definito nel database.

[ \_ Tabella di convalida](-validation-table.md) (parziale)



| Tabella           | Colonna   |
|-----------------|----------|
| ModuleSignature | ModuleID |
| ModuleSignature | Versione  |



 

[ \_ Tabella Columns](-columns-table.md) (parziale)



| Tabella           | Number | Nome     |
|-----------------|--------|----------|
| ModuleSignature | 1      | ModuleID |



 

La colonna Version della tabella ModuleSignature non è presente nel database o è elencata nella \_ tabella Columns.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Riferimento ghiaccio](ice-reference.md)
</dt> </dl>

 

 




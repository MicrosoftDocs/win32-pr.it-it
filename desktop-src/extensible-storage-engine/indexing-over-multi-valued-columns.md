---
description: 'Altre informazioni su: indicizzazione su colonne multivalore'
title: Indicizzazione su colonne multivalore
TOCTitle: Indexing over Multi-Valued Columns
ms:assetid: 90e31df2-2f5b-47a8-84c1-ece6bcc40858
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269341(v=EXCHG.10)
ms:contentKeyID: 32765630
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: aea24e8423b704b7e0345898bcb6ae4b6d7c057b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308540"
---
# <a name="indexing-over-multi-valued-columns"></a>Indicizzazione su colonne multivalore


_**Si applica a:** Windows | Windows Server_

## <a name="indexing-over-multi-valued-columns"></a>Indicizzazione su colonne multivalore

L'indicizzazione su colonne multivalore viene eseguita solo sulla prima colonna multivalore nell'indice. La prima colonna multivalore viene espansa in modo che ogni valore nella colonna venga indicizzato. Tutte le altre colonne multivalore vengono indicizzate solo sul primo valore della colonna. Un indice, ad esempio, viene definito sulla colonna A e sulla colonna B, in cui entrambe le colonne sono multivalore. In un record specificato, la colonna A ha i valori rosso e blu e la colonna B presenta i valori 1, 2 e 3. L'indice risultante darebbe le voci per Red-1 e Blue-1. I valori nella seconda colonna, colonna B, non vengono espansi. Si noti che anche se ogni colonna con tag può essere multivalore, solo le colonne con tag che sono contrassegnate in modo esplicito come multivalore tramite JET_bitColumnMultiValued vengono espanse in questo modo. Inoltre, a causa del fatto che le voci di indice primario contengono record, non è consentito disporre di un indice primario su una colonna multivalore perché ciò comporterebbe più posizioni nell'indice in cui deve risiedere il record. Per ulteriori informazioni, vedere l'argomento relativo alle [colonne contrassegnate, fisse e variabili](./tagged-fixed-and-variable-columns.md) .

A partire da Windows Vista, gli utenti hanno la possibilità di impostare l'opzione JET_bitIndexCrossProduct quando l'indice viene creato con [JetCreateIndex](./jetcreateindex-function.md) o [JetCreateIndex2](./jetcreateindex2-function.md) usando la struttura di [JET_INDEXCREATE](./jet-indexcreate-structure.md) . Quando questa opzione è impostata su un indice, vengono espanse tutte le colonne chiave multivalore nell'indice e viene creato un prodotto incrociato nell'indice per ogni valore in tali colonne. L'esempio precedente restituisce ora le voci per Red-1, Red-2, Red-3, Blue-1, Blue-2, Blue-3. Anche in questo caso, ogni colonna chiave deve essere dichiarata in modo esplicito per essere multivalore tramite JET_bitColumnMultiValued da espandere nell'indice.

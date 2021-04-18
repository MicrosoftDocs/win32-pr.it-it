---
description: ICE32 verifica che le chiavi e le chiavi esterne nel file con estensione msi abbiano lo stesso tipo di definizione delle dimensioni e della colonna.
ms.assetid: cc488ec5-e17a-4829-9763-38ba3c33bfde
title: ICE32
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02d6ff9e4de592ac073050b357aff0c63d984f0d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314223"
---
# <a name="ice32"></a>ICE32

ICE32 verifica che le chiavi e le chiavi esterne nel file con estensione msi abbiano lo stesso tipo di definizione delle dimensioni e della colonna. Questa azione personalizzata ICE esegue il confronto usando la [ \_ tabella di convalida](-validation-table.md) e usando i tipi di definizione restituiti da [**MsiViewGetColumnInfo**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewgetcolumninfo). Per altre informazioni, vedere [formato della definizione di colonna](column-definition-format.md).

## <a name="result"></a>Risultato

ICE32 Invia errori se il file con estensione msi contiene chiavi esterne alle chiavi di un tipo di dati di colonna o di colonna diverso.

## <a name="example"></a>Esempio

ICE32 invia due errori per l'esempio illustrato:

-   È stata definita una chiave esterna e una chiave di dimensioni diverse.
-   È stata definita una chiave esterna e una chiave che differiscono nel tipo di definizione.

[ \_ Tabella di convalida](-validation-table.md) (parziale)



| Tabella | Colonna  | KeyTable | KeyColumn |
|-------|---------|----------|-----------|
| File  | Version | File     | 1         |
| Flap  | Colonna8 | Flap     | 1         |



 

Definizioni di colonna (parziali)



| Tabella | Colonna  | Tipo | Dimensione |
|-------|---------|------|------|
| File  | File    | s    | 72   |
| File  | Versione | S    | 32   |
| Flap  | Colonna 1 | i    | 2    |
| Flap  | Colonna8 | S    | 32   |



 

La colonna Version della tabella file può essere una chiave esterna per un altro file nella tabella file. Questo problema si verifica con i file complementari. Tuttavia, la colonna version consente solo una stringa di lunghezza 32, mentre la colonna file consente una stringa di lunghezza 72. Per correggere questo errore, modificare le lunghezze delle stringhe in modo che corrispondano.

Sono stati definiti una chiave esterna e una chiave che variano in base ai tipi di definizione. Column8 della tabella Flap è elencato come chiave esterna per Column1. Column8 è una colonna stringa e Column1 è una colonna di tipo Integer. È necessario definire la chiave esterna e le coppie di chiavi in modo che i relativi tipi di dati corrispondano.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Riferimento ghiaccio](ice-reference.md)
</dt> </dl>

 

 




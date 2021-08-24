---
description: ICE32 convalida che le chiavi e le chiavi esterne nel file .msi hanno le stesse dimensioni e gli stessi tipi di definizione di colonna.
ms.assetid: cc488ec5-e17a-4829-9763-38ba3c33bfde
title: ICE32
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12e9361cd091afea3444858e64e043b87b779c2313f0ba16bb0ec6cf58fad265
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119528621"
---
# <a name="ice32"></a>ICE32

ICE32 convalida che le chiavi e le chiavi esterne nel file .msi hanno le stesse dimensioni e gli stessi tipi di definizione di colonna. Questa azione personalizzata ICE esegue il confronto usando la [ \_ tabella Validation](-validation-table.md) e i tipi di definizione restituiti da [**MsiViewGetColumnInfo**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewgetcolumninfo). Per altre informazioni, vedere [Formato definizione colonna](column-definition-format.md).

## <a name="result"></a>Risultato

ICE32 invia errori se il file .msi contiene chiavi esterne a chiavi di una lunghezza di colonna o un tipo di dati di colonna diverso.

## <a name="example"></a>Esempio

ICE32 invia due errori per l'esempio illustrato:

-   Sono presenti una chiave esterna e una chiave definite che differiscono per le dimensioni.
-   Sono presenti una chiave esterna e una chiave definite che differiscono per il tipo di definizione.

[ \_ Tabella di convalida](-validation-table.md) (parziale)



| Tabella | Colonna  | KeyTable | KeyColumn |
|-------|---------|----------|-----------|
| File  | Version | File     | 1         |
| Lembo  | Colonna8 | Lembo     | 1         |



 

Definizioni di colonna (parziali)



| Tabella | Colonna  | Tipo | Dimensione |
|-------|---------|------|------|
| File  | File    | s    | 72   |
| File  | Versione | S    | 32   |
| Lembo  | Colonna 1 | i    | 2    |
| Lembo  | Colonna8 | S    | 32   |



 

La colonna Versione della tabella File può essere una chiave esterna per un altro file nella tabella File. Ciò si verifica con i file complementari. Tuttavia, la colonna Versione consente solo una lunghezza di stringa 32, mentre la colonna File consente una lunghezza di stringa 72. Per correggere l'errore, modificare la lunghezza della stringa in modo che corrisponda.

Sono presenti una chiave esterna e una chiave definite che differiscono per i relativi tipi di definizione. La colonna 8 della tabella Flap è elencata come chiave esterna per Column1. Column8 è una colonna stringa e Column1 è una colonna integer. Le coppie di chiave esterna e chiave devono essere definite in modo che i relativi tipi di dati corrispondano.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni di riferimento su ICE](ice-reference.md)
</dt> </dl>

 

 




---
description: ICEM07 verifica che l'ordine dei file nella tabella di sequenza corrisponda all'ordine dei file in MergeModule.CABinet.
ms.assetid: 5778e0c5-2f8d-4562-9c93-d6f6890a74e9
title: ICEM07
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 696d5c92671c3a8347cb43714d43e646a3e14f33
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103882410"
---
# <a name="icem07"></a>ICEM07

ICEM07 verifica che l'ordine dei file nella tabella di sequenza corrisponda all'ordine dei file in [MergeModule.CABinet](mergemodule-cabinet.md).

I moduli CIEM di tipo merge vengono archiviati in un file con estensione cub del modulo merge denominato Mergemod. cub e non nel file con estensione cub contenente i ghiacci utilizzati per la convalida del pacchetto.

## <a name="result"></a>Risultato

ICEM07 Invia un errore se l'ordine dei file nella tabella file non corrisponde all'ordine nel file CAB.

## <a name="example"></a>Esempio

IC0M07 invia il messaggio di errore seguente per l'esempio illustrato.

``` syntax
The file 'FileB.GUID1' appears to be out of sequence. It has position 3 
in the CAB, but not when the file table is ordered by sequence number.
```

[Tabella file](file-table.md)



| File          | Sequenza |
|---------------|----------|
| Filea. *Guid1* | 1        |
| FileB. *Guid1* | 8        |
| FileC. *Guid1* | 52       |



 

Incorporato [MergeModule.CABinet](mergemodule-cabinet.md)



| File          |
|---------------|
| Filea. *Guid1* |
| FileC. *Guid1* |
| Campo. *Guid1* |
| FileB. *Guid1* |



 

Sebbene i numeri di sequenza di file nella tabella file non debbano essere consecutivi e i file aggiuntivi possano esistere nel file CAB, la sequenza relativa di tutti i file nella tabella file deve corrispondere all'ordine in [MergeModule.CABinet](mergemodule-cabinet.md). Per correggere l'errore, modificare il numero di sequenza di FileB in modo che arrivi dopo FileC in modo che corrisponda all'ordine del file nel file CAB oppure ricompilare il file CAB con i file nell'ordine corretto.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Riferimento ghiaccio del modulo merge](merge-module-ice-reference.md)
</dt> </dl>

 

 




---
description: ICE63 controlla la sequenziazione corretta dell'azione RemoveExistingProducts.
ms.assetid: 4dd67bb0-c08a-4a44-b687-0394a3afc2c4
title: ICE63
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5faa6f2ddbcb95cdf12966c2887fe9438a5d610
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103883362"
---
# <a name="ice63"></a>ICE63

ICE63 controlla la sequenziazione corretta dell' [azione RemoveExistingProducts](removeexistingproducts-action.md). È possibile inserire l'azione RemoveExistingProducts:

1.  Tra InstallValidate e InstallInitialize
2.  Subito dopo InstallInitialize o dopo InstallInitialize se le azioni tra InstallInitialize e RemoveExistingProducts non generano azioni script.
3.  Subito dopo InstallExecute o InstallExecuteAgain e prima di InstallFinalize (si applica la stessa restrizione precedente).
4.  Dopo InstallFinalize.

La mancata correzione di un avviso o di un errore segnalato da ICE63 comporta un errore durante l'aggiornamento.

## <a name="result"></a>Risultato

ICE63 Invia un avviso o un errore se la sequenziazione dell'azione RemoveExistingProducts non è corretta.

## <a name="example"></a>Esempio

ICE63 segnala l'errore seguente per l'esempio illustrato.

``` syntax
WARNING: Some action falls between InstallInitialize and RemoveExistingProducts.
```

L'azione ' MyCustomAction ' viene eseguita tra InstallInitialize e RemoveExistingProducts. Se MyCustomAction genera qualsiasi azione nello script, causa problemi nell'installazione.

Per correggere l'errore, verificare che MyCustomAction non generi azioni script né risequenziare le azioni.

[Tabella InstallExecuteSequence](installexecutesequence-table.md)



| Azione                 | Condizione | Sequenza |
|------------------------|-----------|----------|
| InstallInitialize      |           | 1000     |
| MyCustomAction         |           | 1010     |
| RemoveExistingProducts |           | 1020     |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Riferimento ghiaccio](ice-reference.md)
</dt> </dl>

 

 




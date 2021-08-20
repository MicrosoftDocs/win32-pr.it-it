---
description: ICE63 verifica la corretta sequenziazione dell'azione RemoveExistingProducts.
ms.assetid: 4dd67bb0-c08a-4a44-b687-0394a3afc2c4
title: ICE63
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f0de847a3b79c87b8ddc7dbaf3be64f88b9ef34df80d92737b6d9005ffdad24
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118142495"
---
# <a name="ice63"></a>ICE63

ICE63 verifica la corretta sequenziazione [dell'azione RemoveExistingProducts](removeexistingproducts-action.md). È possibile inserire l'azione RemoveExistingProducts:

1.  Tra InstallValidate e InstallInitialize
2.  Immediatamente dopo InstallInitialize o dopo InstallInitialize se le azioni tra InstallInitialize e RemoveExistingProducts non generano azioni script.
3.  Immediatamente dopo InstallExecute o InstallExecuteAgain e prima di InstallFinalize (si applica la stessa restrizione descritta in precedenza).
4.  Dopo InstallFinalize.

Se non si corregge un avviso o un errore segnalato da ICE63, si verifica un errore di aggiornamento.

## <a name="result"></a>Risultato

ICE63 invia un avviso o un errore se la sequenziazione dell'azione RemoveExistingProducts non è corretta.

## <a name="example"></a>Esempio

ICE63 segnala l'errore seguente per l'esempio illustrato.

``` syntax
WARNING: Some action falls between InstallInitialize and RemoveExistingProducts.
```

L'azione 'MyCustomAction' si verifica tra InstallInitialize e RemoveExistingProducts. Se MyCustomAction genera azioni nello script, si verificano problemi durante l'installazione.

Per correggere l'errore, verificare che MyCustomAction non generi azioni script o rieseguire la sequenziazione delle azioni.

[Tabella InstallExecuteSequence](installexecutesequence-table.md)



| Azione                 | Condition | Sequenza |
|------------------------|-----------|----------|
| InstallInitialize      |           | 1000     |
| MyCustomAction         |           | 1010     |
| RemoveExistingProducts |           | 1020     |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni di riferimento su ICE](ice-reference.md)
</dt> </dl>

 

 




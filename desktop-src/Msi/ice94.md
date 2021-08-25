---
description: ICE94 controlla la tabella dei collegamenti, la tabella delle funzionalità e la tabella MsiAssembly e invia un avviso se sono presenti collegamenti non capovolti che puntano a un file di assembly nella Global Assembly Cache.
ms.assetid: 9b1b25b5-b190-47c2-8d43-fa3964e87a6f
title: ICE94
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1dd203fe35b6bedc7d36f3e5a5c18fc6a235d3e65924b41909803e67ab79337e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119894891"
---
# <a name="ice94"></a>ICE94

ICE94 controlla la tabella [collegamento](shortcut-table.md) [,](feature-table.md)la tabella delle funzionalità e la tabella [MsiAssembly](msiassembly-table.md) e invia un avviso se sono presenti collegamenti non capovolti che puntano a un file di assembly nella Global Assembly Cache. Se la voce nel campo Destinazione della tabella Collegamento non è una funzionalità nella tabella Funzionalità, il collegamento non viene capovolto. Se la voce nel campo Componente della tabella Collegamento è elencata anche nella tabella MsiAssembly, il collegamento punta \_ a un file di assembly. Se la voce nel campo Applicazione file della tabella \_ MsiAssembly è vuota, il file di assembly si trova nella Global Assembly Cache.

## <a name="result"></a>Risultato

ICE94 invia l'avviso seguente.



| Avviso ICE94                                                                                | Descrizione                                                                            |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| Il collegamento non annunciato ' \[ 2 \] ' punta a un file di assembly nella Global Assembly Cache. | Un collegamento non capovolto punta a un file di assembly nella Global Assembly Cache. |



 

## <a name="example"></a>Esempio

ICE94 segnala l'errore seguente per l'esempio:

``` syntax
The non-advertised shortcut 'shortcut1' points to an assembly file in the global assembly cache.
```

[Tabella dei collegamenti](shortcut-table.md) (parziale)



| Tasto di scelta rapida  | Componente\_ | Destinazione    |
|-----------|-------------|-----------|
| collegamento1 | c1          | \[file1\] |
| collegamento2 | c2          | feature1  |
| collegamento3 | c3          | \[file2\] |



 

[Tabella delle funzionalità](feature-table.md) (parziale)



| Funzionalità  |
|----------|
| feature1 |



 

[Tabella MsiAssembly](msiassembly-table.md) (parziale)



| Componente\_ | Applicazione \_ file |
|-------------|-------------------|
| c1          |                   |
| c2          |                   |
| c3          | fa1               |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni di riferimento su ICE](ice-reference.md)
</dt> </dl>

 

 




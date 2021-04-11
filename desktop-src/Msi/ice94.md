---
description: ICE94 controlla la tabella dei collegamenti, la tabella delle funzionalità e la tabella MsiAssembly e invia un avviso se sono presenti collegamenti non pubblicizzati che puntano a un file di assembly nel Global Assembly Cache.
ms.assetid: 9b1b25b5-b190-47c2-8d43-fa3964e87a6f
title: ICE94
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8ce52e88a31e246eb4d69defba77b64c2955eb8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233155"
---
# <a name="ice94"></a>ICE94

ICE94 [Controlla la tabella dei collegamenti,](shortcut-table.md)la tabella delle [funzionalità](feature-table.md)e la [tabella MsiAssembly](msiassembly-table.md) e invia un avviso se sono presenti collegamenti non pubblicizzati che puntano a un file di assembly nel Global assembly cache. Se la voce nel campo di destinazione della tabella dei collegamenti non è una funzionalità della tabella delle funzionalità, il collegamento non verrà annunciato. Se la voce nel campo componente \_ della tabella dei collegamenti è elencata anche nella tabella MsiAssembly, il collegamento punta a un file di assembly. Se la voce nel \_ campo applicazione file nella tabella MsiAssembly è vuota, il file di assembly si trova nel Global assembly cache.

## <a name="result"></a>Risultato

ICE94 invia il seguente avviso.



| Avviso di ICE94                                                                                | Descrizione                                                                            |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| Il collegamento non annunciato ' \[ 2 \] ' punta a un file di assembly nel Global assembly cache. | Un collegamento non annunciato sta puntando a un file di assembly nel Global Assembly Cache. |



 

## <a name="example"></a>Esempio

ICE94 segnala l'errore seguente per l'esempio:

``` syntax
The non-advertised shortcut 'shortcut1' points to an assembly file in the global assembly cache.
```

[Tabella collegamenti](shortcut-table.md) (parziale)



| Tasto di scelta rapida  | Componente\_ | Destinazione    |
|-----------|-------------|-----------|
| shortcut1 | c1          | \[file1\] |
| shortcut2 | c2          | Feature1  |
| shortcut3 | c3          | \[file2\] |



 

[Tabella delle funzionalità](feature-table.md) (parziale)



| Funzionalità  |
|----------|
| Feature1 |



 

[Tabella MsiAssembly](msiassembly-table.md) (parziale)



| Componente\_ | \_Applicazione file |
|-------------|-------------------|
| c1          |                   |
| c2          |                   |
| c3          | FA1               |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Riferimento ghiaccio](ice-reference.md)
</dt> </dl>

 

 




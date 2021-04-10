---
description: ICE54 verifica la presenza di componenti che usano un file complementare come percorso della chiave.
ms.assetid: 94fcabfe-4500-42f2-acea-13b9a6681ca6
title: ICE54
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99df2ba90ccb44e33b67aaf8ecdcadc723e8d2fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103882121"
---
# <a name="ice54"></a>ICE54

ICE54 verifica la presenza di componenti che usano un file complementare come percorso della chiave.

Il file del percorso della chiave di un componente non deve derivare la propria versione da un file diverso. Questo può causare un errore di installazione di alcuni file. Per ulteriori informazioni sui file complementari, vedere la [tabella dei file](file-table.md) .

## <a name="result"></a>Risultato

ICE54 pubblica un avviso se un componente dispone di un file di percorso della chiave che deriva la versione da un altro file.

## <a name="example"></a>Esempio

ICE54 restituisce l'avviso seguente per l'esempio illustrato.

``` syntax
Component 'Component1' uses file 'File1' as its KeyPath, but the file's version is provided by the file 'File2'.
```

[Tabella componenti](component-table.md) (parziale)



| Componente  | Attributo | KeyPath |
|------------|-----------|---------|
| Component1 | 0         | File1   |



 

[Tabella file](file-table.md) (parziale)



| File  | Versione | Linguaggio |
|-------|---------|----------|
| File1 | File2   |          |
| File2 | 1.0.0.0 | 1033     |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Riferimento ghiaccio](ice-reference.md)
</dt> </dl>

 

 




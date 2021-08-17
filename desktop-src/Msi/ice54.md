---
description: ICE54 verifica la presenza di componenti che usano un file complementare come percorso della chiave.
ms.assetid: 94fcabfe-4500-42f2-acea-13b9a6681ca6
title: ICE54
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00658bb62b5c29b25f9fb653e216920fc776ba6df0e3fc2f8b47bbdf715040b4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118946608"
---
# <a name="ice54"></a>ICE54

ICE54 verifica la presenza di componenti che usano un file complementare come percorso della chiave.

Il file del percorso della chiave di un componente non deve derivare la versione da un file diverso. Ciò può causare l'installazione di alcuni file. Per altre [informazioni sui file complementari,](file-table.md) vedere la tabella File.

## <a name="result"></a>Risultato

ICE54 invia un avviso se un componente ha un file di percorso della chiave che deriva la versione da un altro file.

## <a name="example"></a>Esempio

ICE54 restituisce l'avviso seguente per l'esempio illustrato.

``` syntax
Component 'Component1' uses file 'File1' as its KeyPath, but the file's version is provided by the file 'File2'.
```

[Tabella dei componenti](component-table.md) (parziale)



| Componente  | Attributo | KeyPath |
|------------|-----------|---------|
| Componente1 | 0         | File1   |



 

[Tabella file](file-table.md) (parziale)



| File  | Versione | Linguaggio |
|-------|---------|----------|
| File1 | File2   |          |
| File2 | 1.0.0.0 | 1033     |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni di riferimento su ICE](ice-reference.md)
</dt> </dl>

 

 




---
description: Una sottoquery è un file di ricerca salvato ( \* . search-ms) che può essere utilizzato come filtro per una nuova query.
ms.assetid: a92c774f-310b-4c40-be1c-0c2b0cac907b
title: Argomento SOTTOQUERY (Windows Search)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f673cf9c2a9867593fd6c8fdac83b5901f531257
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966537"
---
# <a name="subquery-argument-windows-search"></a>Argomento SOTTOQUERY (Windows Search)

Una sottoquery è un file di ricerca salvato ( \* . search-ms) che può essere utilizzato come filtro per una nuova query. I risultati della sottoquery vengono usati come origine per la nuova query. Si immagini, ad esempio, di avere diversi file di ricerca salvati che limitano una query tramite la lista di distribuzione di posta elettronica: reparto. search-ms, TeamProject. search-ms e corporatewide. search-ms. L'uso dell' `subquery` argomento consente di limitare la ricerca di messaggi di posta elettronica a una o a tutte le ricerche salvate.

Questo argomento è organizzato nel modo seguente:

-   [Esempio](#example)
-   [Argomenti correlati](#related-topics)

## <a name="example"></a>Esempio


```
 search-ms:query=vacation&subquery=mydepartment.search-ms
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Introduzione con argomenti di Parameter-Value](getting-started-with-parameter-value-arguments.md)
</dt> <dt>

[Argomenti dell'identificatore delle impostazioni locali](-search-3x-wds-qryidx-localeidentifiers.md)
</dt> <dt>

[Argomento BRICIOLo](-search-3x-wds-qryidx-crumb.md)
</dt> <dt>

[Argomento della sintassi](-search-3x-wds-qryidx-syntaxargument.md)
</dt> <dt>

[Argomento STACKEDBY](-search-3x-wds-qryidx-stackedby.md)
</dt> </dl>

 

 




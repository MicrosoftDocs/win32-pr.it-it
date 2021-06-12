---
description: Informazioni sull'argomento SUBQUERY in Windows Search. Una sottoquery è un file di ricerca salvato che è possibile usare come filtro per una nuova query.
ms.assetid: a92c774f-310b-4c40-be1c-0c2b0cac907b
title: Argomento SUBQUERY (Windows Search)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93b23028d0bddcc674714f51f8b31883052431bd
ms.sourcegitcommit: 8f0a1d212dd154e8d94ab4c0e4ced053fa16823a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/11/2021
ms.locfileid: "112011034"
---
# <a name="subquery-argument-windows-search"></a>Argomento SUBQUERY (Windows Search)

Una sottoquery è un file di ricerca salvato (con estensione search-ms) che è possibile usare come filtro \* per una nuova query. I risultati della sottoquery vengono usati come origine per la nuova query. Si supponga, ad esempio, di avere diversi file di ricerca salvati che limitano una query in base alla lista di distribuzione di posta elettronica: mydepartment.search-ms, teamproject.search-ms e corporatewide.search-ms. L'uso `subquery` dell'argomento consente di limitare le ricerche di posta elettronica a una o a tutte queste ricerche salvate.

Questo argomento è organizzato come segue:

-   [Esempio](#example)
-   [Argomenti correlati](#related-topics)

## <a name="example"></a>Esempio


```
 search-ms:query=vacation&subquery=mydepartment.search-ms
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Attività iniziali con Parameter-Value argomenti](getting-started-with-parameter-value-arguments.md)
</dt> <dt>

[Argomenti dell'identificatore delle impostazioni locali](-search-3x-wds-qryidx-localeidentifiers.md)
</dt> <dt>

[Argomento CRUMB](-search-3x-wds-qryidx-crumb.md)
</dt> <dt>

[Argomento SYNTAX](-search-3x-wds-qryidx-syntaxargument.md)
</dt> <dt>

[Argomento STACKEDBY](-search-3x-wds-qryidx-stackedby.md)
</dt> </dl>

 

 




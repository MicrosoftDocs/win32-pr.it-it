---
title: Direttive pragma
description: RC non supporta le direttive pragma supportate dal compilatore C/C++.
ms.assetid: c7a944c0-a3d4-4568-a9ac-c338f0eaa427
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab0c92136ba5e00d5b821d35ea05a337e7d6abe7
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104046721"
---
# <a name="pragma-directives"></a>Direttive pragma

RC non supporta le direttive pragma supportate dal compilatore C/C++. Tuttavia, RC supporta la direttiva pragma seguente per modificare la tabella codici:

``` syntax
#pragma code_page( [ DEFAULT | CodePageNum ] )
```

Questo pragma non è supportato in un file di risorse incluso (RC). Se pertanto si dispone di un file RC padre che include i file RC per più lingue, utilizzare questo pragma prima di includere un altro file RC anziché utilizzarlo nel file RC incluso. Questo approccio è illustrato nell'esempio seguente.

``` syntax
#include "English.rc"
#pragma code_page(932)
#include "Japanese.rc"
```

Per un elenco di valori per CodePageNum, vedere la pagina relativa agli [identificatori](../intl/code-page-identifiers.md)delle tabelle codici.

 

 
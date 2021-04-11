---
description: Consente di impostare le opzioni di animazione.
ms.assetid: 727b4d87-4164-4915-b158-d21fe7d1b729
title: AnimationOptions
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7bd3c5df8081523ccef2a802e631454fadaeeae
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127130"
---
# <a name="animationoptions"></a>AnimationOptions

Consente di impostare le opzioni di animazione.

``` syntax
template AnimationOptions
{
    < E2BF56C0-840F-11cf-8F52-0040333594A3 >
    DWORD openclosed;
    DWORD positionquality;
} 
```

Dove:

-   openclosed: usare 0 per un'animazione chiusa o 1 per un'animazione aperta. Per impostazione predefinita, un'animazione viene chiusa.
-   positionquality: impostare la qualità della posizione per le chiavi di posizione specificate. Usare 0 per le posizioni spline o 1 per le posizioni lineari.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Modelli](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 




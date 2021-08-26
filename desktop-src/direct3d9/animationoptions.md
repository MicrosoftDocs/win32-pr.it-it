---
description: Consente di impostare le opzioni di animazione.
ms.assetid: 727b4d87-4164-4915-b158-d21fe7d1b729
title: Opzioni di animazione
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 346eaa1b94637fa357f09cd701ac9d99d5ddf2076ee12654076e54bce82527fe
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120069431"
---
# <a name="animationoptions"></a>Opzioni di animazione

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

-   openclosed: usare 0 per un'animazione chiusa o 1 per un'animazione aperta. Per impostazione predefinita, un'animazione è chiusa.
-   positionquality: imposta la qualità della posizione per le chiavi di posizione specificate. Usare 0 per le posizioni della spline o 1 per le posizioni lineari.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Modelli](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 




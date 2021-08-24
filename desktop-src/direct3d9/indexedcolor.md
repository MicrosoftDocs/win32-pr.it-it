---
description: È costituito da un parametro di indice e da un colore RGBA e viene usato per definire i colori dei vertici della mesh. L'indice definisce il vertice a cui viene applicato il colore.
ms.assetid: 63909c54-c2de-4065-9882-58fca2b4e893
title: IndexedColor
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2b0dcaf850786a18e5fc317276939436b93c3a49765d520aa40f88cd53707d2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119563731"
---
# <a name="indexedcolor"></a>IndexedColor

È costituito da un parametro di indice e da un colore RGBA e viene usato per definire i colori dei vertici della mesh. L'indice definisce il vertice a cui viene applicato il colore.

``` syntax
template IndexedColor
{
    < 1630B820-7842-11cf-8F52-0040333594A3 >
    DWORD index;
    ColorRGBA indexColor;
} 
```

Dove:

-   index: valore DWORD. Vedere la descrizione precedente.
-   indexColor: modello ColorRGBA. Vedere [**ColorRGBA**](colorrgba.md).

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Modelli](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 




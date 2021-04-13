---
description: È costituito da un parametro di indice e da un colore RGBA e viene usato per definire i colori dei vertici di rete. L'indice definisce il vertice a cui viene applicato il colore.
ms.assetid: 63909c54-c2de-4065-9882-58fca2b4e893
title: IndexedColor
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c895cf56efedfa7214bcfa6acafd32ab9324bbe8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104341706"
---
# <a name="indexedcolor"></a>IndexedColor

È costituito da un parametro di indice e da un colore RGBA e viene usato per definire i colori dei vertici di rete. L'indice definisce il vertice a cui viene applicato il colore.

``` syntax
template IndexedColor
{
    < 1630B820-7842-11cf-8F52-0040333594A3 >
    DWORD index;
    ColorRGBA indexColor;
} 
```

Dove:

-   index-un valore DWORD. Vedere la descrizione sopra.
-   indexColor: modello ColorRGBA. Vedere [**ColorRGBA**](colorrgba.md).

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Modelli](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 




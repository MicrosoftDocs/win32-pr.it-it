---
title: IAgentPropertySheet GetSize
description: IAgentPropertySheet GetSize
ms.assetid: 09bac150-ad68-40b2-9c2c-760f6bc919e4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd5e185a6e8d55d87e561f727c8dc9df8a8cfd63
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298326"
---
# <a name="iagentpropertysheetgetsize"></a>IAgentPropertySheet:: GetSize

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT GetSize(
   long * plWidth,  // address of variable for property sheet width
   long * plHeight  // address of variable for property sheet height
);
```

Recupera le dimensioni della finestra delle proprietà di Microsoft Agent.

-   Restituisce \_ OK per indicare che l'operazione è stata completata.

<dl> <dt>

<span id="plWidth"></span><span id="plwidth"></span><span id="PLWIDTH"></span>*plWidth*
</dt> <dd>

Indirizzo di una variabile che riceve la larghezza della finestra delle proprietà in pixel rispetto all'origine della schermata (in alto a sinistra).

</dd> <dt>

<span id="plHeight"></span><span id="plheight"></span><span id="PLHEIGHT"></span>*plHeight*
</dt> <dd>

Indirizzo di una variabile che riceve l'altezza della finestra delle proprietà in pixel rispetto all'origine della schermata (in alto a sinistra).

</dd> </dl>

## <a name="see-also"></a>Vedere anche

[**IAgentPropertySheet:: GetPosition**](iagentpropertysheet--getposition.md)


 

 





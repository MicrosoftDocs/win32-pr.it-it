---
title: IAgentPropertySheet GetSize
description: IAgentPropertySheet GetSize
ms.assetid: 09bac150-ad68-40b2-9c2c-760f6bc919e4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1907e011dfbd965eacdd0b37d9dad9b4540b20a381727b62e0880931093df27c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117692313"
---
# <a name="iagentpropertysheetgetsize"></a>IAgentPropertySheet::GetSize

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT GetSize(
   long * plWidth,  // address of variable for property sheet width
   long * plHeight  // address of variable for property sheet height
);
```

Recupera le dimensioni della finestra della finestra delle proprietà di Microsoft Agent.

-   Restituisce S \_ OK per indicare che l'operazione è riuscita.

<dl> <dt>

<span id="plWidth"></span><span id="plwidth"></span><span id="PLWIDTH"></span>*plWidth*
</dt> <dd>

Indirizzo di una variabile che riceve la larghezza della finestra delle proprietà in pixel, rispetto all'origine dello schermo (in alto a sinistra).

</dd> <dt>

<span id="plHeight"></span><span id="plheight"></span><span id="PLHEIGHT"></span>*plHeight*
</dt> <dd>

Indirizzo di una variabile che riceve l'altezza della finestra delle proprietà in pixel, rispetto all'origine dello schermo (in alto a sinistra).

</dd> </dl>

## <a name="see-also"></a>Vedere anche

[**IAgentPropertySheet::GetPosition**](iagentpropertysheet--getposition.md)


 

 





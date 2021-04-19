---
title: PULSANTE affiancato
description: L'attributo affiancato specifica o recupera un valore che indica se l'immagine del pulsante verrà affiancata.
ms.assetid: 5526477d-a235-4960-adef-5cf0ef9c46be
keywords:
- PULSANTE. finestre affiancate Media Player
topic_type:
- apiref
api_name:
- BUTTON.tiled
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c6c1316f10ce9ae3135f4ac35ab214ecdd1096d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333425"
---
# <a name="buttontiled"></a>PULSANTE affiancato

L'attributo **affiancato** specifica o recupera un valore che indica se l'immagine del **pulsante** verrà affiancata.

``` syntax
        elementID.tiled
```

## <a name="possible-values"></a>Valori possibili

Questo attributo è un **valore booleano** di lettura/scrittura.



| Valore | Descrizione                       |
|-------|-----------------------------------|
| true  | L'immagine verrà affiancata.              |
| false | Valore predefinito. L'immagine non verrà affiancata. |



 

## <a name="remarks"></a>Commenti

Se l'immagine è più piccola dell'area effettiva del controllo, il affiancamento dell'immagine lo ripeterà fino a riempire l'intera area. Se un'immagine non è specificata o non può essere recuperata, l'oggetto **affiancato** verrà impostato su false.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7,0 o successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elemento BUTTON**](button-element.md)
</dt> <dt>

[**BUTTON. image**](button-image.md)
</dt> </dl>

 

 






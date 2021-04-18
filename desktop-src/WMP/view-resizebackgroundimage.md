---
title: Visualizza resizeBackgroundImage
description: L'attributo resizeBackgroundImage specifica o recupera un valore che indica se è possibile ridimensionare l'immagine di sfondo.
ms.assetid: d18f3def-777f-4a71-961e-73bae98a4c64
keywords:
- Visualizza Media Player Windows resizeBackgroundImage
topic_type:
- apiref
api_name:
- VIEW.resizeBackgroundImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 397929d69cc6ac6ad51c29883898c153218afdca
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324071"
---
# <a name="viewresizebackgroundimage"></a>Visualizza resizeBackgroundImage

L'attributo **resizeBackgroundImage** specifica o recupera un valore che indica se è possibile ridimensionare l'immagine di sfondo.

``` syntax
        elementID.resizeBackgroundImage
```

## <a name="possible-values"></a>Valori possibili

Questo attributo è un **valore booleano** di lettura/scrittura.



| Valori | Descrizione                                      |
|--------|--------------------------------------------------|
| true   | È possibile ridimensionare l'immagine di sfondo.             |
| false  | Valore predefinito. Non è possibile ridimensionare l'immagine di sfondo. |



 

## <a name="remarks"></a>Commenti

Se si imposta questo attributo su true, l'immagine di sfondo verrà ridimensionata in modo da adattarsi ai valori correnti degli attributi di **larghezza** e **altezza** .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------|
| Versione<br/> | Windows Media Player 9 serie o versione successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elemento VIEW**](view-element.md)
</dt> <dt>

[**Visualizza. backgroundImage**](view-backgroundimage.md)
</dt> </dl>

 

 






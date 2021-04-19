---
title: Visualizza. ridimensionabile
description: L'attributo ridimensionabile recupera un valore che indica se la vista può essere ridimensionata.
ms.assetid: 4f0e4f31-cf16-498f-823f-da43566043b1
keywords:
- Visualizza. Media Player di Windows ridimensionabili
topic_type:
- apiref
api_name:
- VIEW.resizable
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed4d61973e34891d336ea5729ea40478c6c32808
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324070"
---
# <a name="viewresizable"></a>Visualizza. ridimensionabile

L'attributo **ridimensionabile** recupera un valore che indica se la **vista** può essere ridimensionata.

``` syntax
        elementID.resizable
```

## <a name="possible-values"></a>Valori possibili

Questo attributo è un valore **booleano** di sola lettura con un valore predefinito uguale all'attributo della **barra** del titolo.



| Valori | Descrizione             |
|--------|-------------------------|
| true   | La visualizzazione può essere ridimensionata.    |
| false  | Impossibile ridimensionare la visualizzazione. |



 

## <a name="remarks"></a>Commenti

Se non è presente alcuna **barra** di titolo e pertanto nessuna finestra o bordo, è necessario usare il metodo **size** per ridimensionare l'elemento di **visualizzazione** .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7,0 o successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elemento VIEW**](view-element.md)
</dt> </dl>

 

 






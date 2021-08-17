---
title: VIEW.resizable
description: L'attributo ridimensionabile recupera un valore che indica se l'oggetto VIEW può essere ridimensionato.
ms.assetid: 4f0e4f31-cf16-498f-823f-da43566043b1
keywords:
- VIEW.resizable Windows Media Player
topic_type:
- apiref
api_name:
- VIEW.resizable
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 622c732ce6a1218fa16bbe70c1ef18d53ba4211abfde9d39fc794ec862348033
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118332909"
---
# <a name="viewresizable"></a>VIEW.resizable

**L'attributo ridimensionabile** recupera un valore che indica se **l'oggetto VIEW** può essere ridimensionato.

``` syntax
        elementID.resizable
```

## <a name="possible-values"></a>Valori possibili

Questo attributo è un valore **booleano** di sola lettura con un valore predefinito uguale **all'attributo della barra del** titolo.



| Valori | Descrizione             |
|--------|-------------------------|
| true   | La visualizzazione può essere ridimensionata.    |
| false  | Impossibile ridimensionare la visualizzazione. |



 

## <a name="remarks"></a>Commenti

Se non è presente **alcuna barra del titolo** e pertanto non sono presenti finestre o bordi, è necessario usare il metodo **size** per ridimensionare l'elemento **VIEW.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7.0 o successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elemento VIEW**](view-element.md)
</dt> </dl>

 

 






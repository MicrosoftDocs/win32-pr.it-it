---
title: Funzione di tipo point2 (D2d1helper. h)
description: Crea un punto che archivia le coordinate usando il tipo di dati specificato.
ms.assetid: 59a631ae-d70e-4ee2-9546-2d19da40aa9b
keywords:
- Point2 funzione di tipo Direct2D
topic_type:
- apiref
api_name:
- Point2 Type Function
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f614f49077ed198c5e85d17b9ee3c84a5e300670
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302033"
---
# <a name="point2type-function"></a>Point2 ( <Type> funzione)

Crea un punto che archivia le coordinate usando il tipo di dati specificato.

``` syntax
template<typename Type>
typename TypeTraits<Type>::Point Point2(
  Type x,
  Type y
);
```

## <a name="template-parameters"></a>Parametri di template



| Parametro | Descrizione                                                                                                       |
|-----------|-------------------------------------------------------------------------------------------------------------------|
| Type      | Tipo di dati utilizzato per archiviare la coordinata x e la coordinata y del punto. I valori possibili sono FLOAT e UINT32. |



 

## <a name="parameters"></a>Parametri



| Parametro | Descrizione                    |
|-----------|--------------------------------|
| x         | Coordinata x del punto. |
| y         | Coordinata y del punto. |



 

## <a name="return-value"></a>Valore restituito

Punto che contiene la coordinata x e la coordinata y specificate.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7, Windows Vista con SP2 e aggiornamento della piattaforma per app desktop di Windows Vista \[ \| UWP\]<br/>                          |
| Server minimo supportato<br/> | Windows Server 2008 R2, Windows Server 2008 con SP2 e aggiornamento della piattaforma per app desktop di Windows Server 2008 \[ \| UWP\]<br/> |
| Telefono minimo supportato<br/>  | Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 e app per Windows Runtime\]<br/>                                                  |
| Intestazione<br/>                   | <dl> <dt>D2d1helper. h</dt> </dl>                                                  |
| Libreria<br/>                  | <dl> <dt>D2d1. lib</dt> </dl>                                                      |
| DLL<br/>                      | <dl> <dt>D2d1.dll</dt> </dl>                                                      |



 

 






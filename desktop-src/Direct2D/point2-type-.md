---
title: Funzione di tipo Point2 (D2d1helper.h)
description: Crea un punto che archivia le coordinate utilizzando il tipo di dati specificato.
ms.assetid: 59a631ae-d70e-4ee2-9546-2d19da40aa9b
keywords:
- Funzione di tipo Point2 Direct2D
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
ms.openlocfilehash: d925cc5676e6f0c9a8fb27a3ba2a12591ee87a5a72d5937e365fa57179e47ce1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118160377"
---
# <a name="point2type-function"></a>Funzione <Type> Point2

Crea un punto che archivia le coordinate utilizzando il tipo di dati specificato.

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
| Client minimo supportato<br/> | Windows 7, Windows Vista con SP2 e l'aggiornamento della piattaforma per Windows app desktop di Vista \[ \| per le app UWP\]<br/>                          |
| Server minimo supportato<br/> | Windows Server 2008 R2, Windows Server 2008 con SP2 e Aggiornamento della piattaforma per app desktop Windows Server 2008 \[ \| UWP\]<br/> |
| Telefono minimo supportato<br/>  | Windows Phone 8.1 \[ Windows Phone Silverlight 8.1 e Windows Runtime\]<br/>                                                  |
| Intestazione<br/>                   | <dl> <dt>D2d1helper.h</dt> </dl>                                                  |
| Libreria<br/>                  | <dl> <dt>D2d1.lib</dt> </dl>                                                      |
| DLL<br/>                      | <dl> <dt>D2d1.dll</dt> </dl>                                                      |



 

 






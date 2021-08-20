---
title: Funzione Rect Type (D2d1helper.h)
description: Crea una struttura rettangolare che archivia le coordinate usando il tipo di dati specificato.
ms.assetid: b152efaf-0779-4024-b998-82a347abba71
keywords:
- Funzione di tipo Rect Direct2D
topic_type:
- apiref
api_name:
- Rect Type Function
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dfb9dd2703a843b9f09ba1404cd9acfddc25620ff2dc4a00566b4c1582847449
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119075015"
---
# <a name="recttype-function"></a>Funzione <Type> Rect

Crea una struttura rettangolare che archivia le coordinate usando il tipo di dati specificato.

``` syntax
template<typename Type>
typename TypeTraits<Type>::Rect Rect(
  Type left,
  Type top,
  Type right,
  Type bottom
);
```

## <a name="template-parameters"></a>Parametri di template



| Parametro | Descrizione                                                                                                |
|-----------|------------------------------------------------------------------------------------------------------------|
| Type      | Tipo di dati utilizzato per archiviare le dimensioni del rettangolo. I valori possibili **sono FLOAT** e **UINT32.** |



 

## <a name="parameters"></a>Parametri



| Parametro | Descrizione                                             |
|-----------|---------------------------------------------------------|
| sinistro      | Coordinata x dell'angolo superiore sinistro del rettangolo.  |
| top       | Coordinata y dell'angolo superiore sinistro del rettangolo.  |
| right     | Coordinata x dell'angolo inferiore destro del rettangolo. |
| bottom    | Coordinata y dell'angolo inferiore destro del rettangolo. |



 

## <a name="return-value"></a>Valore restituito

Struttura rettangolare che contiene le coordinate specificate.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7, Windows Vista con SP2 e Aggiornamento piattaforma per Windows app desktop di Vista \[ \| app UWP\]<br/>                          |
| Server minimo supportato<br/> | Windows Server 2008 R2, Windows Server 2008 con SP2 e aggiornamento della piattaforma per Windows app desktop di Windows Server 2008 \[ app desktop \| UWP\]<br/> |
| Telefono minimo supportato<br/>  | Windows Phone 8.1 \[ Windows Phone silverlight 8.1 e Windows Runtime\]<br/>                                                  |
| Intestazione<br/>                   | <dl> <dt>D2d1helper.h</dt> </dl>                                                  |
| Libreria<br/>                  | <dl> <dt>D2d1.lib</dt> </dl>                                                      |
| DLL<br/>                      | <dl> <dt>D2d1.dll</dt> </dl>                                                      |



 

 






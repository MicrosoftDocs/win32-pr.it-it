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
ms.openlocfilehash: 2e5f56fd9cbcfd576a441d9199e7ec1114cfb9f3
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122884483"
---
# <a name="rectlttypegt-function"></a>Funzione rect &lt; type &gt;

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
| Client minimo supportato<br/> | Windows 7, Windows Vista con SP2 e Aggiornamento piattaforma per app desktop Windows Vista \[ \| app UWP\]<br/>                          |
| Server minimo supportato<br/> | Windows Server 2008 R2, Windows Server 2008 con SP2 e aggiornamento della piattaforma per app desktop Windows Server 2008 \[ \| app UWP\]<br/> |
| Telefono minimo supportato<br/>  | Windows Phone 8.1 \[ Windows Phone Silverlight 8.1 e Windows Runtime\]<br/>                                                  |
| Intestazione<br/>                   | <dl> <dt>D2d1helper.h</dt> </dl>                                                  |
| Libreria<br/>                  | <dl> <dt>D2d1.lib</dt> </dl>                                                      |
| DLL<br/>                      | <dl> <dt>D2d1.dll</dt> </dl>                                                      |



 

 






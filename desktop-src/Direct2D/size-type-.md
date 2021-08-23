---
title: Funzione Size Type (D2d1helper.h)
description: Crea una struttura di dimensioni che archivia la larghezza e l'altezza usando il tipo di dati specificato.
ms.assetid: 9f7e37a3-440e-40c0-a527-9fcbd207dce8
keywords:
- Funzione Size Type Direct2D
topic_type:
- apiref
api_name:
- Size Type Function
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf2bac3b43cf083d4f2d3588fed41d55380a435cc10c56cdfdb5cae1929d12c3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119292781"
---
# <a name="sizetype-function"></a>Funzione <Type> Size

Crea una struttura di dimensioni che archivia la larghezza e l'altezza usando il tipo di dati specificato.

``` syntax
template<typename Type>
typename TypeTraits<Type>::Size Size(
  Type width,
  Type height
);
```

## <a name="template-parameters"></a>Parametri di template



| Parametro | Descrizione                                                                                         |
|-----------|-----------------------------------------------------------------------------------------------------|
| Type      | Tipo di dati utilizzato per archiviare la larghezza e l'altezza delle dimensioni. I valori possibili sono FLOAT e UINT32. |



 

## <a name="parameters"></a>Parametri



| Parametro | Descrizione        |
|-----------|--------------------|
| width     | Larghezza della dimensione.  |
| altezza    | Altezza della dimensione. |



 

## <a name="return-value"></a>Valore restituito

Dimensione che contiene la larghezza e l'altezza specificate.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7, Windows Vista con SP2 e l'aggiornamento della piattaforma per Windows app desktop di Vista \[ \| per le app UWP\]<br/>                          |
| Server minimo supportato<br/> | Windows Server 2008 R2, Windows Server 2008 con SP2 e aggiornamento della piattaforma per app desktop Windows Server 2008 \[ \| app UWP\]<br/> |
| Telefono minimo supportato<br/>  | Windows Phone 8.1 \[ Windows Phone Silverlight 8.1 e Windows Runtime\]<br/>                                                  |
| Intestazione<br/>                   | <dl> <dt>D2d1helper.h</dt> </dl>                                                  |
| Libreria<br/>                  | <dl> <dt>D2d1.lib</dt> </dl>                                                      |
| DLL<br/>                      | <dl> <dt>D2d1.dll</dt> </dl>                                                      |



 

 






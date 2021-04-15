---
title: Funzione type size (D2d1helper. h)
description: Crea una struttura di dimensioni che archivia la larghezza e l'altezza usando il tipo di dati specificato.
ms.assetid: 9f7e37a3-440e-40c0-a527-9fcbd207dce8
keywords:
- Funzione tipo dimensione Direct2D
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
ms.openlocfilehash: a300ab0ce7da57440516733459f703379cf5a943
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476258"
---
# <a name="sizetype-function"></a>Size ( <Type> funzione)

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

Dimensioni che contengono la larghezza e l'altezza specificate.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7, Windows Vista con SP2 e aggiornamento della piattaforma per app desktop di Windows Vista \[ \| UWP\]<br/>                          |
| Server minimo supportato<br/> | Windows Server 2008 R2, Windows Server 2008 con SP2 e aggiornamento della piattaforma per app desktop di Windows Server 2008 \[ \| UWP\]<br/> |
| Telefono minimo supportato<br/>  | Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 e app per Windows Runtime\]<br/>                                                  |
| Intestazione<br/>                   | <dl> <dt>D2d1helper. h</dt> </dl>                                                  |
| Libreria<br/>                  | <dl> <dt>D2d1. lib</dt> </dl>                                                      |
| DLL<br/>                      | <dl> <dt>D2d1.dll</dt> </dl>                                                      |



 

 






---
title: Metodo INVALIDATELayout IDWriteTextLayout3
description: Invalida il layout, forzando la ricorsione del layout prima di chiamare le funzioni di metrica o disegno. Ciò è utile se la localizzazione di un tipo di carattere cambia e il layout deve essere ridisegnato o se le dimensioni di un oggetto IDWriteInlineObject implementato dal client cambiano.
ms.assetid: 65b42ee1-5b67-1f6d-0e4b-ee60b192e7b7
keywords:
- Metodo InvalidateLayout Direct Write
- Metodo InvalidateLayout Direct Write, interfaccia IDWriteTextLayout3
- Metodo InvalidateLayout dell'interfaccia IDWriteTextLayout3 Direct Write
topic_type:
- apiref
api_name:
- IDWriteTextLayout3.InvalidateLayout
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af698ce5f94918be281e633342060f70ba3f62655d7aec3794686a7793c4364a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117816082"
---
# <a name="idwritetextlayout3invalidatelayout-method"></a>Metodo IDWriteTextLayout3::InvalidateLayout

Invalida il layout, forzando la ricorsione del layout prima di chiamare le funzioni di metrica o disegno. Ciò è utile se la localizzazione di un tipo di carattere cambia e il layout deve essere ridisegnato o se le dimensioni di un oggetto IDWriteInlineObject implementato dal client cambiano.

## <a name="syntax"></a>Sintassi


```C++
HRESULT InvalidateLayout();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8.1 solo app desktop\]<br/>                                            |
| Server minimo supportato<br/> | Windows Server 2012 Solo app desktop R2 \[\]<br/>                                 |
| Telefono minimo supportato<br/>  | Windows Phone 8.1 \[ Windows Phone silverlight 8.1 e Windows Runtime\]<br/> |
| Libreria<br/>                  | <dl> <dt>Dwrite.lib</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>Dwrite.dll</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IDWriteTextLayout3**](idwritetextlayout3.md)
</dt> </dl>

 

 






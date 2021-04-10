---
title: Metodo IDWriteTextLayout3 InvalidateLayout
description: Invalida il layout, forzando il layout da rimisurare prima di chiamare le metriche o le funzioni di disegno. Questa operazione è utile se la località di un tipo di carattere viene modificata e il layout deve essere ridisegnato o se le dimensioni di un client implementate IDWriteInlineObject cambiano.
ms.assetid: 65b42ee1-5b67-1f6d-0e4b-ee60b192e7b7
keywords:
- Scrittura diretta metodo InvalidateLayout
- Metodo InvalidateLayout scrittura diretta, interfaccia IDWriteTextLayout3
- IDWriteTextLayout3 Interface Direct Write, metodo InvalidateLayout
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
ms.openlocfilehash: b5df97d4590f62f586a570d52428b6560a7d88df
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120254"
---
# <a name="idwritetextlayout3invalidatelayout-method"></a>Metodo IDWriteTextLayout3:: InvalidateLayout

Invalida il layout, forzando il layout da rimisurare prima di chiamare le metriche o le funzioni di disegno. Questa operazione è utile se la località di un tipo di carattere viene modificata e il layout deve essere ridisegnato o se le dimensioni di un client implementate IDWriteInlineObject cambiano.

## <a name="syntax"></a>Sintassi


```C++
HRESULT InvalidateLayout();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un codice di errore **HRESULT** .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 8.1 \[ solo app desktop\]<br/>                                            |
| Server minimo supportato<br/> | Solo app desktop Windows Server 2012 R2 \[\]<br/>                                 |
| Telefono minimo supportato<br/>  | Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 e app per Windows Runtime\]<br/> |
| Libreria<br/>                  | <dl> <dt>DWrite. lib</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>Dwrite.dll</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IDWriteTextLayout3**](idwritetextlayout3.md)
</dt> </dl>

 

 






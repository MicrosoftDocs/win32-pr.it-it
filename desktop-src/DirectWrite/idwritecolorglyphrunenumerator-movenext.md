---
title: Metodo MoveNext IDWriteColorGlyphRunEnumerator
description: Passare al glifo successivo eseguito nell'enumeratore.
ms.assetid: E6336C0E-F880-485C-9111-A102298257C1
keywords:
- Scrittura diretta metodo MoveNext
- Metodo MoveNext scrittura diretta, interfaccia IDWriteColorGlyphRunEnumerator
- IDWriteColorGlyphRunEnumerator Interface Direct Write, metodo MoveNext
topic_type:
- apiref
api_name:
- IDWriteColorGlyphRunEnumerator.MoveNext
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15c9963916c07f1df8cf3cfedb49b9e3fd66d0df
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518112"
---
# <a name="idwritecolorglyphrunenumeratormovenext-method"></a>Metodo IDWriteColorGlyphRunEnumerator:: MoveNext

Passare al glifo successivo eseguito nell'enumeratore.

## <a name="syntax"></a>Sintassi


```C++
HRESULT MoveNext(
  [out] BOOL *haveRun
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*haveRun* \[ out\]
</dt> <dd>

Tipo: **bool \** _

Restituisce _ *true** se è presente una successiva esecuzione del glifo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un codice di errore **HRESULT** .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | App \[ desktop di Windows 8.1 app \| UWP\]<br/>                                     |
| Server minimo supportato<br/> | App desktop di Windows Server 2012 R2 \[ \| UWP\]<br/>                          |
| Telefono minimo supportato<br/>  | Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 e app per Windows Runtime\]<br/> |
| Libreria<br/>                  | <dl> <dt>DWrite. lib</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>Dwrite.dll</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IDWriteColorGlyphRunEnumerator**](idwritecolorglyphrunenumerator.md)
</dt> </dl>

 

 






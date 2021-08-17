---
title: Metodo IdWriteTextLayout3 GetLineSpacing
description: Ottiene informazioni sull'interlinea.
ms.assetid: 6b93a3ec-c8ea-2e64-45b5-51565d6de173
keywords:
- Metodo GetLineSpacing Direct Write
- Metodo GetLineSpacing Direct Write, interfaccia IDWriteTextLayout3
- IdWriteTextLayout3 interface Direct Write , GetLineSpacing method
topic_type:
- apiref
api_name:
- IDWriteTextLayout3.GetLineSpacing
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 96444f0e50cbb79074c6fc6d8b041d91c0751616ec5afe7024704709a2240947
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119964011"
---
# <a name="idwritetextlayout3getlinespacing-method"></a>Metodo IDWriteTextLayout3::GetLineSpacing

Ottiene informazioni sull'interlinea.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetLineSpacing(
  [out] DWRITE_LINE_SPACING *lineSpacingOptions
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lineSpacingOptions* \[ Cambio\]
</dt> <dd>

Come gestire lo spazio tra le righe.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8.1 solo app desktop\]<br/>                                            |
| Server minimo supportato<br/> | Windows Server 2012 Solo \[ app desktop R2\]<br/>                                 |
| Telefono minimo supportato<br/>  | Windows Phone 8.1 \[ Windows Phone Silverlight 8.1 e Windows Runtime\]<br/> |
| Libreria<br/>                  | <dl> <dt>Dwrite.lib</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>Dwrite.dll</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IDWriteTextLayout3**](idwritetextlayout3.md)
</dt> </dl>

 

 






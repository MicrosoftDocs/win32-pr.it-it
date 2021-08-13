---
title: Metodo IdWriteTextLayout3 SetLineSpacing
description: Impostare l'interlinea. | Metodo IdWriteTextLayout3 SetLineSpacing
ms.assetid: 1bfca257-189c-4d18-628c-aff8217d2775
keywords:
- Metodo SetLineSpacing Direct Write
- Metodo SetLineSpacing Direct Write, interfaccia IDWriteTextLayout3
- Interfaccia IDWriteTextLayout3 Scrittura diretta, metodo SetLineSpacing
topic_type:
- apiref
api_name:
- IDWriteTextLayout3.SetLineSpacing
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d1c054fd63beb85303a7d163a16b55f07613b687085be53e22d814b0003c63c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118649379"
---
# <a name="idwritetextlayout3setlinespacing-method"></a>Metodo IDWriteTextLayout3::SetLineSpacing

Impostare l'interlinea.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetLineSpacing(
  [in] const DWRITE_LINE_SPACING *lineSpacingOptions
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lineSpacingOptions* \[ Pollici\]
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

 

 






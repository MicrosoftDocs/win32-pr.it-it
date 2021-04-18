---
title: Metodo IDWriteTextLayout DetermineMinWidth
description: Determina la larghezza minima possibile con cui è possibile impostare il layout senza interruzioni di emergenza tra i caratteri di parole intere che si verificano.
ms.assetid: 8efa1471-1b74-46d4-ac6d-fb1839ce2e74
keywords:
- Scrittura diretta metodo DetermineMinWidth
- Metodo DetermineMinWidth scrittura diretta, interfaccia IDWriteTextLayout
- IDWriteTextLayout Interface Direct Write, metodo DetermineMinWidth
topic_type:
- apiref
api_name:
- IDWriteTextLayout.DetermineMinWidth
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2525f770030b80f0e9c0d6df9e5ec88becbb394b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330156"
---
# <a name="idwritetextlayoutdetermineminwidth-method"></a>IDWriteTextLayout::D Metodo etermineMinWidth

Determina la larghezza minima possibile con cui è possibile impostare il layout senza interruzioni di emergenza tra i caratteri di parole intere che si verificano.

## <a name="syntax"></a>Sintassi


```C++
virtual HRESULT DetermineMinWidth(
  [out] FLOAT *minWidth
) = 0;
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*MinWidth* \[ out\]
</dt> <dd>

Tipo: **float \***

Larghezza minima.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un codice di errore **HRESULT** .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------|
| Libreria<br/> | <dl> <dt>DWrite. lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>Dwrite.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout)
</dt> <dt>

[**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout)
</dt> </dl>

 


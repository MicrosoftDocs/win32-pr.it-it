---
title: Metodo IDWriteTextLayout DetermineMinWidth
description: Determina la larghezza minima possibile su cui è possibile impostare il layout senza che si verifichi un'interruzione di emergenza tra i caratteri di parole intere.
ms.assetid: 8efa1471-1b74-46d4-ac6d-fb1839ce2e74
keywords:
- Metodo DetermineMinWidth Direct Write
- Metodo DetermineMinWidth Scrittura diretta, interfaccia IDWriteTextLayout
- Interfaccia IDWriteTextLayout Scrittura diretta, metodo DetermineMinWidth
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
ms.openlocfilehash: 41123f2a5d584341c344248d0af936f34fc04e49c9aabc1cb73ecea0eacc84ff
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120075531"
---
# <a name="idwritetextlayoutdetermineminwidth-method"></a>Metodo IDWriteTextLayout::D etermineMinWidth

Determina la larghezza minima possibile su cui è possibile impostare il layout senza che si verifichi un'interruzione di emergenza tra i caratteri di parole intere.

## <a name="syntax"></a>Sintassi


```C++
virtual HRESULT DetermineMinWidth(
  [out] FLOAT *minWidth
) = 0;
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*minWidth* \[ Cambio\]
</dt> <dd>

Tipo: **\* FLOAT**

Larghezza minima.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------|
| Libreria<br/> | <dl> <dt>Dwrite.lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>Dwrite.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout)
</dt> <dt>

[**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout)
</dt> </dl>

 


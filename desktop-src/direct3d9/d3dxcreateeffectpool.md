---
description: Creare un pool di effetti. Un pool viene usato per condividere parametri tra effetti.
ms.assetid: 5b202f85-b32b-4041-8873-0de535c2f59f
title: Funzione D3DXCreateEffectPool (D3DX9Effect. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateEffectPool
api_type:
- LibDef
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 14753500ac15fb0ed30d46b1121431af78e1fe93
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104235172"
---
# <a name="d3dxcreateeffectpool-function"></a>D3DXCreateEffectPool (funzione)

Creare un pool di effetti. Un pool viene usato per condividere parametri tra effetti.

## <a name="syntax"></a>Sintassi


```C++
HRESULT D3DXCreateEffectPool(
  _Out_ LPD3DXEFFECTPOOL *ppPool
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ppPool* \[ out\]
</dt> <dd>

Tipo: **[ **LPD3DXEFFECTPOOL**](id3dxeffectpool.md)\***

Restituisce un puntatore al pool creato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è \_ OK.

Se gli argomenti non sono validi, il metodo restituirà D3DERR \_ INVALIDCALL.

Se il metodo ha esito negativo, il valore restituito sarà E avrà \_ esito negativo.

## <a name="remarks"></a>Commenti

Per gli effetti all'interno di un pool, i parametri condivisi con lo stesso nome condividono i valori.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Effect. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni effetto](dx9-graphics-reference-effects-functions.md)
</dt> </dl>

 

 





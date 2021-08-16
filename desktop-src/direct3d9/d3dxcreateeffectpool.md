---
description: Creare un pool di effetti. Un pool viene usato per condividere i parametri tra gli effetti.
ms.assetid: 5b202f85-b32b-4041-8873-0de535c2f59f
title: Funzione D3DXCreateEffectPool (D3DX9Effect.h)
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
ms.openlocfilehash: 55df5e579b724a26e30223a0a0df7ffa815bda5a64b6f7d7e7e2c2c7f02f2fc1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118804577"
---
# <a name="d3dxcreateeffectpool-function"></a>Funzione D3DXCreateEffectPool

Creare un pool di effetti. Un pool viene usato per condividere i parametri tra gli effetti.

## <a name="syntax"></a>Sintassi


```C++
HRESULT D3DXCreateEffectPool(
  _Out_ LPD3DXEFFECTPOOL *ppPool
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ppPool* \[ Cambio\]
</dt> <dd>

Tipo: **[ **LPD3DXEFFECTPOOL**](id3dxeffectpool.md)\***

Restituisce un puntatore al pool creato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è S \_ OK.

Se gli argomenti non sono validi, il metodo restituirà D3DERR \_ INVALIDCALL.

Se il metodo ha esito negativo, il valore restituito sarà E \_ FAIL.

## <a name="remarks"></a>Commenti

Per gli effetti all'interno di un pool, i parametri condivisi con lo stesso nome condividono i valori.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Effect.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni degli effetti](dx9-graphics-reference-effects-functions.md)
</dt> </dl>

 

 





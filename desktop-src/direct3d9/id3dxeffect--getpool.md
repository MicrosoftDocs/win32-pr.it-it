---
description: Ottiene un puntatore al pool di parametri condivisi.
ms.assetid: 1e999fd5-76ef-43fa-8a77-ae6f2821f46d
title: Metodo ID3DXEffect::GetPool (D3DX9Effect.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.GetPool
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 0220b2864d6c668c2d4fbb71925da6452f6cc8661d0d931a379969418dfe7e19
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118521227"
---
# <a name="id3dxeffectgetpool-method"></a>Metodo ID3DXEffect::GetPool

Ottiene un puntatore al pool di parametri condivisi.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetPool(
  [out] LPD3DXEFFECTPOOL *ppPool
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ppPool* \[ Cambio\]
</dt> <dd>

Tipo: **[ **LPD3DXEFFECTPOOL**](id3dxeffectpool.md)\***

Puntatore a [**un oggetto ID3DXEffectPool.**](id3dxeffectpool.md)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Questo metodo restituisce sempre il valore S \_ OK.

## <a name="remarks"></a>Commenti

I pool contengono parametri condivisi tra gli effetti. Vedere [Clonazione e condivisione (Direct3D 9).](cloning-and-sharing.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Effect.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXEffect](id3dxeffect.md)
</dt> </dl>

 

 





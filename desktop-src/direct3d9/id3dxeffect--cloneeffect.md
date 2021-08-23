---
description: Crea una copia di un effetto.
ms.assetid: 6272bce0-b712-4a61-afe2-8f572993b03e
title: Metodo ID3DXEffect::CloneEffect (D3DX9Effect.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.CloneEffect
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: ab5ebe2898c1525d3a539121d1e57708c4713df3a06b43bfa41572f0e7b23b45
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119494261"
---
# <a name="id3dxeffectcloneeffect-method"></a>Metodo ID3DXEffect::CloneEffect

Crea una copia di un effetto.

## <a name="syntax"></a>Sintassi


```C++
HRESULT CloneEffect(
  [in]  LPDIRECT3DDEVICE9 pDevice,
  [out] LPD3DXEFFECT      *ppEffect
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pDevice* \[ Pollici\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Puntatore a [**un'interfaccia IDirect3DDevice9,**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) che rappresenta il dispositivo associato all'effetto.

</dd> <dt>

*ppEffect* \[ Cambio\]
</dt> <dd>

Tipo: **[ **LPD3DXEFFECT**](id3dxeffect.md)\***

Puntatore a [**un'interfaccia ID3DXEffect**](id3dxeffect.md) contenente l'effetto clonato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è S \_ OK. Se il metodo ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.

## <a name="remarks"></a>Commenti

> [!Note]  
> Questa funzione non clona un effetto se l'utente specifica [D3DXFX \_ NOT \_ CLONEABLE](d3dxfx.md) durante la creazione dell'effetto.

 

Per aggiornare i parametri condivisi e non condivisi in una tecnica attiva di un effetto clonato, vedere [**ID3DXEffect::CommitChanges**](id3dxeffect--commitchanges.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Effect.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXEffect](id3dxeffect.md)
</dt> </dl>

 

 

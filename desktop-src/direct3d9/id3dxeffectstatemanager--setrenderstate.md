---
description: Funzione di callback che deve essere implementata da un utente per impostare lo stato di rendering.
ms.assetid: a5a27e30-c141-44a4-b8d4-38c1d6076b2a
title: Metodo ID3DXEffectStateManager::SetRenderState (D3DX9Effect.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectStateManager.SetRenderState
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: c7d34dae1d0789b80d896b72be7e35420daf587986ac2725e880b81597b15e88
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119459621"
---
# <a name="id3dxeffectstatemanagersetrenderstate-method"></a>Metodo ID3DXEffectStateManager::SetRenderState

Funzione di callback che deve essere implementata da un utente per impostare lo stato di rendering.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetRenderState(
  [in] D3DRENDERSTATETYPE State,
  [in] DWORD              Value
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Stato* \[ Pollici\]
</dt> <dd>

Tipo: **[ **D3DRENDERSTATETYPE**](./d3drenderstatetype.md)**

Stato di rendering da impostare. [**D3DRENDERSTATETYPE**](./d3drenderstatetype.md)

</dd> <dt>

*Valore* \[ Pollici\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Valore dello stato di rendering. Vedere [Stati degli effetti (Direct3D 9).](effect-states.md)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Il metodo implementato dall'utente deve restituire S \_ OK. Se il callback non riesce quando si imposta lo stato del dispositivo, si verificherà una delle condizioni seguenti:

-   L'effetto avrà esito negativo [**durante ID3DXEffect::BeginPass**](id3dxeffect--beginpass.md).
-   La chiamata allo stato dell'effetto dinamico ( [**ad esempio IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate)) avrà esito negativo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Effect.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXEffectStateManager](id3dxeffectstatemanager.md)
</dt> </dl>

 

 

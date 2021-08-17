---
description: Funzione di callback che deve essere implementata da un utente per impostare un campionatore.
ms.assetid: 1e19e8cd-341d-4372-9182-8b3c82155407
title: Metodo ID3DXEffectStateManager::SetSamplerState (D3DX9Effect.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectStateManager.SetSamplerState
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 0227335c2110590439873b965b2d1393a42dd575bf530ce83aae5228547fda26
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119121477"
---
# <a name="id3dxeffectstatemanagersetsamplerstate-method"></a>Metodo ID3DXEffectStateManager::SetSamplerState

Funzione di callback che deve essere implementata da un utente per impostare un campionatore.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetSamplerState(
  [in] DWORD               Sampler,
  [in] D3DSAMPLERSTATETYPE Type,
  [in] DWORD               Value
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Campionatore* \[ Pollici\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Numero del campionatore in base zero.

</dd> <dt>

*Tipo* \[ Pollici\]
</dt> <dd>

Tipo: **[ **D3DSAMPLERSTATETYPE**](./d3dsamplerstatetype.md)**

Identifica lo stato del campionatore, che può specificare il filtro, l'indirizzamento o il colore del bordo. Vedere [**D3DSAMPLERSTATETYPE**](./d3dsamplerstatetype.md).

</dd> <dt>

*Valore* \[ Pollici\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Valore di uno dei tipi di stato del campionatore in Type.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Il metodo implementato dall'utente deve restituire S \_ OK. Se il callback ha esito negativo durante l'impostazione dello stato del dispositivo, si verificherà una delle condizioni seguenti:

-   L'effetto avrà esito negativo durante [**ID3DXEffect::BeginPass**](id3dxeffect--beginpass.md).
-   La chiamata allo stato dell'effetto dinamico ( [**ad esempio IDirect3DDevice9::SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate)) avrà esito negativo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Effect.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXEffectStateManager](id3dxeffectstatemanager.md)
</dt> </dl>

 

 

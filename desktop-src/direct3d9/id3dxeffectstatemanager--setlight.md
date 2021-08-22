---
description: Funzione di callback che deve essere implementata da un utente per impostare una luce.
ms.assetid: 3b9b2cbd-79f5-4ea4-a47b-da23b091adfd
title: Metodo ID3DXEffectStateManager::SetLight (D3DX9Effect.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectStateManager.SetLight
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 83250450a0510949267ffd52f17e6e9013a646d40229efcf7d5bcc7a396e1b09
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119372081"
---
# <a name="id3dxeffectstatemanagersetlight-method"></a>Metodo ID3DXEffectStateManager::SetLight

Funzione di callback che deve essere implementata da un utente per impostare una luce.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetLight(
  [in]       DWORD     Index,
  [in] const D3DLight9 *pLight
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Indice* \[ Pollici\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Indice in base zero della luce. Si tratta dello stesso indice in [**IDirect3DDevice9::SetLight**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setlight).

</dd> <dt>

*pLight* \[ Pollici\]
</dt> <dd>

Tipo: **const [**D3DLight9**](d3dlight9.md) \***

Oggetto chiaro. Vedere [**D3DLIGHT9.**](d3dlight9.md)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Il metodo implementato dall'utente deve restituire S \_ OK. Se il callback non riesce quando si imposta lo stato del dispositivo, si verificherà una delle condizioni seguenti:

-   L'effetto avrà esito negativo [**durante ID3DXEffect::BeginPass**](id3dxeffect--beginpass.md).
-   La chiamata dello stato dell'effetto dinamico ( [**ad esempio IDirect3DDevice9::SetLight**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setlight)) avrà esito negativo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Effect.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXEffectStateManager](id3dxeffectstatemanager.md)
</dt> </dl>

 

 

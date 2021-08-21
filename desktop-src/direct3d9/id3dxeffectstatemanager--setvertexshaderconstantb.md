---
description: 'Metodo ID3DXEffectStateManager::SetVertexShaderConstantB: funzione di callback che deve essere implementata da un utente per impostare una matrice di costanti booleane vertex shader.'
ms.assetid: 25fd0c68-11b5-4401-a2f8-86075ba3fa54
title: Metodo ID3DXEffectStateManager::SetVertexShaderConstantB (D3DX9Effect.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectStateManager.SetVertexShaderConstantB
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 0db8c141f16a14db57e5d6867a9894399bacf5a5cebb7c7e14a2592ea7f09bff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119121437"
---
# <a name="id3dxeffectstatemanagersetvertexshaderconstantb-method"></a>Metodo ID3DXEffectStateManager::SetVertexShaderConstantB

Funzione di callback che deve essere implementata da un utente per impostare una matrice di costanti booleane vertex shader.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetVertexShaderConstantB(
  [out]       UINT StartRegister,
  [out] const BOOL *pConstantData,
  [out]       UINT RegisterCount
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*StartRegister* \[ Cambio\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Indice in base zero del primo registro delle costanti.

</dd> <dt>

*pConstantData* \[ Cambio\]
</dt> <dd>

Tipo: **const [**BOOL**](../winprog/windows-data-types.md) \***

Matrice di costanti booleane.

</dd> <dt>

*RegisterCount* \[ Cambio\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Numero di registri in pConstantData.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Il metodo implementato dall'utente deve restituire S \_ OK. Se il callback ha esito negativo durante l'impostazione dello stato del dispositivo, si verificherà una delle condizioni seguenti:

-   L'effetto avrà esito negativo durante [**ID3DXEffect::BeginPass**](id3dxeffect--beginpass.md).
-   La chiamata allo stato dell'effetto dinamico ( ad esempio [**IDirect3DDevice9::SetVertexShaderConstantB**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshaderconstantb)) avrà esito negativo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Effect.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXEffectStateManager](id3dxeffectstatemanager.md)
</dt> </dl>

 

 

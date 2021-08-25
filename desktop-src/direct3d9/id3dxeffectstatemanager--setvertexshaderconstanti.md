---
description: 'Metodo ID3DXEffectStateManager::SetVertexShaderConstantI: funzione di callback che deve essere implementata da un utente per impostare una matrice di costanti integer di vertex shader.'
ms.assetid: 0035c97a-1b17-4665-9032-7b3b9a9d2cff
title: Metodo ID3DXEffectStateManager::SetVertexShaderConstantI (D3DX9Effect.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectStateManager.SetVertexShaderConstantI
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 949f2cb23e15e3cfb99fcb6880795cfbd6019a8c858198b23bb9db6508714d44
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119856691"
---
# <a name="id3dxeffectstatemanagersetvertexshaderconstanti-method"></a>Metodo ID3DXEffectStateManager::SetVertexShaderConstantI

Funzione di callback che deve essere implementata da un utente per impostare una matrice di costanti integer di vertex shader.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetVertexShaderConstantI(
  [out]       UINT StartRegister,
  [out] const INT  *pConstantData,
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

Tipo: **const [**INT**](../winprog/windows-data-types.md) \***

Matrice di costanti integer.

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
-   La chiamata allo stato dell'effetto dinamico ( ad esempio [**IDirect3DDevice9::SetVertexShaderConstantI**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshaderconstanti)) avrà esito negativo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Effect.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXEffectStateManager](id3dxeffectstatemanager.md)
</dt> </dl>

 

 

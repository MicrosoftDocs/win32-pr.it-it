---
description: Funzione di callback che deve essere implementata da un utente per impostare lo stato della fase della trama.
ms.assetid: cc86a483-ccf0-400d-b14d-ab55a3cf4b98
title: 'Metodo ID3DXEffectStateManager:: SetTextureStageState (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectStateManager.SetTextureStageState
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 937fd3f2b89dc093d9dceb9441f53d6be2cb06b5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323080"
---
# <a name="id3dxeffectstatemanagersettexturestagestate-method"></a>Metodo ID3DXEffectStateManager:: SetTextureStageState

Funzione di callback che deve essere implementata da un utente per impostare lo stato della fase della trama.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetTextureStageState(
  [in] DWORD                    Stage,
  [in] D3DTEXTURESTAGESTATETYPE Type,
  [in] DWORD                    Value
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Fase* \[ in\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Fase a cui è assegnata la trama. Si tratta del valore di indice in [**IDirect3DDevice9:: setexture**](/windows/desktop/api) o [**IDirect3DDevice9:: SetTextureStageState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate).

</dd> <dt>

*Tipo* \[ di in\]
</dt> <dd>

Tipo: **[ **D3DTEXTURESTAGESTATETYPE**](./d3dtexturestagestatetype.md)**

Definisce il tipo di operazione che viene eseguita da una fase della trama. Vedere [**D3DTEXTURESTAGESTATETYPE**](./d3dtexturestagestatetype.md).

</dd> <dt>

*Valore* \[ di in\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Può essere un'operazione ([**D3DTEXTUREOP**](./d3dtextureop.md)) o un valore di argomento ([D3DTA](d3dta.md)), a seconda di ciò che viene scelto per il tipo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Il metodo implementato dall'utente deve restituire S \_ OK. Se il callback ha esito negativo quando si imposta lo stato del dispositivo, si verificherà una delle condizioni seguenti:

-   L'effetto avrà esito negativo durante [**ID3DXEffect:: BeginPass**](id3dxeffect--beginpass.md).
-   La chiamata allo stato dell'effetto dinamico, ad esempio [**IDirect3DDevice9:: SetTextureStageState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate), avrà esito negativo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Effect. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXEffectStateManager](id3dxeffectstatemanager.md)
</dt> </dl>

 

 

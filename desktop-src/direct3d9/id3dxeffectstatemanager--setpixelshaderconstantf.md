---
description: Funzione di callback che deve essere implementata da un utente per impostare una matrice di costanti a virgola mobile del vertex shader.
ms.assetid: db87ca8c-2539-4d80-854c-25b114a7e7e0
title: 'Metodo ID3DXEffectStateManager:: SetPixelShaderConstantF (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectStateManager.SetPixelShaderConstantF
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 19e8654fbc851460fea932a8c858240c5e4631de
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323000"
---
# <a name="id3dxeffectstatemanagersetpixelshaderconstantf-method"></a>Metodo ID3DXEffectStateManager:: SetPixelShaderConstantF

Funzione di callback che deve essere implementata da un utente per impostare una matrice di costanti a virgola mobile del vertex shader.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetPixelShaderConstantF(
  [out]       UINT  StartRegister,
  [out] const FLOAT *pConstantData,
  [out]       UINT  RegisterCount
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*StartRegister* \[ out\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Indice in base zero del primo registro costante.

</dd> <dt>

*pConstantData* \[ out\]
</dt> <dd>

Tipo: **const [**float**](../winprog/windows-data-types.md) \***

Matrice di costanti a virgola mobile.

</dd> <dt>

*RegisterCount* \[ out\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Numero di registri in pConstantData.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Il metodo implementato dall'utente deve restituire S \_ OK. Se il callback ha esito negativo quando si imposta lo stato del dispositivo, si verificherà una delle condizioni seguenti:

-   L'effetto avrà esito negativo durante [**ID3DXEffect:: BeginPass**](id3dxeffect--beginpass.md).
-   La chiamata allo stato dell'effetto dinamico, ad esempio [**IDirect3DDevice9:: SetPixelShaderConstantF**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstantf), avrà esito negativo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Effect. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXEffectStateManager](id3dxeffectstatemanager.md)
</dt> </dl>

 

 

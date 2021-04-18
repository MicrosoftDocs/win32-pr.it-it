---
description: Funzione di callback che deve essere implementata da un utente per impostare lo stato del materiale.
ms.assetid: 4c5e903f-551b-4346-a5eb-301a3a5b9b44
title: 'Metodo ID3DXEffectStateManager:: sematerial (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectStateManager.SetMaterial
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: b503bd195468fb323e7e655c0bdd201e25dfdce2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323003"
---
# <a name="id3dxeffectstatemanagersetmaterial-method"></a>Metodo ID3DXEffectStateManager:: sematerial

Funzione di callback che deve essere implementata da un utente per impostare lo stato del materiale.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetMaterial(
  [in] const D3DMATERIAL9 *pMaterial
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pMaterial* \[ in\]
</dt> <dd>

Tipo: **const [**D3DMATERIAL9**](d3dmaterial9.md) \***

Puntatore allo stato del materiale. Vedere [**D3DMATERIAL9**](d3dmaterial9.md).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Il metodo implementato dall'utente deve restituire S \_ OK. Se il callback ha esito negativo quando si imposta lo stato del dispositivo, si verificherà una delle condizioni seguenti:

-   L'effetto avrà esito negativo durante [**ID3DXEffect:: BeginPass**](id3dxeffect--beginpass.md).
-   La chiamata allo stato dell'effetto dinamico, ad esempio [**IDirect3DDevice9:: sematerial**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setmaterial), avrà esito negativo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Effect. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXEffectStateManager](id3dxeffectstatemanager.md)
</dt> </dl>

 

 

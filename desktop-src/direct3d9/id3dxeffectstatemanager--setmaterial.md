---
description: Funzione di callback che deve essere implementata da un utente per impostare lo stato materiale.
ms.assetid: 4c5e903f-551b-4346-a5eb-301a3a5b9b44
title: Metodo ID3DXEffectStateManager::SetMaterial (D3DX9Effect.h)
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
ms.openlocfilehash: 67e8b1ad498b5aacbae7aaad2d6b63fa406d54d6315a4e75b3028efe3107eaf8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118802875"
---
# <a name="id3dxeffectstatemanagersetmaterial-method"></a>Metodo ID3DXEffectStateManager::SetMaterial

Funzione di callback che deve essere implementata da un utente per impostare lo stato materiale.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetMaterial(
  [in] const D3DMATERIAL9 *pMaterial
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pMaterial* \[ Pollici\]
</dt> <dd>

Tipo: **const [**D3DMATERIAL9**](d3dmaterial9.md) \***

Puntatore allo stato materiale. Vedere [**D3DMATERIAL9.**](d3dmaterial9.md)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Il metodo implementato dall'utente deve restituire S \_ OK. Se il callback non riesce quando si imposta lo stato del dispositivo, si verificherà una delle condizioni seguenti:

-   L'effetto avrà esito negativo [**durante ID3DXEffect::BeginPass**](id3dxeffect--beginpass.md).
-   La chiamata di stato dell'effetto dinamico ( [**ad esempio IDirect3DDevice9::SetMaterial**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setmaterial)) avrà esito negativo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Effect.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXEffectStateManager](id3dxeffectstatemanager.md)
</dt> </dl>

 

 

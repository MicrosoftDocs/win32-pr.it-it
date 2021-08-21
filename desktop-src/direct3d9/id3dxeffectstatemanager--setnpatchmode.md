---
description: Funzione di callback che deve essere implementata da un utente per impostare il numero di segmenti di suddivisione per N-patch.
ms.assetid: f94910ee-3385-44d3-b4f1-a0e88c7afa39
title: Metodo ID3DXEffectStateManager::SetNPatchMode (D3DX9Effect.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectStateManager.SetNPatchMode
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 220d0541e6779ab1a3d4f3e189175abd7da82b1c8b7f378522d0c9df11896e88
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119044429"
---
# <a name="id3dxeffectstatemanagersetnpatchmode-method"></a>Metodo ID3DXEffectStateManager::SetNPatchMode

Funzione di callback che deve essere implementata da un utente per impostare il numero di segmenti di suddivisione per N-patch.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetNPatchMode(
  [in] FLOAT nSegments
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*nSegments* \[ Pollici\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Suddividere la superficie in questo numero di suddivisioni. Corrisponde al numero usato da [**IDirect3DDevice9::SetNPatchMode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setnpatchmode).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Il metodo implementato dall'utente deve restituire S \_ OK. Se il callback ha esito negativo durante l'impostazione dello stato del dispositivo, si verificherà una delle condizioni seguenti:

-   L'effetto avrà esito negativo durante [**ID3DXEffect::BeginPass**](id3dxeffect--beginpass.md).
-   La chiamata allo stato dell'effetto dinamico , ad esempio [**IDirect3DDevice9::SetNPatchMode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setnpatchmode), avrà esito negativo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Effect.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXEffectStateManager](id3dxeffectstatemanager.md)
</dt> </dl>

 

 

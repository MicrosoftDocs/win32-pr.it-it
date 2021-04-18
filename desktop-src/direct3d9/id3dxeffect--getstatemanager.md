---
description: Ottenere il gestore degli Stati dell'effetto.
ms.assetid: 4a09eb2a-2393-40b0-81b9-3c27998c2b77
title: 'Metodo ID3DXEffect:: GetStateManager (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.GetStateManager
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 293b642dfecfa4cc14426addf2567d43dffa7233
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322358"
---
# <a name="id3dxeffectgetstatemanager-method"></a>Metodo ID3DXEffect:: GetStateManager

Ottenere il gestore degli Stati dell'effetto.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetStateManager(
  [out] LPD3DXEFFECTSTATEMANAGER *ppManager
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ppManager* \[ out\]
</dt> <dd>

Tipo: **[ **LPD3DXEFFECTSTATEMANAGER**](id3dxeffectstatemanager.md)\***

Restituisce un puntatore al gestore di stato. Vedere [**ID3DXEffectStateManager**](id3dxeffectstatemanager.md).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è D3D \_ OK. Se il metodo ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.

## <a name="remarks"></a>Commenti

[**ID3DXEffectStateManager**](id3dxeffectstatemanager.md) è un'interfaccia implementata dall'utente che fornisce callback in un'applicazione per l'impostazione dello stato del dispositivo da un effetto.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Effect. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXEffect](id3dxeffect.md)
</dt> <dt>

[**ID3DXEffect::SetStateManager**](id3dxeffect--setstatemanager.md)
</dt> </dl>

 

 





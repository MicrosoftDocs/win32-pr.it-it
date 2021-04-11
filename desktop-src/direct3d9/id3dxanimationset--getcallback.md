---
description: Ottiene informazioni su un callback specifico nel set di animazioni.
ms.assetid: e8388bfc-5438-4216-a98f-dd0dbca12c87
title: 'Metodo ID3DXAnimationSet:: getCallback (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationSet.GetCallback
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f4cde6c9d51fd29c0412f33b34ca7bea8260dfea
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104235203"
---
# <a name="id3dxanimationsetgetcallback-method"></a>Metodo ID3DXAnimationSet:: getCallback

Ottiene informazioni su un callback specifico nel set di animazioni.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetCallback(
  [in]  DOUBLE Position,
  [in]  DWORD  Flags,
  [out] DOUBLE *pCallbackPosition,
  [out] LPVOID *ppCallbackData
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Posizione* \[ in\]
</dt> <dd>

Tipo: **[ **Double**](../winprog/windows-data-types.md)**

Posizione da cui trovare i callback.

</dd> <dt>

*Flag* \[ in\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Flag di ricerca di callback. Questo parametro può essere impostato su una combinazione di uno o più flag dei [**\_ \_ flag di ricerca D3DXCALLBACK**](./d3dxcallback-search-flags.md).

</dd> <dt>

*pCallbackPosition* \[ out\]
</dt> <dd>

Tipo: **[ **Double**](../winprog/windows-data-types.md)\***

Puntatore alla posizione del callback.

</dd> <dt>

*ppCallbackData* \[ out\]
</dt> <dd>

Tipo: **[ **LPVOID**](../winprog/windows-data-types.md)\***

Indirizzo del puntatore ai dati di callback.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

I valori restituiti da questo metodo sono implementati da un programmatore di applicazioni. In generale, se non si verificano errori, programmare il metodo per restituire D3D \_ OK. In caso contrario, programmare il metodo per restituire un messaggio di errore appropriato da [D3DERR](d3derr.md) o [**D3DXERR**](./d3dxerr.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXAnimationSet](id3dxanimationset.md)
</dt> </dl>

 

 

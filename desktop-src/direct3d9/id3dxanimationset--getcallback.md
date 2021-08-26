---
description: 'Metodo ID3DXAnimationSet::GetCallback: ottiene informazioni su un callback specifico nel set di animazioni.'
ms.assetid: e8388bfc-5438-4216-a98f-dd0dbca12c87
title: Metodo ID3DXAnimationSet::GetCallback (D3dx9anim.h)
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
ms.openlocfilehash: 4ded66bbe90320250667511d1c9468073693ce789cdb7add8574f42a4756136d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120026591"
---
# <a name="id3dxanimationsetgetcallback-method"></a>Metodo ID3DXAnimationSet::GetCallback

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

*Posizione* \[ Pollici\]
</dt> <dd>

Tipo: **[ **DOUBLE**](../winprog/windows-data-types.md)**

Posizione da cui trovare i callback.

</dd> <dt>

*Flag* \[ Pollici\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Flag di ricerca di callback. Questo parametro può essere impostato su una combinazione di uno o più flag [**di D3DXCALLBACK \_ SEARCH \_ FLAGS**](./d3dxcallback-search-flags.md).

</dd> <dt>

*pCallbackPosition* \[ Cambio\]
</dt> <dd>

Tipo: **[ **DOUBLE**](../winprog/windows-data-types.md)\***

Puntatore alla posizione del callback.

</dd> <dt>

*ppCallbackData* \[ Cambio\]
</dt> <dd>

Tipo: **[ **LPVOID**](../winprog/windows-data-types.md)\***

Indirizzo del puntatore ai dati di callback.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

I valori restituiti di questo metodo vengono implementati da un programmatore di applicazioni. In generale, se non si verifica alcun errore, programmare il metodo per restituire D3D \_ OK. In caso contrario, programmare il metodo per restituire un messaggio di errore appropriato [da D3DERR](d3derr.md) o [**D3DXERR**](./d3dxerr.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9anim.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXAnimationSet](id3dxanimationset.md)
</dt> </dl>

 

 

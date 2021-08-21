---
description: Ottiene il nome di un'animazione, in base al relativo indice.
ms.assetid: vs|directx_sdk|~\id3dxanimationset__getanimationnamebyindex.htm
title: Metodo ID3DXAnimationSet::GetAnimationNameByIndex (D3dx9anim.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationSet.GetAnimationNameByIndex
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: dfcc939cb498906ad57798bdb1fd2891f060b067cff76255123e48b24bce955f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118987801"
---
# <a name="id3dxanimationsetgetanimationnamebyindex-method"></a>Metodo ID3DXAnimationSet::GetAnimationNameByIndex

Ottiene il nome di un'animazione, in base al relativo indice.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetAnimationNameByIndex(
  [in]  UINT   Index,
  [out] LPCSTR *ppName
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Indice* \[ Pollici\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Indice dell'animazione.

</dd> <dt>

*ppName* \[ Cambio\]
</dt> <dd>

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)\***

Indirizzo di un puntatore a una stringa che riceve il nome dell'animazione.

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

 

 

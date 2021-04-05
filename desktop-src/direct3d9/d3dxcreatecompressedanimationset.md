---
description: Crea un'interfaccia del set di animazioni con fotogrammi chiave ID3DXCompressedAnimationSet che archivia i dati del fotogramma chiave in un formato compresso.
ms.assetid: c3f97d35-5654-4d85-a337-d77819ce3874
title: Funzione D3DXCreateCompressedAnimationSet (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateCompressedAnimationSet
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8aab23466cecf43a50a4136eb0b3d93a271dcb0e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103969382"
---
# <a name="d3dxcreatecompressedanimationset-function"></a>D3DXCreateCompressedAnimationSet (funzione)

Crea un'interfaccia del set di animazioni con fotogrammi chiave [**ID3DXCompressedAnimationSet**](id3dxcompressedanimationset.md) che archivia i dati del fotogramma chiave in un formato compresso.

## <a name="syntax"></a>Sintassi


```C++
HRESULT D3DXCreateCompressedAnimationSet(
  _In_        LPCSTR                       pName,
  _In_        DOUBLE                       TicksPerSecond,
  _In_        D3DXPLAYBACK_TYPE            Playback,
  _In_        LPD3DXBUFFER                 pCompressedData,
  _In_        UINT                         NumCallbackKeys,
  _In_  const LPD3DXKEY_CALLBACK           *pCallKeys,
  _Out_       LPD3DXCOMPRESSEDANIMATIONSET *ppAnimationSet
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pname* \[ in\]
</dt> <dd>

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Puntatore al nome del set di animazioni.

</dd> <dt>

*TicksPerSecond* \[ in\]
</dt> <dd>

Tipo: **[ **Double**](../winprog/windows-data-types.md)**

Numero di cicli del fotogramma chiave che intercorrono al secondo.

</dd> <dt>

*Riproduzione* \[ in esecuzione in\]
</dt> <dd>

Tipo: **[ **D3DXPLAYBACK \_**](./d3dxplayback-type.md)**

Tipo del ciclo di riproduzione del set di animazioni. Vedere [**D3DXPLAYBACK \_ Type**](./d3dxplayback-type.md).

</dd> <dt>

*pCompressedData* \[ in\]
</dt> <dd>

Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)**

Puntatore al buffer [**ID3DXBuffer**](id3dxbuffer.md) che archivia il set di animazioni come dati compressi.

</dd> <dt>

*NumCallbackKeys* \[ in\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Numero di chiavi di callback.

</dd> <dt>

*pCallKeys* \[ in\]
</dt> <dd>

Tipo: **const [**LPD3DXKEY \_ callback**](d3dxkey-callback.md) \***

Puntatore a una struttura di [**\_ callback D3DXKEY**](d3dxkey-callback.md) che archivia i dati di callback utente.

</dd> <dt>

*ppAnimationSet* \[ out\]
</dt> <dd>

Tipo: **[ **LPD3DXCOMPRESSEDANIMATIONSET**](id3dxcompressedanimationset.md)\***

Indirizzo di un puntatore all'interfaccia [**ID3DXCompressedAnimationSet**](id3dxcompressedanimationset.md) che archivia i dati del set di animazioni con fotogrammi chiave in un formato compresso.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se la funzione ha esito positivo, il valore restituito è \_ OK. Se la funzione ha esito negativo, il valore restituito può essere uno dei valori seguenti: D3DERR \_ INVALIDCALL, E \_ OutOfMemory.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni di animazione](dx9-graphics-reference-d3dx-functions-animation.md)
</dt> </dl>

 

 

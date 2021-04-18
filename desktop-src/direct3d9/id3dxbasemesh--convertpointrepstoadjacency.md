---
description: Converte i dati rappresentativi del punto in informazioni adiacenza mesh.
ms.assetid: 6ae40486-74be-45a8-9971-f20517c8dcf0
title: 'Metodo ID3DXBaseMesh:: ConvertPointRepsToAdjacency (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseMesh.ConvertPointRepsToAdjacency
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b1c38d7790d575bdf6794e0e21f1c4043e80257c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322554"
---
# <a name="id3dxbasemeshconvertpointrepstoadjacency-method"></a>Metodo ID3DXBaseMesh:: ConvertPointRepsToAdjacency

Converte i dati rappresentativi del punto in informazioni adiacenza mesh.

## <a name="syntax"></a>Sintassi


```C++
HRESULT ConvertPointRepsToAdjacency(
  [in]      const DWORD *pPRep,
  [in, out]       DWORD *pAdjacency
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pPRep* \[ in\]
</dt> <dd>

Tipo: **const [**DWORD**](../winprog/windows-data-types.md) \***

Puntatore a una matrice di un valore DWORD per vertice della mesh che contiene i dati rappresentativi del punto. Questo parametro è facoltativo. Se si specifica un valore **null** , questo parametro verrà interpretato come una matrice di identità.

</dd> <dt>

*pAdjacency* \[ in uscita\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***

Puntatore a una matrice di tre DWORD per ogni volto che specifica i tre elementi adiacenti per ogni viso nella mesh. Il numero di byte in questa matrice deve essere almeno 3 \* [**ID3DXBaseMesh:: GetNumFaces**](id3dxbasemesh--getnumfaces.md) \* sizeof (DWORD).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è D3D \_ OK. Se il metodo ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, E \_ OutOfMemory.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXBaseMesh](id3dxbasemesh.md)
</dt> </dl>

 

 

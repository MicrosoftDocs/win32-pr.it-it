---
description: Genera un nuovo mapping ottimizzato del viso per un elenco di triangoli.
ms.assetid: 428c2af8-43e7-4cf7-8b9b-04ba5cff82c8
title: Funzione D3DXOptimizeFaces (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXOptimizeFaces
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 165f81d9b829ce7a7b22ced6fb37851f926ed861f11b79feca3a63c763dabbb7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118525230"
---
# <a name="d3dxoptimizefaces-function"></a>Funzione D3DXOptimizeFaces

Genera un nuovo mapping ottimizzato del viso per un elenco di triangoli.

## <a name="syntax"></a>Sintassi


```C++
HRESULT D3DXOptimizeFaces(
  _In_    LPCVOID pIndices,
  _In_    UINT    NumFaces,
  _In_    UINT    NumVertices,
  _In_    BOOL    Indices32Bit,
  _Inout_ DWORD   *pFaceRemap
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pIndices* \[ Pollici\]
</dt> <dd>

Tipo: **[ **LPCVOID**](../winprog/windows-data-types.md)**

Puntatore agli indici dell'elenco triangolare da usare per l'ordinamento dei vertici.

</dd> <dt>

*NumFaces* \[ Pollici\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Numero di visi nell'elenco di triangoli. Per le mesh a 16 bit, questo limite è di 2^16 - 1 (65535) o meno visi.

</dd> <dt>

*NumVertices* \[ Pollici\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Numero di vertici a cui fa riferimento l'elenco di triangoli.

</dd> <dt>

*Indices32Bit* \[ Pollici\]
</dt> <dd>

Tipo: **[ **BOOL**](../winprog/windows-data-types.md)**

Flag che indica il tipo di indice: **TRUE** se gli indici sono a 32 bit (più di 65535 indici), **FALSE** se gli indici sono a 16 bit (65535 o meno indici).

</dd> <dt>

*pFaceRemap* \[ in, out\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***

Puntatore alla faccia mesh originale divisa per generare la faccia corrente.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se la funzione ha esito positivo, il valore restituito è D3D \_ OK. Se la funzione ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Commenti

Dal punto di vista funzionale, la procedura di ottimizzazione di questa funzione equivale a chiamare [**ID3DXMesh::Optimize**](id3dxmesh--optimize.md) con il flag D3DXMESHOPT DEVICEINDEPENDENT, ma questa funzione usa in modo più efficiente le \_ cache dei vertici.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni mesh](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 

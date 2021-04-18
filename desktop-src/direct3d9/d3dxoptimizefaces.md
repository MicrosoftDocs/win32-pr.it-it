---
description: Genera un nuovo mapping del volto ottimizzato per un elenco di triangolo.
ms.assetid: 428c2af8-43e7-4cf7-8b9b-04ba5cff82c8
title: Funzione D3DXOptimizeFaces (D3DX9Mesh. h)
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
ms.openlocfilehash: 6c56dec04e01b542d2c760852a58826a8186c213
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322119"
---
# <a name="d3dxoptimizefaces-function"></a>D3DXOptimizeFaces (funzione)

Genera un nuovo mapping del volto ottimizzato per un elenco di triangolo.

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

*pIndices* \[ in\]
</dt> <dd>

Tipo: **[ **LPCVOID**](../winprog/windows-data-types.md)**

Puntatore agli indici di elenco di triangolo da usare per l'ordinamento dei vertici.

</dd> <dt>

*NumFaces* \[ in\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Numero di visi nell'elenco dei triangoli. Per le mesh a 16 bit, questo limite è di 2 ^ 16-1 (65535) o di un numero inferiore di visi.

</dd> <dt>

*NumVertices* \[ in\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Numero di vertici a cui fa riferimento l'elenco dei triangoli.

</dd> <dt>

*Indices32Bit* \[ in\]
</dt> <dd>

Tipo: **[ **bool**](../winprog/windows-data-types.md)**

Flag che indica il tipo di indice: **true** se gli indici sono a 32 bit (più di 65535 indici); **false** se gli indici sono a 16 bit (65535 o un numero inferiore di indici).

</dd> <dt>

*pFaceRemap* \[ in uscita\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***

Puntatore al quadrante mesh originale diviso per generare la faccia corrente.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se la funzione ha esito positivo, il valore restituito è D3D \_ OK. Se la funzione ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, E \_ OutOfMemory.

## <a name="remarks"></a>Commenti

La procedura di ottimizzazione di questa funzione è equivalente dal punto di vista funzionale alla chiamata a [**ID3DXMesh:: Optimize**](id3dxmesh--optimize.md) con il \_ flag D3DXMESHOPT DEVICEINDEPENDENT, ma questa funzione consente un uso più efficiente delle cache dei vertici.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni mesh](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 

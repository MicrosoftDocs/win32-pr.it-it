---
description: Converte il subset di mesh specificato in una serie di strisce.
ms.assetid: 4f005383-6a5a-4393-ac88-202e45946d3d
title: Funzione D3DXConvertMeshSubsetToStrips (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXConvertMeshSubsetToStrips
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 345c80305f42df410f42cf255f1b9e0d8f353b448134779b416d686db4b40c05
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118526789"
---
# <a name="d3dxconvertmeshsubsettostrips-function"></a>Funzione D3DXConvertMeshSubsetToStrips

Converte il subset di mesh specificato in una serie di strisce.

## <a name="syntax"></a>Sintassi


```C++
HRESULT D3DXConvertMeshSubsetToStrips(
  _In_  LPD3DXBASEMESH         MeshIn,
  _In_  DWORD                  AttribId,
  _In_  DWORD                  IBOptions,
  _Out_ LPDIRECT3DINDEXBUFFER9 *ppIndexBuffer,
  _Out_ DWORD                  *pNumIndices,
  _Out_ LPD3DXBUFFER           *ppStripLengths,
  _Out_ DWORD                  *pNumStrips
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*MeshIn* \[ Pollici\]
</dt> <dd>

Tipo: **[ **LPD3DXBASEMESH**](id3dxbasemesh.md)**

Puntatore a [**un'interfaccia ID3DXBaseMesh,**](id3dxbasemesh.md) che rappresenta la mesh da convertire in una striscia.

</dd> <dt>

*AttribId* \[ Pollici\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

ID attributo del subset di mesh da convertire in strisce.

</dd> <dt>

*Opzioni IB* \[ Pollici\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Combinazione di uno o più flag [**dell'enumerazione D3DXMESH,**](./d3dxmesh.md) specificando le opzioni per la creazione del index buffer. Non può essere D3DXMESH \_ a 32 BIT. Il index buffer verrà creato con indici a 32 o 16 bit a seconda del formato del index buffer della mesh specificato dal *parametro MeshIn.*

</dd> <dt>

*ppIndexBuffer* \[ Cambio\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DINDEXBUFFER9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dindexbuffer9)\***

Puntatore a [**un'interfaccia IDirect3DIndexBuffer9,**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dindexbuffer9) che rappresenta index buffer contenente la striscia.

</dd> <dt>

*pNumIndices* \[ Cambio\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***

Numero di indici nel buffer restituiti nel *parametro ppIndexBuffer.*

</dd> <dt>

*ppStripLengths* \[ Cambio\]
</dt> <dd>

Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Buffer contenente una matrice di un valore DWORD per ogni striscia, che specifica il numero di triangoli nell'elenco.

</dd> <dt>

*pNumStrips* \[ Cambio\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***

Numero di singole strisce nella matrice index buffer e la matrice di lunghezza della striscia corrispondente.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se la funzione ha esito positivo, il valore restituito è D3D \_ OK. Se la funzione ha esito negativo, il valore restituito può essere uno dei valori seguenti: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Commenti

Prima di eseguire questa funzione, chiamare [**Optimize**](id3dxmesh--optimize.md) o [**D3DXOptimizeFaces**](d3dxoptimizefaces.md)con il flag ATTRSORT D3DXMESHOPT \_ impostato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni mesh](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 

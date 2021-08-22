---
description: Pulisce una mesh, prepararla per la semplificazione.
ms.assetid: 2b586ecc-db87-4b20-a4fc-c8b547bebf65
title: Funzione D3DXCleanMesh (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCleanMesh
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: adc5d60b66dc9eaa06314e18ead26412b8572e9dbc649070c37891a62fb9ecbe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119495911"
---
# <a name="d3dxcleanmesh-function"></a>Funzione D3DXCleanMesh

Pulisce una mesh, prepararla per la semplificazione.

## <a name="syntax"></a>Sintassi


```C++
HRESULT D3DXCleanMesh(
  _In_        D3DXCLEANTYPE CleanType,
  _In_        LPD3DXMESH    pMeshIn,
  _In_  const DWORD         *pAdjacencyIn,
  _Out_       LPD3DXMESH    *ppMeshOut,
  _Out_       DWORD         *pAdjacencyOut,
  _Out_       LPD3DXBUFFER  *ppErrorsAndWarnings
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*CleanType* \[ Pollici\]
</dt> <dd>

Tipo: **[ **D3DXCLEANTYPE**](./d3dxcleantype.md)**

Operazioni sui vertici da eseguire in preparazione per la pulizia della mesh. Vedere [**D3DXCLEANTYPE.**](./d3dxcleantype.md)

</dd> <dt>

*pMeshIn* \[ Pollici\]
</dt> <dd>

Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)**

Puntatore a [**un'interfaccia ID3DXMesh**](id3dxmesh.md) che rappresenta la mesh da pulire.

</dd> <dt>

*pAdjacencyIn* \[ Pollici\]
</dt> <dd>

Tipo: **const [**DWORD**](../winprog/windows-data-types.md) \***

Puntatore a una matrice di tre DWORD per viso che specificano i tre vicini per ogni viso nella mesh da pulire.

</dd> <dt>

*ppMeshOut* \[ Cambio\]
</dt> <dd>

Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)\***

Indirizzo di un puntatore a [**un'interfaccia ID3DXMesh,**](id3dxmesh.md) che rappresenta la mesh pulita restituita. Viene restituita la stessa mesh passata se non è necessaria alcuna pulizia.

</dd> <dt>

*pAdjacencyOut* \[ Cambio\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***

Puntatore a una matrice di tre DWORD per viso che specificano i tre elementi adiacenti per ogni viso nella mesh di output.

</dd> <dt>

*ppErrorsAndWarnings* \[ Cambio\]
</dt> <dd>

Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Restituisce un buffer contenente una stringa di errori e avvisi che illustrano i problemi rilevati nella rete.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se la funzione ha esito positivo, il valore restituito è D3D \_ OK. Se la funzione ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Commenti

Questa funzione pulisce una mesh usando il metodo di pulizia e le opzioni specificate nel parametro CleanType. Per una descrizione delle opzioni disponibili, vedere l'enumerazione [**D3DXCLEANTYPE**](./d3dxcleantype.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni mesh](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 

---
description: 'Metodo ID3DXMesh::Optimize: genera una nuova mesh con visi e vertici riordinati per ottimizzare le prestazioni del disegno.'
ms.assetid: 6a9bf7b9-2cb9-4b42-92d9-2a121ff79284
title: Metodo ID3DXMesh::Optimize (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMesh.Optimize
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: debec1c0ee54e612ab0de832dbc5c2481dcefad8
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108093309"
---
# <a name="id3dxmeshoptimize-method"></a>Metodo ID3DXMesh::Optimize

Genera una nuova mesh con visi e vertici riordinati per ottimizzare le prestazioni del disegno.

## <a name="syntax"></a>Sintassi


```C++
HRESULT Optimize(
  [in]            DWORD        Flags,
  [in]      const DWORD        *pAdjacencyIn,
  [in, out]       DWORD        *pAdjacencyOut,
  [in, out]       DWORD        *pFaceRemap,
  [out]           LPD3DXBUFFER *ppVertexRemap,
  [out]           LPD3DXMESH   *ppOptMesh
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Flag* \[ Pollici\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Specifica il tipo di ottimizzazione da eseguire. Questo parametro può essere impostato su una combinazione di uno o più flag [**di D3DXMESHOPT**](./d3dxmeshopt.md) e [**D3DXMESH**](./d3dxmesh.md) (ad eccezione di D3DXMESH \_ 32BIT, D3DXMESH \_ IB \_ WRITEONLY e D3DXMESH \_ WRITEONLY).

</dd> <dt>

*pAdjacencyIn* \[ Pollici\]
</dt> <dd>

Tipo: **const [**DWORD**](../winprog/windows-data-types.md) \***

Puntatore a una matrice di tre DWORD per ogni viso che specifica i tre elementi adiacenti per ogni viso nella mesh di origine. Se il bordo non ha visi adiacenti, il valore è 0xffffffff. Vedere la sezione Osservazioni.

</dd> <dt>

*pAdjacencyOut* \[ in, out\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***

Puntatore a una matrice di tre DWORD per ogni viso che specifica i tre elementi adiacenti per ogni viso nella mesh ottimizzata. Se il bordo non ha visi adiacenti, il valore è 0xffffffff.

</dd> <dt>

*pFaceRemap* \[ in, out\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***

Matrice di DWORD, uno per ogni viso, che identifica il viso della mesh originale corrispondente a ogni viso nella mesh ottimizzata. Se il valore fornito per questo argomento è **NULL,** i dati di modifica del mapping dei visi non vengono restituiti.

</dd> <dt>

*ppVertexRemap* \[ Cambio\]
</dt> <dd>

Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Indirizzo di un puntatore a un'interfaccia [**ID3DXBuffer,**](id3dxbuffer.md) che contiene un valore DWORD per ogni vertice che specifica il mapping dei nuovi vertici ai vertici vecchi. Questo nuovo mapping è utile se è necessario modificare i dati esterni in base al nuovo mapping dei vertici.

</dd> <dt>

*ppOptMesh* \[ Cambio\]
</dt> <dd>

Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)\***

Indirizzo di un puntatore a [**un'interfaccia ID3DXMesh,**](id3dxmesh.md) che rappresenta la mesh ottimizzata.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è D3D \_ OK. Se il metodo ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Commenti

Questo metodo genera una nuova mesh. Prima di eseguire Optimize, un'applicazione deve generare un buffer di adiacenza chiamando [**ID3DXBaseMesh::GenerateAdjacency**](id3dxbasemesh--generateadjacency.md). Il buffer di adienze contiene dati di adizia, ad esempio un elenco di bordi e le facce adiacenti l'una all'altra.

Questo metodo è molto simile al metodo [**ID3DXBaseMesh::CloneMesh,**](id3dxbasemesh--clonemesh.md) ad eccezione del fatto che può eseguire l'ottimizzazione durante la generazione del nuovo clone della mesh. La mesh di output eredita tutti i parametri di creazione della mesh di input.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXMesh](id3dxmesh.md)
</dt> <dt>

[**ID3DXMesh::OptimizeInplace**](id3dxmesh--optimizeinplace.md)
</dt> </dl>

 

 

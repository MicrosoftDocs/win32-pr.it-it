---
description: Genera una nuova mesh con visi e vertici riordinati per ottimizzare le prestazioni del disegno.
ms.assetid: 6a9bf7b9-2cb9-4b42-92d9-2a121ff79284
title: 'Metodo ID3DXMesh:: Optimize (D3DX9Mesh. h)'
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
ms.openlocfilehash: 7752e08236094d7038a5e77ac1a679f787305022
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103969522"
---
# <a name="id3dxmeshoptimize-method"></a>Metodo ID3DXMesh:: Optimize

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

*Flag* \[ in\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Specifica il tipo di ottimizzazione da eseguire. Questo parametro può essere impostato su una combinazione di uno o più flag di [**D3DXMESHOPT**](./d3dxmeshopt.md) e [**D3DXMESH**](./d3dxmesh.md) (eccetto D3DXMESH a \_ 32 bit, D3DXMESH \_ IB \_ WRITEONLY e D3DXMESH \_ WRITEONLY).

</dd> <dt>

*pAdjacencyIn* \[ in\]
</dt> <dd>

Tipo: **const [**DWORD**](../winprog/windows-data-types.md) \***

Puntatore a una matrice di tre DWORD per ogni volto che specifica i tre elementi adiacenti per ogni viso nella mesh di origine. Se il bordo non ha visi adiacenti, il valore è 0xFFFFFFFF. Vedere la sezione Osservazioni.

</dd> <dt>

*pAdjacencyOut* \[ in uscita\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***

Puntatore a una matrice di tre DWORD per ogni volto che specifica i tre elementi adiacenti per ogni viso nella mesh ottimizzata. Se il bordo non ha visi adiacenti, il valore è 0xFFFFFFFF.

</dd> <dt>

*pFaceRemap* \[ in uscita\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***

Matrice di DWORD, una per ogni volto, che identifica la faccia mesh originale che corrisponde a ogni face nella mesh ottimizzata. Se il valore fornito per questo argomento è **null**, non vengono restituiti i dati di riassociazione della faccia.

</dd> <dt>

*ppVertexRemap* \[ out\]
</dt> <dd>

Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Indirizzo di un puntatore a un'interfaccia [**ID3DXBuffer**](id3dxbuffer.md) , che contiene un valore DWORD per ogni vertice che specifica la modalità di mapping dei nuovi vertici ai vertici precedenti. Questo mapping è utile se è necessario modificare i dati esterni in base al nuovo mapping dei vertici.

</dd> <dt>

*ppOptMesh* \[ out\]
</dt> <dd>

Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)\***

Indirizzo di un puntatore a un'interfaccia [**ID3DXMesh**](id3dxmesh.md) , che rappresenta la mesh ottimizzata.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è D3D \_ OK. Se il metodo ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, E \_ OutOfMemory.

## <a name="remarks"></a>Commenti

Questo metodo genera una nuova mesh. Prima di eseguire l'ottimizzazione, un'applicazione deve generare un buffer adiacenza chiamando [**ID3DXBaseMesh:: GenerateAdjacency**](id3dxbasemesh--generateadjacency.md). Il buffer adiacenza contiene dati adiacenza, ad esempio un elenco di bordi e i visi adiacenti.

Questo metodo è molto simile al metodo [**ID3DXBaseMesh:: CloneMesh**](id3dxbasemesh--clonemesh.md) , ad eccezione del fatto che può eseguire l'ottimizzazione durante la generazione del nuovo clone della mesh. La mesh di output eredita tutti i parametri di creazione della mesh di input.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXMesh](id3dxmesh.md)
</dt> <dt>

[**ID3DXMesh:: OptimizeInplace**](id3dxmesh--optimizeinplace.md)
</dt> </dl>

 

 

---
description: Genera una mesh con visi e vertici riordinati per ottimizzare le prestazioni del disegno. Questo metodo riordina la mesh esistente.
ms.assetid: 2cdaf627-d1d3-44f0-a5ae-9023d4b0de45
title: Metodo ID3DXMesh::OptimizeInplace (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMesh.OptimizeInplace
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 0075e7a0b823f0d747859a4717a440e0c244fde76076e4b285c7d1b2a7e78d00
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119120805"
---
# <a name="id3dxmeshoptimizeinplace-method"></a>Metodo ID3DXMesh::OptimizeInplace

Genera una mesh con visi e vertici riordinati per ottimizzare le prestazioni del disegno. Questo metodo riordina la mesh esistente.

## <a name="syntax"></a>Sintassi


```C++
HRESULT OptimizeInplace(
  [in]        DWORD        Flags,
  [in]  const DWORD        *pAdjacencyIn,
  [out]       DWORD        *pAdjacencyOut,
  [out]       DWORD        *pFaceRemap,
  [out]       LPD3DXBUFFER *ppVertexRemap
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Flag* \[ Pollici\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Combinazione di uno o [**più flag D3DXMESHOPT,**](./d3dxmeshopt.md) specificando il tipo di ottimizzazione da eseguire.

</dd> <dt>

*pAdjacencyIn* \[ Pollici\]
</dt> <dd>

Tipo: **const [**DWORD**](../winprog/windows-data-types.md) \***

Puntatore a una matrice di tre DWORD per ogni viso che specifica i tre elementi adiacenti per ogni viso nella mesh di origine. Se il bordo non ha visi adiacenti, il valore è 0xffffffff.

</dd> <dt>

*pAdjacencyOut* \[ Cambio\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***

Puntatore a una matrice di tre DWORD per viso che specifica i tre elementi adiacenti per ogni viso nella mesh ottimizzata. Se il bordo non ha visi adiacenti, il valore è 0xffffffff. Se il valore fornito per questo argomento è **NULL,** i dati di adienza non vengono restituiti.

</dd> <dt>

*pFaceRemap* \[ Cambio\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***

Matrice di DWORD, uno per ogni viso, che identifica il viso della mesh originale corrispondente a ogni viso nella mesh ottimizzata. Se il valore fornito per questo argomento è **NULL,** i dati di modifica del mapping dei visi non vengono restituiti.

</dd> <dt>

*ppVertexRemap* \[ Cambio\]
</dt> <dd>

Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Indirizzo di un puntatore a [**un'interfaccia ID3DXBuffer,**](id3dxbuffer.md) che contiene un valore DWORD per ogni vertice che specifica il mapping dei nuovi vertici ai vertici vecchi. Questo nuovo mapping è utile se è necessario modificare i dati esterni in base al nuovo mapping dei vertici. Se il valore fornito per questo argomento è **NULL,** i dati di ridefinizione dei vertici non vengono restituiti.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è D3D \_ OK. Se il metodo ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, D3DXERR \_ CANNOTATTRSORT, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Commenti

Prima di **eseguire ID3DXMesh::OptimizeInplace,** un'applicazione deve generare un buffer di adiacenza chiamando [**ID3DXBaseMesh::GenerateAdjacency**](id3dxbasemesh--generateadjacency.md). Il buffer di adienza contiene dati di adicenza, ad esempio un elenco di bordi e visi adiacenti.

> [!Note]  
> Questo metodo avrà esito negativo se la mesh condivide il buffer dei vertici con un'altra mesh, a meno che D3DXMESHOPT IGNOREVERTS non sia \_ impostato in Flag.

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXMesh](id3dxmesh.md)
</dt> <dt>

[**ID3DXMesh::Optimize**](id3dxmesh--optimize.md)
</dt> </dl>

 

 

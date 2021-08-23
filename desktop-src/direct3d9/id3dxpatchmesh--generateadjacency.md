---
description: Generare un elenco di bordi della mesh e delle patch che condividono ogni bordo.
ms.assetid: 024528c0-2c0d-4448-9b38-05cf8d6ffc63
title: Metodo ID3DXPatchMesh::GenerateAdjacency (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPatchMesh.GenerateAdjacency
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 41e821d853a8a8f981f1174d654f17475c0363cdcc97bb537e308ccd72e38190
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118987201"
---
# <a name="id3dxpatchmeshgenerateadjacency-method"></a>Metodo ID3DXPatchMesh::GenerateAdjacency

Generare un elenco di bordi della mesh e delle patch che condividono ogni bordo.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GenerateAdjacency(
  [in] FLOAT fTolerance
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*fTolerance* \[ Pollici\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Specifica che i vertici che differiscono per posizione per minore della tolleranza devono essere considerati coincidenti.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è D3D \_ OK. Se il metodo ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Commenti

Dopo che un'applicazione genera informazioni di adicenza per una mesh, i dati della mesh possono essere ottimizzati per migliorare le prestazioni di disegno. Questo metodo determina quali patch sono adiacenti (all'interno della tolleranza specificata). Queste informazioni vengono usate internamente per ottimizzare la tessellazione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXPatchMesh](id3dxpatchmesh.md)
</dt> <dt>

[**ID3DXPatchMesh::Optimize**](id3dxpatchmesh--optimize.md)
</dt> </dl>

 

 

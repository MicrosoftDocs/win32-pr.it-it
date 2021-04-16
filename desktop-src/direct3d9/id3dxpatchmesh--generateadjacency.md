---
description: Generare un elenco di bordi della rete e le patch che condividono ogni bordo.
ms.assetid: 024528c0-2c0d-4448-9b38-05cf8d6ffc63
title: 'Metodo ID3DXPatchMesh:: GenerateAdjacency (D3DX9Mesh. h)'
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
ms.openlocfilehash: 68de2a77b9d27391c57ec299ceb87d29166ee248
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104401932"
---
# <a name="id3dxpatchmeshgenerateadjacency-method"></a>Metodo ID3DXPatchMesh:: GenerateAdjacency

Generare un elenco di bordi della rete e le patch che condividono ogni bordo.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GenerateAdjacency(
  [in] FLOAT fTolerance
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*fTolerance* \[ in\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

Specifica che i vertici che differiscono in base a un numero inferiore rispetto alla tolleranza devono essere considerati coincidenti.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è D3D \_ OK. Se il metodo ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, E \_ OutOfMemory.

## <a name="remarks"></a>Commenti

Quando un'applicazione genera informazioni adiacenza per una mesh, i dati della mesh possono essere ottimizzati per migliorare le prestazioni di disegno. Questo metodo determina quali patch sono adiacenti (entro la tolleranza fornita). Queste informazioni vengono utilizzate internamente per ottimizzare la suddivisione a mosaico.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXPatchMesh](id3dxpatchmesh.md)
</dt> <dt>

[**ID3DXPatchMesh:: Optimize**](id3dxpatchmesh--optimize.md)
</dt> </dl>

 

 

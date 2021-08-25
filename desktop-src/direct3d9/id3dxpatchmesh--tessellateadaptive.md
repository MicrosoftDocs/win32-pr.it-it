---
description: Esegue la tessellazione adattiva in base al criterio a tessellazione adattiva basato su z.
ms.assetid: 9f8f5c18-e866-4893-ba07-2a3c0d26c028
title: Metodo ID3DXPatchMesh::TessellateAdaptive (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPatchMesh.TessellateAdaptive
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d6365cfcf50debfeeb28fd493b76ac60943ee14f27a2dadec168b3dd4d31ace1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119856291"
---
# <a name="id3dxpatchmeshtessellateadaptive-method"></a>Metodo ID3DXPatchMesh::TessellateAdaptive

Esegue la tessellazione adattiva in base al criterio a tessellazione adattiva basato su z.

## <a name="syntax"></a>Sintassi


```C++
HRESULT TessellateAdaptive(
  [in] const D3DXVECTOR4 *pTrans,
  [in]       DWORD       dwMaxTessLevel,
  [in]       DWORD       dwMinTessLevel,
  [in]       LPD3DXMESH  pMesh
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pTrans* \[ Pollici\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR4**](d3dxvector4.md) \***

Specifica un vettore 4D punteggiato con i vertici per ottenere la quantità adattiva a tessellazione per vertice. Ogni bordo viene a tessellato al valore medio dei livelli a tessellazione per i due vertici che connette.

</dd> <dt>

*dwMaxTessLevel* \[ Pollici\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Limite massimo per la tessellazione adattiva. Questo è il numero di vertici introdotti tra i vertici esistenti. Questo valore intero può essere compreso tra 1 e 32, inclusi.

</dd> <dt>

*dwMinTessLevel* \[ Pollici\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Limite minimo per la tessellazione adattiva. Questo è il numero di vertici introdotti tra i vertici esistenti. Questo valore intero può essere compreso tra 1 e 32, inclusi.

</dd> <dt>

*pMesh* \[ Pollici\]
</dt> <dd>

Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)**

Mesh a tessella risultante. Vedere [**ID3DXMesh**](id3dxmesh.md).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è D3D \_ OK. Se il metodo ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Commenti

Questa funzione funzionerà in modo più efficiente se la mesh di patch è stata ottimizzata usando [**ID3DXPatchMesh::Optimize**](id3dxpatchmesh--optimize.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXPatchMesh](id3dxpatchmesh.md)
</dt> </dl>

 

 

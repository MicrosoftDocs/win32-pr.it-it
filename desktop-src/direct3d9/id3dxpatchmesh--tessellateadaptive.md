---
description: Esegue lo schema a mosaico adattivo basato sul criterio a mosaico adattivo basato su z.
ms.assetid: 9f8f5c18-e866-4893-ba07-2a3c0d26c028
title: 'Metodo ID3DXPatchMesh:: TessellateAdaptive (D3DX9Mesh. h)'
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
ms.openlocfilehash: e4cc6c6b7ff7b0cdb99e56386df49529f26c9166
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323050"
---
# <a name="id3dxpatchmeshtessellateadaptive-method"></a>Metodo ID3DXPatchMesh:: TessellateAdaptive

Esegue lo schema a mosaico adattivo basato sul criterio a mosaico adattivo basato su z.

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

*pTrans* \[ in\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR4**](d3dxvector4.md) \***

Specifica un vettore 4D punteggiato con i vertici per ottenere l'importo a mosaico adattivo per vertice. Ogni bordo è tassellati al valore medio dei livelli a mosaico per i due vertici a cui si connette.

</dd> <dt>

*dwMaxTessLevel* \[ in\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Limite massimo per lo schema a mosaico adattivo. Il numero di vertici introdotti tra i vertici esistenti. Questo valore integer può variare da 1 a 32, inclusi.

</dd> <dt>

*dwMinTessLevel* \[ in\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Limite minimo per lo schema a mosaico adattivo. Il numero di vertici introdotti tra i vertici esistenti. Questo valore integer può variare da 1 a 32, inclusi.

</dd> <dt>

*pMesh* \[ in\]
</dt> <dd>

Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)**

Mesh tassellati risultante. Vedere [**ID3DXMesh**](id3dxmesh.md).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è D3D \_ OK. Se il metodo ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, E \_ OutOfMemory.

## <a name="remarks"></a>Commenti

Questa funzione verrà eseguita in modo più efficiente se la mesh patch è stata ottimizzata con [**ID3DXPatchMesh:: Optimize**](id3dxpatchmesh--optimize.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXPatchMesh](id3dxpatchmesh.md)
</dt> </dl>

 

 

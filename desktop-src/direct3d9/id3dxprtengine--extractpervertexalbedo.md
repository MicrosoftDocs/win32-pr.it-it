---
description: Copia i valori di albedo per vertice da una mesh.
ms.assetid: 3a6f1cc2-a870-4463-98df-599d9fbd9d78
title: 'Metodo ID3DXPRTEngine:: ExtractPerVertexAlbedo (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.ExtractPerVertexAlbedo
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ed23b75b3113421b6242f49416e4b54bfce336f4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103969488"
---
# <a name="id3dxprtengineextractpervertexalbedo-method"></a>Metodo ID3DXPRTEngine:: ExtractPerVertexAlbedo

Copia i valori di albedo per vertice da una mesh.

## <a name="syntax"></a>Sintassi


```C++
HRESULT ExtractPerVertexAlbedo(
  [in] LPD3DXMESH   pMesh,
  [in] D3DDECLUSAGE Usage,
  [in] UINT         NumChanIn
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pMesh* \[ in\]
</dt> <dd>

Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)**

Puntatore all'oggetto mesh [**ID3DXMesh**](id3dxmesh.md) usato in [**D3DXCreatePRTEngine**](d3dxcreateprtengine.md) per creare l'oggetto [**ID3DXPRTEngine**](id3dxprtengine.md) .

</dd> <dt>

*Utilizzo* \[ di in\]
</dt> <dd>

Tipo: **[ **D3DDECLUSAGE**](./d3ddeclusage.md)**

Descrizioni dell'utilizzo dei vertici da copiare dalla mesh. Vedere [**D3DDECLUSAGE**](./d3ddeclusage.md).

</dd> <dt>

*NumChanIn* \[ in\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Numero di canali dei colori da copiare dalla mesh. Impostare su 1 per specificare i materiali grigi (R = G = B) o 3 per abilitare gli effetti di emorragia del colore.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è \_ OK. Se il metodo ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, E \_ OutOfMemory.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXPRTEngine](id3dxprtengine.md)
</dt> </dl>

 

 

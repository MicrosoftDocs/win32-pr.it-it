---
description: Estrae i coefficienti di proiezione del componente principale per campione (PCA) da un buffer di dati compresso ID3DXPRTCompBuffer e aggiunge i dati a un oggetto ID3DXMesh.
ms.assetid: 0680d626-f07a-43d3-acb9-e8db82b5e933
title: 'Metodo ID3DXPRTCompBuffer:: ExtractToMesh (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTCompBuffer.ExtractToMesh
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 607b583b89358d2d28030a4187b1608174d849c0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322321"
---
# <a name="id3dxprtcompbufferextracttomesh-method"></a>Metodo ID3DXPRTCompBuffer:: ExtractToMesh

Estrae i coefficienti di proiezione del componente principale per campione (PCA) da un buffer di dati compresso [**ID3DXPRTCompBuffer**](id3dxprtcompbuffer.md) e aggiunge i dati a un oggetto [**ID3DXMesh**](id3dxmesh.md) .

## <a name="syntax"></a>Sintassi


```C++
HRESULT ExtractToMesh(
  [in] UINT         NumPCA,
  [in] D3DDECLUSAGE Usage,
  [in] UINT         UsageIndexStart,
  [in] LPD3DXMESH   pScene
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*NumPCA* \[ in\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Numero di coefficienti PCA da estrarre dal buffer.

</dd> <dt>

*Utilizzo* \[ di in\]
</dt> <dd>

Tipo: **[ **D3DDECLUSAGE**](./d3ddeclusage.md)**

Descrizioni dell'utilizzo dei vertici della mesh. Vedere [**D3DDECLUSAGE**](./d3ddeclusage.md).

</dd> <dt>

*UsageIndexStart* \[ in\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Indice iniziale per i coefficienti PCA da archiviare nella rete mesh.

</dd> <dt>

*pScene* \[ in\]
</dt> <dd>

Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)**

Puntatore a un oggetto mesh [**ID3DXMesh**](id3dxmesh.md) in cui vengono archiviati i coefficienti PCA.

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

[ID3DXPRTCompBuffer](id3dxprtcompbuffer.md)
</dt> </dl>

 

 

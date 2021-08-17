---
description: Estrae i coefficienti di proiezione PCA (Principal Component Analysis) per campione da un buffer di dati compresso ID3DXPRTCompBuffer e aggiunge i dati a un oggetto ID3DXMesh.
ms.assetid: 0680d626-f07a-43d3-acb9-e8db82b5e933
title: Metodo ID3DXPRTCompBuffer::ExtractToMesh (D3DX9Mesh.h)
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
ms.openlocfilehash: 410ec268da89ad4033c88a90c2b37bfa8e78a7b9c229cab72c8ad07e666fce42
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117730037"
---
# <a name="id3dxprtcompbufferextracttomesh-method"></a>Metodo ID3DXPRTCompBuffer::ExtractToMesh

Estrae i coefficienti di proiezione PCA (Principal Component Analysis) per campione da un buffer di dati compresso [**ID3DXPRTCompBuffer**](id3dxprtcompbuffer.md) e aggiunge i dati a un [**oggetto ID3DXMesh.**](id3dxmesh.md)

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

*NumPCA* \[ Pollici\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Numero di coefficienti PCA da estrarre dal buffer.

</dd> <dt>

*Utilizzo* \[ Pollici\]
</dt> <dd>

Tipo: **[ **D3DDECLUSAGE**](./d3ddeclusage.md)**

Descrizioni dell'utilizzo dei vertici della mesh. Vedere [**D3DDECLUSAGE.**](./d3ddeclusage.md)

</dd> <dt>

*UsageIndexStart* \[ Pollici\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Indice iniziale per i coefficienti PCA da archiviare nella mesh.

</dd> <dt>

*pScene* \[ Pollici\]
</dt> <dd>

Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)**

Puntatore a un oggetto mesh [**ID3DXMesh**](id3dxmesh.md) che archivierà i coefficienti PCA.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è S \_ OK. Se il metodo ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXPRTCompBuffer](id3dxprtcompbuffer.md)
</dt> </dl>

 

 

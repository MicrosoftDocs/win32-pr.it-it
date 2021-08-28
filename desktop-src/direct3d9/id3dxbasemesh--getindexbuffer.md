---
description: 'Metodo ID3DXBaseMesh::GetIndexBuffer: recupera i dati in un index buffer.'
ms.assetid: 8e14a047-a8a6-4763-88c7-3b439044eeb4
title: Metodo ID3DXBaseMesh::GetIndexBuffer (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseMesh.GetIndexBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d47f13a60a681df83df788d91a69c9981746e18df4c65062a9191d2e18de2006
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119848491"
---
# <a name="id3dxbasemeshgetindexbuffer-method"></a>Metodo ID3DXBaseMesh::GetIndexBuffer

Recupera i dati in un index buffer.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetIndexBuffer(
  [out, retval] LPDIRECT3DINDEXBUFFER9 *ppIB
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ppIB* \[ out, retval\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DINDEXBUFFER9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dindexbuffer9)\***

Indirizzo di un puntatore a [**un'interfaccia IDirect3DIndexBuffer9,**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dindexbuffer9) che rappresenta l'index buffer oggetto associato alla mesh.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è D3D \_ OK. Se il metodo ha esito negativo, il valore restituito può essere D3DERR \_ INVALIDCALL.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXBaseMesh](id3dxbasemesh.md)
</dt> </dl>

 

 

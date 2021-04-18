---
description: Clona una mesh usando un codice FVF (Flexible Vertex Format).
ms.assetid: b7d23ea9-1a2f-46e3-bcb5-82040d2a1e12
title: 'Metodo ID3DXBaseMesh:: CloneMeshFVF (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseMesh.CloneMeshFVF
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 4cb3b0ad33e54e79464949f441842173fb48a180
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322556"
---
# <a name="id3dxbasemeshclonemeshfvf-method"></a>Metodo ID3DXBaseMesh:: CloneMeshFVF

Clona una mesh usando un codice FVF (Flexible Vertex Format).

## <a name="syntax"></a>Sintassi


```C++
HRESULT CloneMeshFVF(
  [in]          DWORD             Options,
  [in]          DWORD             FVF,
  [in]          LPDIRECT3DDEVICE9 pDevice,
  [out, retval] LPD3DXMESH        *ppCloneMesh
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Opzioni* \[ di in\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Combinazione di uno o più flag [**D3DXMESH**](./d3dxmesh.md) che specificano le opzioni di creazione per la mesh.

</dd> <dt>

*FVF* \[ in\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Combinazione di codici FVF, che specifica il formato del vertice per i vertici nella mesh di output. Per i valori dei codici, vedere [D3DFVF](d3dfvf.md).

</dd> <dt>

*PDEVICE* \[ in\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Puntatore a un'interfaccia [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) che rappresenta l'oggetto dispositivo associato alla mesh.

</dd> <dt>

*ppCloneMesh* \[ out, retval\]
</dt> <dd>

Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)\***

Indirizzo di un puntatore a un'interfaccia [**ID3DXMesh**](id3dxmesh.md) , che rappresenta la mesh clonata.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è D3D \_ OK. Se il metodo ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, E \_ OutOfMemory.

## <a name="remarks"></a>Commenti

**ID3DXBaseMesh:: CloneMeshFVF** viene usato per riformattare e modificare il layout dei dati del vertice. Questa operazione viene eseguita creando un nuovo oggetto mesh. Ad esempio, usarlo per aggiungere spazio per normali, coordinate di trama, colori, pesi e così via, che non erano presenti prima.

[**ID3DXBaseMesh:: UpdateSemantics**](id3dxbasemesh--updatesemantics.md) aggiorna la dichiarazione di vertice con informazioni semantiche diverse senza modificare il layout del buffer del vertice. Questo metodo non modifica il contenuto del buffer dei vertici. Ad esempio, usarlo per rietichettare una coordinata di trama 3D come una binormale o tangente o viceversa.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXBaseMesh](id3dxbasemesh.md)
</dt> <dt>

[**D3DXFVFFromDeclarator**](d3dxfvffromdeclarator.md)
</dt> </dl>

 

 

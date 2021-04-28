---
description: 'Funzione D3DXLoadMeshHierarchyFromXInMemory: carica la prima gerarchia di frame da un file con estensione x.'
ms.assetid: 428e5cfb-d6a5-4a7f-b082-2d8898e65490
title: Funzione D3DXLoadMeshHierarchyFromXInMemory (D3dx9anim.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXLoadMeshHierarchyFromXInMemory
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 551810c839e619985d9a380197553f5fe4fc9be8
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098209"
---
# <a name="d3dxloadmeshhierarchyfromxinmemory-function"></a>Funzione D3DXLoadMeshHierarchyFromXInMemory

Carica la prima gerarchia di frame da un file con estensione x.

## <a name="syntax"></a>Sintassi


```C++
HRESULT D3DXLoadMeshHierarchyFromXInMemory(
  _In_  LPCVOID                   pMemory,
  _In_  DWORD                     SizeOfMemory,
  _In_  DWORD                     MeshOptions,
  _In_  LPDIRECT3DDEVICE9         pDevice,
  _In_  LPD3DXALLOCATEHIERARCHY   pAlloc,
  _In_  LPD3DXLOADUSERDATA        pUserDataLoader,
  _Out_ LPD3DXFRAME               *ppFrameHeirarchy,
  _Out_ LPD3DXANIMATIONCONTROLLER *ppAnimController
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pMemory* \[ Pollici\]
</dt> <dd>

Tipo: **[ **LPCVOID**](../winprog/windows-data-types.md)**

Puntatore a un buffer che contiene la gerarchia mesh.

</dd> <dt>

*SizeOfMemory* \[ Pollici\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Dimensioni del buffer pMemory, in byte.

</dd> <dt>

*MeshOptions* \[ Pollici\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Combinazione di uno o più flag [**dell'enumerazione D3DXMESH**](./d3dxmesh.md) che specificano le opzioni di creazione per la mesh.

</dd> <dt>

*pDevice* \[ Pollici\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Puntatore a [**un'interfaccia IDirect3DDevice9,**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) l'oggetto dispositivo associato alla mesh.

</dd> <dt>

*pAlloc* \[ Pollici\]
</dt> <dd>

Tipo: **[ **LPD3DXALLOCATEHIERARCHY**](id3dxallocatehierarchy.md)**

Puntatore a [**un'interfaccia ID3DXAllocateHierarchy.**](id3dxallocatehierarchy.md)

</dd> <dt>

*pUserDataLoader* \[ Pollici\]
</dt> <dd>

Tipo: **[ **LPD3DXLOADUSERDATA**](id3dxloaduserdata.md)**

Interfaccia fornita dall'applicazione che consente il caricamento dei dati utente. Vedere [**ID3DXLoadUserData.**](id3dxloaduserdata.md)

</dd> <dt>

*ppFrameHeirarchy* \[ Cambio\]
</dt> <dd>

Tipo: **[ **LPD3DXFRAME**](d3dxframe.md)\***

Restituisce un puntatore alla gerarchia di frame caricata. Vedere [**D3DXFRAME.**](d3dxframe.md)

</dd> <dt>

*ppAnimController* \[ Cambio\]
</dt> <dd>

Tipo: **[ **LPD3DXANIMATIONCONTROLLER**](id3dxanimationcontroller.md)\***

Restituisce un puntatore al controller di animazione corrispondente all'animazione nel file con estensione x. Viene creato con tracce ed eventi predefiniti. Vedere [**ID3DXAnimationController.**](id3dxanimationcontroller.md)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se la funzione ha esito positivo, il valore restituito è D3D \_ OK. Se la funzione ha esito negativo, il valore restituito può essere uno dei valori seguenti: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Commenti

Tutte le mesh nel file verranno compresse in un'unica mesh di output. Se il file contiene una gerarchia di frame, tutte le trasformazioni verranno applicate alla mesh.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9anim.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni di animazione](dx9-graphics-reference-d3dx-functions-animation.md)
</dt> </dl>

 

 

---
description: Carica una mesh dalla memoria.
ms.assetid: bbaecc00-97ab-433c-b0c7-ac7837bfc3be
title: Funzione D3DXLoadMeshFromXInMemory (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXLoadMeshFromXInMemory
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 19427da28b90fe4410a65f0321b5dcd486b4c917d209f1f20762d05899b4eb0f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119044949"
---
# <a name="d3dxloadmeshfromxinmemory-function"></a>Funzione D3DXLoadMeshFromXInMemory

Carica una mesh dalla memoria.

## <a name="syntax"></a>Sintassi


```C++
HRESULT D3DXLoadMeshFromXInMemory(
  _In_  LPCVOID           Memory,
  _In_  DWORD             SizeOfMemory,
  _Out_ DWORD             Options,
  _In_  LPDIRECT3DDEVICE9 pD3DDevice,
  _Out_ LPD3DXBUFFER      *ppAdjacency,
  _Out_ LPD3DXBUFFER      *ppMaterials,
  _Out_ LPD3DXBUFFER      *ppEffectInstances,
  _Out_ DWORD             *pNumMaterials,
  _Out_ LPD3DXMESH        *ppMesh
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Memoria* \[ Pollici\]
</dt> <dd>

Tipo: **[ **LPCVOID**](../winprog/windows-data-types.md)**

Puntatore al buffer di memoria che contiene i dati della mesh.

</dd> <dt>

*SizeOfMemory* \[ Pollici\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Dimensioni del file in memoria, in byte.

</dd> <dt>

*Opzioni* \[ Cambio\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Combinazione di uno o più flag [**dell'enumerazione D3DXMESH,**](./d3dxmesh.md) specificando le opzioni di creazione per la mesh.

</dd> <dt>

*pD3DDevice* \[ Pollici\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Puntatore a [**un'interfaccia IDirect3DDevice9,**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) l'oggetto dispositivo associato alla mesh.

</dd> <dt>

*ppAdjacency* \[ Cambio\]
</dt> <dd>

Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Indirizzo di un puntatore a [**un'interfaccia ID3DXBuffer.**](id3dxbuffer.md) Quando il metodo viene restituito, questo parametro viene riempito con una matrice di tre DWORD per viso che specificano i tre elementi adiacenti per ogni viso nella mesh.

</dd> <dt>

*ppMaterials* \[ Cambio\]
</dt> <dd>

Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Indirizzo di un puntatore a [**un'interfaccia ID3DXBuffer.**](id3dxbuffer.md) Quando questo metodo viene restituito, questo parametro viene riempito con una matrice di strutture [**D3DXMATERIAL,**](d3dxmaterial.md) contenente le informazioni salvate nel file DirectX.

</dd> <dt>

*ppEffectInstances* \[ Cambio\]
</dt> <dd>

Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Puntatore a un buffer contenente una matrice di istanze dell'effetto, una per ogni gruppo di attributi nella mesh restituita. Un'istanza dell'effetto è una particolare istanza di informazioni sullo stato usate per inizializzare un effetto. Vedere [**D3DXEFFECTINSTANCE**](d3dxeffectinstance.md). Per altre informazioni sull'accesso al buffer, vedere [**ID3DXBuffer**](id3dxbuffer.md).

</dd> <dt>

*pNumMaterials* \[ Cambio\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***

Puntatore al numero [**di strutture D3DXMATERIAL**](d3dxmaterial.md) nella matrice *ppMaterials,* quando il metodo restituisce .

</dd> <dt>

*ppMesh* \[ Cambio\]
</dt> <dd>

Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)\***

Indirizzo di un puntatore a [**un'interfaccia ID3DXMesh,**](id3dxmesh.md) che rappresenta la mesh caricata.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se la funzione ha esito positivo, il valore restituito è D3D \_ OK. Se la funzione ha esito negativo, il valore restituito può essere uno dei valori seguenti: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Commenti

Tutte le mesh nel file verranno compresse in un'unica mesh di output. Se il file contiene una gerarchia di frame, tutte le trasformazioni verranno applicate alla mesh.

Per i file mesh che non contengono informazioni sull'istanza dell'effetto, le istanze predefinite dell'effetto verranno generate dalle informazioni sui materiali nel file con estensione x. Un'istanza predefinita dell'effetto avrà valori predefiniti che corrispondono ai membri della [**struttura D3DMATERIAL9.**](d3dmaterial9.md)

Viene compilato anche il nome predefinito della trama, ma viene gestito in modo diverso. Il nome sarà , che corrisponde a una variabile di effetto con il nome Texture0@Name "Texture0" con un'annotazione denominata "Name". Conterrà il nome del file di stringa per la trama.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni mesh](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[**D3DXEFFECTDEFAULT**](d3dxeffectdefault.md)
</dt> <dt>

[**D3DXEFFECTINSTANCE**](d3dxeffectinstance.md)
</dt> </dl>

 

 

---
description: Carica una mesh di patch da un oggetto ID3DXFileData.
ms.assetid: 8054e33e-6bf8-4a56-9f66-30600732c84f
title: Funzione D3DXLoadPatchMeshFromXof (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXLoadPatchMeshFromXof
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8bfdf0faf0a9a8d8d32d38899cdd666d7c4a5d3910119ac36cbca2bf8bb33430
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119564831"
---
# <a name="d3dxloadpatchmeshfromxof-function"></a>Funzione D3DXLoadPatchMeshFromXof

Carica una mesh di patch da un [**oggetto ID3DXFileData.**](id3dxfiledata.md)

## <a name="syntax"></a>Sintassi


```C++
HRESULT D3DXLoadPatchMeshFromXof(
  _In_  LPD3DXFILEDATA    pxofMesh,
  _In_  DWORD             Options,
  _In_  LPDIRECT3DDEVICE9 pD3DDevice,
  _Out_ LPD3DXBUFFER      *ppMaterials,
  _Out_ LPD3DXBUFFER      *ppEffectInstances,
  _Out_ PDWORD            pNumMaterials,
  _Out_ LPD3DXPATCHMESH   *ppMesh
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pxofMesh* \[ Pollici\]
</dt> <dd>

Tipo: **[ **LPD3DXFILEDATA**](id3dxfiledata.md)**

Puntatore a [**un'interfaccia ID3DXFileData**](id3dxfiledata.md) che rappresenta l'oggetto dati del file da caricare.

</dd> <dt>

*Opzioni* \[ Pollici\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Combinazione di uno o [**più flag D3DXMESH,**](./d3dxmesh.md) specificando le opzioni di creazione per la mesh.

</dd> <dt>

*pD3DDevice* \[ Pollici\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Puntatore al dispositivo da cui viene creata la mesh.

</dd> <dt>

*ppMaterials* \[ Cambio\]
</dt> <dd>

Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Matrice di materiali contenuti nella mesh. Ogni materiale viene indicizzato da [**un'interfaccia ID3DXBuffer.**](id3dxbuffer.md)

</dd> <dt>

*ppEffectInstances* \[ Cambio\]
</dt> <dd>

Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Puntatore a un buffer contenente una matrice di istanze dell'effetto, una per gruppo di attributi nella mesh restituita. Un'istanza dell'effetto è una particolare istanza di informazioni sullo stato utilizzata per inizializzare un effetto. Vedere [**D3DXEFFECTINSTANCE**](d3dxeffectinstance.md). Per altre informazioni sull'accesso al buffer, vedere [**ID3DXBuffer.**](id3dxbuffer.md)

</dd> <dt>

*pNumMaterials* \[ Cambio\]
</dt> <dd>

Tipo: **PDWORD**

Puntatore che contiene il numero di materiali nella mesh.

</dd> <dt>

*ppMesh* \[ Cambio\]
</dt> <dd>

Tipo: **[ **LPD3DXPATCHMESH**](id3dxpatchmesh.md)\***

Indirizzo di un puntatore a [**un'interfaccia ID3DXPatchMesh,**](id3dxpatchmesh.md) che rappresenta la mesh caricata.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se la funzione ha esito positivo, il valore restituito è D3D \_ OK. Se la funzione ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Commenti

Per i file mesh che non contengono informazioni sull'istanza dell'effetto, le istanze dell'effetto predefinito verranno generate dalle informazioni sui materiali nel file con estensione x. Un'istanza dell'effetto predefinito avrà valori predefiniti che corrispondono ai membri della [**struttura D3DMATERIAL9.**](d3dmaterial9.md)

Viene compilato anche il nome predefinito della trama, ma viene gestito in modo diverso. Il nome sarà , che corrisponde a una variabile dell'effetto in base al nome Texture0@Name "Texture0" con un'annotazione denominata "Name". Conterrà il nome del file di stringa per la trama.

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

 

 

---
description: Carica una mesh di interfaccia da un oggetto dati di file DirectX con estensione x.
ms.assetid: db284061-2996-4a5f-972d-24577dd1a6d7
title: Funzione D3DXLoadSkinMeshFromXof (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXLoadSkinMeshFromXof
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 28805e56e4c7600b37ce68ac586148de59fe668704726ea0a71c4721a2699a09
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119564691"
---
# <a name="d3dxloadskinmeshfromxof-function"></a>Funzione D3DXLoadSkinMeshFromXof

Carica una mesh di interfaccia da un oggetto dati di file DirectX con estensione x.

## <a name="syntax"></a>Sintassi


```C++
HRESULT D3DXLoadSkinMeshFromXof(
  _In_  LPD3DXFILEDATA    pxofMesh,
  _In_  DWORD             Options,
  _In_  LPDIRECT3DDEVICE9 pD3DDevice,
  _Out_ LPD3DXBUFFER      *ppAdjacency,
  _Out_ LPD3DXBUFFER      *ppMaterials,
  _Out_ LPD3DXBUFFER      *ppEffectInstances,
  _Out_ DWORD             *pMatOut,
  _Out_ LPD3DXSKININFO    *ppSkinInfo,
  _Out_ LPD3DXMESH        *ppMesh
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

Combinazione di uno o più flag, [**dall'enumerazione D3DXMESH,**](./d3dxmesh.md) che specifica le opzioni di creazione per la mesh.

</dd> <dt>

*pD3DDevice* \[ Pollici\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Puntatore a [**un'interfaccia IDirect3DDevice9,**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) l'oggetto dispositivo associato alla mesh.

</dd> <dt>

*ppAdjacency* \[ Cambio\]
</dt> <dd>

Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Indirizzo di un puntatore a [**un'interfaccia ID3DXBuffer.**](id3dxbuffer.md) Quando questo metodo viene restituito, questo parametro viene riempito con una matrice di tre DWORD per ogni viso che specificano i tre elementi adiacenti per ogni viso nella mesh.

</dd> <dt>

*ppMaterials* \[ Cambio\]
</dt> <dd>

Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Indirizzo di un puntatore a [**un'interfaccia ID3DXBuffer.**](id3dxbuffer.md) Quando il metodo viene restituito, questo parametro viene riempito con una matrice di [**strutture D3DXMATERIAL.**](d3dxmaterial.md)

</dd> <dt>

*ppEffectInstances* \[ Cambio\]
</dt> <dd>

Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Puntatore a un buffer contenente una matrice di istanze dell'effetto, una per gruppo di attributi nella mesh restituita. Un'istanza dell'effetto è una particolare istanza di informazioni sullo stato utilizzata per inizializzare un effetto. Vedere [**D3DXEFFECTINSTANCE**](d3dxeffectinstance.md). Per altre informazioni sull'accesso al buffer, vedere [**ID3DXBuffer.**](id3dxbuffer.md)

</dd> <dt>

*pMatOut* \[ Cambio\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***

Puntatore al numero [**di strutture D3DXMATERIAL**](d3dxmaterial.md) nella matrice *ppMaterials,* quando il metodo restituisce un risultato.

</dd> <dt>

*ppSkinInfo* \[ Cambio\]
</dt> <dd>

Tipo: **[ **LPD3DXSKININFO**](id3dxskininfo.md)\***

Indirizzo di un puntatore a [**un'interfaccia ID3DXSkinInfo,**](id3dxskininfo.md) che rappresenta le informazioni di interfaccia.

</dd> <dt>

*ppMesh* \[ Cambio\]
</dt> <dd>

Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)\***

Indirizzo di un puntatore a [**un'interfaccia ID3DXMesh,**](id3dxmesh.md) che rappresenta la mesh caricata.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se la funzione ha esito positivo, il valore restituito è D3D \_ OK. Se la funzione ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY

## <a name="remarks"></a>Commenti

Questo metodo accetta un puntatore a un oggetto interno nel file con estensione x, consentendo di caricare la gerarchia dei frame.

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

 

 

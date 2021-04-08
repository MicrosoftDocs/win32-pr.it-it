---
description: Carica una mesh da una risorsa.
ms.assetid: 3cf253dc-4f3f-4949-ab24-8225667f95f2
title: Funzione D3DXLoadMeshFromXResource (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXLoadMeshFromXResource
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b3e1d9d14d86296df48e2d27f77e2f79f3ad73c2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103762029"
---
# <a name="d3dxloadmeshfromxresource-function"></a>D3DXLoadMeshFromXResource (funzione)

Carica una mesh da una risorsa.

## <a name="syntax"></a>Sintassi


```C++
HRESULT D3DXLoadMeshFromXResource(
  _In_  HMODULE           Module,
  _In_  LPCSTR            Name,
  _In_  LPCSTR            Type,
  _In_  DWORD             Options,
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

*Modulo* \[ di in\]
</dt> <dd>

Tipo: **[ **hmodule**](../winprog/windows-data-types.md)**

Handle per il modulo in cui si trova la risorsa o **null** per il modulo associato all'immagine utilizzata dal sistema operativo per creare il processo corrente. Vedere la sezione Osservazioni.

</dd> <dt>

*Nome* \[ in\]
</dt> <dd>

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Puntatore a una stringa che specifica la risorsa da cui creare la mesh. Vedere la sezione Osservazioni.

</dd> <dt>

*Tipo* \[ di in\]
</dt> <dd>

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Puntatore a una stringa che specifica il tipo di risorsa. Vedere la sezione Osservazioni.

</dd> <dt>

*Opzioni* \[ di in\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Combinazione di uno o più flag dell'enumerazione [**D3DXMESH**](./d3dxmesh.md) che specificano le opzioni di creazione per la mesh.

</dd> <dt>

*pD3DDevice* \[ in\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Puntatore a un'interfaccia [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , l'oggetto dispositivo associato alla mesh.

</dd> <dt>

*ppAdjacency* \[ out\]
</dt> <dd>

Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Indirizzo di un puntatore a un'interfaccia [**ID3DXBuffer**](id3dxbuffer.md) . Quando il metodo restituisce un risultato, questo parametro viene riempito con una matrice di tre DWORD per ogni volto che specifica i tre elementi adiacenti per ogni viso nella mesh.

</dd> <dt>

*ppMaterials* \[ out\]
</dt> <dd>

Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Indirizzo di un puntatore a un'interfaccia [**ID3DXBuffer**](id3dxbuffer.md) . Quando questo metodo viene restituito, questo parametro viene compilato con una matrice di strutture [**D3DXMATERIAL**](d3dxmaterial.md) , che contiene le informazioni salvate nel file DirectX.

</dd> <dt>

*ppEffectInstances* \[ out\]
</dt> <dd>

Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Puntatore a un buffer che contiene una matrice di istanze di effetto, una per ogni gruppo di attributi nella mesh restituita. Un'istanza dell'effetto è una particolare istanza delle informazioni sullo stato usate per inizializzare un effetto. Vedere [**D3DXEFFECTINSTANCE**](d3dxeffectinstance.md). Per ulteriori informazioni sull'accesso al buffer, vedere [**ID3DXBuffer**](id3dxbuffer.md).

</dd> <dt>

*pNumMaterials* \[ out\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***

Puntatore al numero di strutture [**D3DXMATERIAL**](d3dxmaterial.md) nella matrice *ppMaterials* quando il metodo restituisce.

</dd> <dt>

*ppMesh* \[ out\]
</dt> <dd>

Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)\***

Indirizzo di un puntatore a un'interfaccia [**ID3DXMesh**](id3dxmesh.md) , che rappresenta la mesh caricata.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se la funzione ha esito positivo, il valore restituito è D3D \_ OK. Se la funzione ha esito negativo, il valore restituito può essere uno dei valori seguenti: D3DERR \_ INVALIDCALL, E \_ OutOfMemory.

## <a name="remarks"></a>Commenti

Vedere [**FindResource**](/windows/win32/api/winbase/nf-winbase-findresourcea) per altre informazioni sui parametri Module, Name e Type.

Tutte le mesh nel file verranno compresse in una mesh di output. Se il file contiene una gerarchia di frame, tutte le trasformazioni verranno applicate alla rete.

Per i file mesh che non contengono informazioni sull'istanza di effetto, le istanze di effetto predefinite verranno generate dalle informazioni sul materiale nel file con estensione x. Un'istanza dell'effetto predefinito avrà valori predefiniti che corrispondono ai membri della struttura [**D3DMATERIAL9**](d3dmaterial9.md) .

Il nome di trama predefinito viene anche compilato, ma viene gestito in modo diverso. Il nome sarà Texture0@Name , che corrisponde a una variabile Effect con il nome "Texture0" con un'annotazione denominata "Name". Questo conterrà il nome del file di stringa per la trama.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni mesh](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[**D3DXEFFECTDEFAULT**](d3dxeffectdefault.md)
</dt> <dt>

[**D3DXEFFECTINSTANCE**](d3dxeffectinstance.md)
</dt> </dl>

 

 

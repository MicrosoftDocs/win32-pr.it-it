---
description: Carica la prima gerarchia di frame da un file con estensione x.
ms.assetid: 1d446b23-9028-4187-b97c-a61edfe68e39
title: Funzione D3DXLoadMeshHierarchyFromX (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXLoadMeshHierarchyFromX
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 308ebf127708849bec8ee8a4f2601f029562634a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103969305"
---
# <a name="d3dxloadmeshhierarchyfromx-function"></a>D3DXLoadMeshHierarchyFromX (funzione)

Carica la prima gerarchia di frame da un file con estensione x.

## <a name="syntax"></a>Sintassi


```C++
HRESULT D3DXLoadMeshHierarchyFromX(
  _In_  LPCTSTR                   Filename,
  _In_  DWORD                     MeshOptions,
  _In_  LPDIRECT3DDEVICE9         pDevice,
  _In_  LPD3DXALLOCATEHIERARCHY   pAlloc,
  _In_  LPD3DXLOADUSERDATA        pUserDataLoader,
  _Out_ LPD3DXFRAME               *ppFrameHierarchy,
  _Out_ LPD3DXANIMATIONCONTROLLER *ppAnimController
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Nome file* \[ in\]
</dt> <dd>

Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**

Puntatore a una stringa che specifica il nome del file. Se le impostazioni del compilatore richiedono Unicode, il tipo di dati LPCTSTR viene risolto in LPCWSTR. In caso contrario, il tipo di dati String viene risolto in LPCSTR. Vedere la sezione Osservazioni.

</dd> <dt>

*MeshOptions* \[ in\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Combinazione di uno o più flag dell'enumerazione [**D3DXMESH**](./d3dxmesh.md) che specificano le opzioni di creazione per la mesh.

</dd> <dt>

*PDEVICE* \[ in\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Puntatore a un'interfaccia [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , l'oggetto dispositivo associato alla mesh.

</dd> <dt>

*pAlloc* \[ in\]
</dt> <dd>

Tipo: **[ **LPD3DXALLOCATEHIERARCHY**](id3dxallocatehierarchy.md)**

Puntatore a un'interfaccia [**ID3DXAllocateHierarchy**](id3dxallocatehierarchy.md) .

</dd> <dt>

*pUserDataLoader* \[ in\]
</dt> <dd>

Tipo: **[ **LPD3DXLOADUSERDATA**](id3dxloaduserdata.md)**

Interfaccia fornita dall'applicazione che consente il caricamento dei dati utente. Vedere [**ID3DXLoadUserData**](id3dxloaduserdata.md).

</dd> <dt>

*ppFrameHierarchy* \[ out\]
</dt> <dd>

Tipo: **[ **LPD3DXFRAME**](d3dxframe.md)\***

Restituisce un puntatore alla gerarchia dei frame caricati. Vedere [**D3DXFRAME**](d3dxframe.md).

</dd> <dt>

*ppAnimController* \[ out\]
</dt> <dd>

Tipo: **[ **LPD3DXANIMATIONCONTROLLER**](id3dxanimationcontroller.md)\***

Restituisce un puntatore al controller di animazione corrispondente all'animazione nel file con estensione x. Questa operazione viene creata con tracce ed eventi predefiniti. Vedere [**ID3DXAnimationController**](id3dxanimationcontroller.md).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se la funzione ha esito positivo, il valore restituito è D3D \_ OK. Se la funzione ha esito negativo, il valore restituito può essere uno dei valori seguenti: D3DERR \_ INVALIDCALL, E \_ OutOfMemory.

## <a name="remarks"></a>Commenti

L'impostazione del compilatore determina anche la versione della funzione. Se è definito Unicode, la chiamata di funzione viene risolta in D3DXLoadMeshHierarchyFromXW. In caso contrario, la chiamata di funzione viene risolta in D3DXLoadMeshHierarchyFromXA.

Tutte le mesh nel file verranno compresse in una mesh di output. Se il file contiene una gerarchia di frame, tutte le trasformazioni verranno applicate alla rete.

**D3DXLoadMeshHierarchyFromX** carica i dati di animazione e la gerarchia dei frame da un file con estensione x. Analizza il file con estensione x e compila una gerarchia dei frame e un controller di animazione in base all'oggetto derivato da [**ID3DXAllocateHierarchy**](id3dxallocatehierarchy.md)passato attraverso pAlloc. Il caricamento dei dati richiede diversi passaggi, come indicato di seguito:

1.  Derivare [**ID3DXAllocateHierarchy**](id3dxallocatehierarchy.md), implementando ogni metodo. Questa operazione Controlla la modalità di allocazione e liberazione di frame e mesh.
2.  Derivare [**ID3DXLoadUserData**](id3dxloaduserdata.md), implementando ogni metodo. Se il file con estensione x non contiene dati incorporati definiti dall'utente o se non è necessario, è possibile ignorare questa parte.
3.  Creare un oggetto della classe [**ID3DXAllocateHierarchy**](id3dxallocatehierarchy.md) e, facoltativamente, la classe LoadUserData. Non è necessario chiamare alcun metodo di questi oggetti.
4.  Chiamare **D3DXLoadMeshHierarchyFromX**, passando l'oggetto [**ID3DXAllocateHierarchy**](id3dxallocatehierarchy.md) e l'oggetto [**ID3DXLoadUserData**](id3dxloaduserdata.md) (o **null**) per creare la gerarchia dei frame e il controller di animazione. Tutti i set di animazioni e i frame vengono registrati automaticamente nel controller di animazione.

Durante il caricamento, [**CreateFrame**](id3dxallocatehierarchy--createframe.md) e [**LoadFrameChildData**](id3dxloaduserdata--loadframechilddata.md) vengono richiamati in ogni frame per controllare il caricamento e l'allocazione del frame. L'applicazione definisce questi metodi per controllare la modalità di archiviazione dei frame. [**CreateMeshContainer**](id3dxallocatehierarchy--createmeshcontainer.md) e [**LoadMeshChildData**](id3dxloaduserdata--loadmeshchilddata.md) vengono richiamati in ogni oggetto mesh per controllare il caricamento e l'allocazione di oggetti mesh. [**LoadTopLevelData**](id3dxloaduserdata--loadtopleveldata.md) viene richiamato per ogni oggetto di primo livello che non viene caricato dagli altri metodi.

Per liberare questi dati, chiamare ID3DXAnimationController:: Release per liberare i set di animazioni e [**D3DXFRAMEDestroy**](d3dxframedestroy.md), passando il nodo radice della gerarchia dei frame e un oggetto della classe [**ID3DXAllocateHierarchy**](id3dxallocatehierarchy.md) derivata. [**DestroyFrame**](id3dxallocatehierarchy--destroyframe.md) e [**DestroyMeshContainer**](id3dxallocatehierarchy--destroymeshcontainer.md) verranno chiamati per ogni oggetto frame e mesh nella gerarchia dei frame. L'implementazione di **DestroyFrame** deve rilasciare tutti gli elementi allocati da [**CreateFrame**](id3dxallocatehierarchy--createframe.md)e allo stesso modo per i metodi del contenitore mesh.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni di animazione](dx9-graphics-reference-d3dx-functions-animation.md)
</dt> </dl>

 

 

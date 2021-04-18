---
description: Salva una mesh in un file con estensione x.
ms.assetid: 6d9cbca8-3847-4e15-95d4-9df3f8269665
title: Funzione D3DXSaveMeshToX (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSaveMeshToX
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 504e7ad69b83c67dad52ebbf0f6d1eef8639a9fd
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322603"
---
# <a name="d3dxsavemeshtox-function"></a>D3DXSaveMeshToX (funzione)

Salva una mesh in un file con estensione x.

## <a name="syntax"></a>Sintassi


```C++
HRESULT D3DXSaveMeshToX(
  _In_       LPCTSTR            pFilename,
  _In_       LPD3DXMESH         pMesh,
  _In_ const DWORD              *pAdjacency,
  _In_ const D3DXMATERIAL       *pMaterials,
  _In_ const D3DXEFFECTINSTANCE *pEffectInstances,
  _In_       DWORD              NumMaterials,
  _In_       DWORD              Format
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pFilename* \[ in\]
</dt> <dd>

Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**

Puntatore a una stringa che specifica il nome del file. Se le impostazioni del compilatore richiedono Unicode, il tipo di dati LPCTSTR viene risolto in LPCWSTR. In caso contrario, il tipo di dati String viene risolto in LPCSTR. Vedere la sezione Osservazioni.

</dd> <dt>

*pMesh* \[ in\]
</dt> <dd>

Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)**

Puntatore a un'interfaccia [**ID3DXMesh**](id3dxmesh.md) , che rappresenta la mesh da salvare in un file con estensione x.

</dd> <dt>

*pAdjacency* \[ in\]
</dt> <dd>

Tipo: **const [**DWORD**](../winprog/windows-data-types.md) \***

Puntatore a una matrice di tre DWORD per ogni volto che specifica i tre elementi adiacenti per ogni viso nella mesh. Questo parametro può essere **null**.

</dd> <dt>

*pMaterials* \[ in\]
</dt> <dd>

Tipo: **const [**D3DXMATERIAL**](d3dxmaterial.md) \***

Puntatore a una matrice di strutture [**D3DXMATERIAL**](d3dxmaterial.md) , che contiene le informazioni sul materiale da salvare nel file con estensione x.

</dd> <dt>

*pEffectInstances* \[ in\]
</dt> <dd>

Tipo: **const [**D3DXEFFECTINSTANCE**](d3dxeffectinstance.md) \***

Puntatore a una matrice di istanze di effetto, una per ogni gruppo di attributi nella mesh. Questo parametro può essere **null**. Un'istanza dell'effetto è una particolare istanza delle informazioni sullo stato usate per inizializzare un effetto. Per ulteriori informazioni, vedere [**D3DXEFFECTINSTANCE**](d3dxeffectinstance.md).

</dd> <dt>

*NumMaterials* \[ in\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Numero di strutture [**D3DXMATERIAL**](d3dxmaterial.md) nella matrice *pMaterials* .

</dd> <dt>

*Formato* \[ in\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Combinazione del formato di file e delle opzioni di salvataggio quando si salva un file con estensione x. Vedere [D3DX X file costanti](dx9-graphics-reference-d3dx-x-file-constants.md).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se la funzione ha esito positivo, il valore restituito è D3D \_ OK. Se la funzione ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Commenti

L'impostazione del compilatore determina anche la versione della funzione. Se è definito Unicode, la chiamata di funzione viene risolta in D3DXSaveMeshToXW. In caso contrario, la chiamata di funzione viene risolta in D3DXSaveMeshToXA perché vengono utilizzate le stringhe ANSI.

Il formato di file predefinito è binario; Tuttavia, se un file viene specificato sia come file binario sia come file di testo, verrà salvato come file di testo. Indipendentemente dal formato del file, è anche possibile usare il formato compresso per ridurre le dimensioni del file.

Di seguito è riportato un esempio di codice tipico di come usare questa funzione.


```
ID3DXMesh*    m_pMesh;           // Mesh object to be saved to a .x file
D3DXMATERIAL* m_pMaterials;      // Array of material structs in the mesh
DWORD         m_dwNumMaterials;  // Number of material structs in the mesh
    
DWORD dwFormat = D3DXF_FILEFORMAT_BINARY;  // Binary-format .x file (default)
// DWORD dwFormat = D3DXF_FILEFORMAT_TEXT; // Text-format .x file
    
// Load mesh into m_pMesh and determine values of m_pMaterials and 
// m_dwNumMaterials with calls to D3DXLoadMeshxxx or other D3DX functions
    
// ...
        
D3DXSaveMeshToX(
    L"outputxfilename.x",
    m_pMesh,
    NULL,
    m_pMaterials,
    NULL,
    m_dwNumMaterials,
    dwFormat );
```



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

 

 

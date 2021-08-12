---
description: Crea un file con estensione x e salva la gerarchia mesh e le animazioni corrispondenti.
ms.assetid: 803926fe-8cb7-422a-9920-56f7d0b0d0ea
title: Funzione D3DXSaveMeshHierarchyToFile (D3dx9anim.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSaveMeshHierarchyToFile
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 892d27e305badc2cf1b21de41a1f9d37da13f36c1521135a79a65619e31903f1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118298529"
---
# <a name="d3dxsavemeshhierarchytofile-function"></a>Funzione D3DXSaveMeshHierarchyToFile

Crea un file con estensione x e salva la gerarchia mesh e le animazioni corrispondenti.

## <a name="syntax"></a>Sintassi


```C++
HRESULT D3DXSaveMeshHierarchyToFile(
  _In_       LPCSTR                    pFilename,
  _In_       DWORD                     XFormat,
  _In_ const D3DXFRAME                 *pFrameRoot,
  _In_       LPD3DXANIMATIONCONTROLLER pAnimController,
  _In_       LPD3DXSAVEUSERDATA        pUserDataSaver
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pFilename* \[ Pollici\]
</dt> <dd>

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Puntatore a una stringa che specifica il nome del file con estensione x che identifica la mesh salvata. Se le impostazioni del compilatore richiedono Unicode, il tipo di dati LPCTSTR viene risolto in LPCWSTR. In caso contrario, il tipo di dati stringa viene risolto in LPCSTR. Vedere la sezione Osservazioni.

</dd> <dt>

*XFormat* \[ Pollici\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Formato del file con estensione x (testo o binario, compresso o meno). Vedere FILEFORMAT D3DXF. \_ D3DXF FILEFORMAT COMPRESSED può essere combinato (usando un OR logico) con i flag \_ \_ D3DXF FILEFORMAT BINARY o \_ \_ D3DXF \_ FILEFORMAT \_ TEXT per ridurre le dimensioni del file di output.

</dd> <dt>

*pFrameRoot* \[ Pollici\]
</dt> <dd>

Tipo: **const [**D3DXFRAME**](d3dxframe.md) \***

Nodo radice della gerarchia da salvare. Vedere [**D3DXFRAME**](d3dxframe.md).

</dd> <dt>

*pAnimController* \[ Pollici\]
</dt> <dd>

Tipo: **[ **LPD3DXANIMATIONCONTROLLER**](id3dxanimationcontroller.md)**

Controller di animazione con set di animazioni da archiviare. Vedere [**ID3DXAnimationController**](id3dxanimationcontroller.md).

</dd> <dt>

*pUserDataSaver* \[ Pollici\]
</dt> <dd>

Tipo: **[ **LPD3DXSAVEUSERDATA**](id3dxsaveuserdata.md)**

Interfaccia fornita dall'applicazione che consente di salvare i dati utente. Vedere [**ID3DXSaveUserData**](id3dxsaveuserdata.md).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se la funzione ha esito positivo, il valore restituito è D3D \_ OK. Se la funzione ha esito negativo, il valore restituito può essere: D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Commenti

L'impostazione del compilatore determina anche la versione della funzione. Se unicode è definito, la chiamata di funzione viene risolta in D3DXSaveMeshHierarchyToFileW. In caso contrario, la chiamata di funzione viene risolta in D3DXSaveMeshHierarchyToFileA.

Questa funzione non salva i set di animazioni compressi.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9anim.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni di animazione](dx9-graphics-reference-d3dx-functions-animation.md)
</dt> <dt>

[Informazioni di riferimento sul file X](dx9-graphics-reference-d3dx-x-file.md)
</dt> </dl>

 

 

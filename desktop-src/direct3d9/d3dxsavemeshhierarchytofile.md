---
description: Crea un file con estensione x e salva la gerarchia mesh e le relative animazioni corrispondenti.
ms.assetid: 803926fe-8cb7-422a-9920-56f7d0b0d0ea
title: Funzione D3DXSaveMeshHierarchyToFile (D3dx9anim. h)
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
ms.openlocfilehash: f2de65f9bc2f9e40a5bc07c6f0b4d00112f0df21
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322604"
---
# <a name="d3dxsavemeshhierarchytofile-function"></a>D3DXSaveMeshHierarchyToFile (funzione)

Crea un file con estensione x e salva la gerarchia mesh e le relative animazioni corrispondenti.

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

*pFilename* \[ in\]
</dt> <dd>

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Puntatore a una stringa che specifica il nome del file con estensione x che identifica la mesh salvata. Se le impostazioni del compilatore richiedono Unicode, il tipo di dati LPCTSTR viene risolto in LPCWSTR. In caso contrario, il tipo di dati String viene risolto in LPCSTR. Vedere la sezione Osservazioni.

</dd> <dt>

*XFormat* \[ in\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Formato del file con estensione x (testo o binario, compresso o meno). Vedere D3DXF \_ FILEformat. D3DXF \_ FileFormat \_ compresso può essere combinato (usando un OR logico) con i flag di testo FileFormat D3DXF \_ \_ o D3DXF \_ \_ per ridurre le dimensioni del file di output.

</dd> <dt>

*pFrameRoot* \[ in\]
</dt> <dd>

Tipo: **const [**D3DXFRAME**](d3dxframe.md) \***

Nodo radice della gerarchia da salvare. Vedere [**D3DXFRAME**](d3dxframe.md).

</dd> <dt>

*pAnimController* \[ in\]
</dt> <dd>

Tipo: **[ **LPD3DXANIMATIONCONTROLLER**](id3dxanimationcontroller.md)**

Controller di animazione con set di animazioni da archiviare. Vedere [**ID3DXAnimationController**](id3dxanimationcontroller.md).

</dd> <dt>

*pUserDataSaver* \[ in\]
</dt> <dd>

Tipo: **[ **LPD3DXSAVEUSERDATA**](id3dxsaveuserdata.md)**

Interfaccia fornita dall'applicazione che consente il salvataggio dei dati utente. Vedere [**ID3DXSaveUserData**](id3dxsaveuserdata.md).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se la funzione ha esito positivo, il valore restituito è D3D \_ OK. Se la funzione ha esito negativo, il valore restituito può essere: D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Commenti

L'impostazione del compilatore determina anche la versione della funzione. Se è definito Unicode, la chiamata di funzione viene risolta in D3DXSaveMeshHierarchyToFileW. In caso contrario, la chiamata di funzione viene risolta in D3DXSaveMeshHierarchyToFileA.

Questa funzione non salva i set di animazioni compressi.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni di animazione](dx9-graphics-reference-d3dx-functions-animation.md)
</dt> <dt>

[Riferimento al file X](dx9-graphics-reference-d3dx-x-file.md)
</dt> </dl>

 

 

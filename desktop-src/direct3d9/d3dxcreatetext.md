---
description: Crea una mesh contenente il testo specificato, usando il tipo di carattere associato al contesto di dispositivo.
ms.assetid: 1c8b0dc6-51b8-45bf-b4c0-b67e3d128097
title: Funzione D3DXCreateText (D3dx9shape. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateText
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 4f6202a534dde727e21b6513ad30077f2e3b3e52
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322724"
---
# <a name="d3dxcreatetext-function"></a>D3DXCreateText (funzione)

Crea una mesh contenente il testo specificato, usando il tipo di carattere associato al contesto di dispositivo.

## <a name="syntax"></a>Sintassi


```C++
HRESULT D3DXCreateText(
  _In_  LPDIRECT3DDEVICE9   pDevice,
  _In_  HDC                 hDC,
  _In_  LPCTSTR             pText,
  _In_  FLOAT               Deviation,
  _In_  FLOAT               Extrusion,
  _Out_ LPD3DXMESH          *ppMesh,
  _Out_ LPD3DXBUFFER        *ppAdjacency,
  _Out_ LPGLYPHMETRICSFLOAT pGlyphMetrics
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*PDEVICE* \[ in\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Puntatore al dispositivo che ha creato la mesh.

</dd> <dt>

*HDC* \[ in\]
</dt> <dd>

Tipo: **HDC**

Contesto di dispositivo, contenente il tipo di carattere per l'output. Il tipo di carattere selezionato dal contesto di dispositivo deve essere un tipo di carattere TrueType.

</dd> <dt>

*ptext* \[ in\]
</dt> <dd>

Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**

Puntatore a una stringa che specifica il testo da generare. Se le impostazioni del compilatore richiedono Unicode, il tipo di dati LPCTSTR viene risolto in LPCWSTR. In caso contrario, il tipo di dati String viene risolto in LPCSTR. Vedere la sezione Osservazioni.

</dd> <dt>

*Deviazione* \[ in\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

Deviazione massima delle linee dei tipi di carattere TrueType.

</dd> <dt>

*Estrusione* \[ in\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

Quantità per estrudere il testo nella direzione della z negativa.

</dd> <dt>

*ppMesh* \[ out\]
</dt> <dd>

Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)\***

Puntatore alla mesh restituita.

</dd> <dt>

*ppAdjacency* \[ out\]
</dt> <dd>

Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Puntatore a un buffer contenente le informazioni adiacenza. Può essere **null**.

</dd> <dt>

*pGlyphMetrics* \[ out\]
</dt> <dd>

Tipo: **[ **LPGLYPHMETRICSFLOAT**](/windows/win32/api/wingdi/ns-wingdi-glyphmetricsfloat)**

Puntatore a una matrice di strutture [**GLYPHMETRICSFLOAT**](/windows/win32/api/wingdi/ns-wingdi-glyphmetricsfloat) che contengono i dati della metrica del glifo. Ogni elemento contiene informazioni sulla posizione e sull'orientamento del glifo corrispondente nella stringa. Il numero di elementi nella matrice deve essere uguale al numero di caratteri nella stringa. Si noti che l'origine in ogni struttura non è relativa all'intera stringa, bensì è relativa a tale cella di caratteri. Per calcolare l'intero rettangolo di delimitazione, aggiungere l'incremento per ogni glifo durante l'attraversamento della stringa. Se non si è interessati alle dimensioni del glifo, impostare questo parametro su **null**.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se la funzione ha esito positivo, il valore restituito è D3D \_ OK. Se la funzione ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OutOfMemory.

## <a name="remarks"></a>Commenti

L'impostazione del compilatore determina anche la versione della funzione. Se è definito Unicode, la chiamata di funzione viene risolta in D3DXCreateTextW. In caso contrario, la chiamata di funzione viene risolta in D3DXCreateTextA perché vengono utilizzate le stringhe ANSI.

Questa funzione crea una mesh con l' \_ opzione di creazione gestita D3DXMESH e [D3DFVF \_ xyz \| D3DFVF \_ Normal](d3dfvf.md) Flexible Vertex Format (FVF).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9shape. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>    |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni di disegno di forme](dx9-graphics-reference-d3dx-functions-shape.md)
</dt> </dl>

 

 

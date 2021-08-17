---
description: Cerca un commento specifico in uno shader. Il commento è identificato da un codice a quattro caratteri (FOURCC) nel primo DWORD del commento.
ms.assetid: 86ab8330-fd48-4d14-835c-92399c6c8a38
title: Funzione D3DXFindShaderComment (D3DX9Shader.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFindShaderComment
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 07ff15b77866732f7a2dcab814e1ccf84d5344f640d83300af874e162485879b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118096056"
---
# <a name="d3dxfindshadercomment-function"></a>Funzione D3DXFindShaderComment

Cerca un commento specifico in uno shader. Il commento è identificato da un codice a quattro caratteri (FOURCC) nel primo DWORD del commento.

## <a name="syntax"></a>Sintassi


```C++
HRESULT D3DXFindShaderComment(
  _In_  const DWORD   *pFunction,
  _In_        DWORD   FourCC,
  _In_        LPCVOID *ppData,
  _Out_       UINT    *pSizeInBytes
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pFunction* \[ Pollici\]
</dt> <dd>

Tipo: **const [**DWORD**](../winprog/windows-data-types.md) \***

Puntatore al flusso DWORD della funzione shader.

</dd> <dt>

*FourCC* \[ Pollici\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Codice FOURCC che identifica il blocco di commenti. Vedere [FourCC Formats (Formati FourCC).](d3dformat.md)

</dd> <dt>

*ppData* \[ Pollici\]
</dt> <dd>

Tipo: **[ **LPCVOID**](../winprog/windows-data-types.md)\***

Restituisce un puntatore ai dati di commento (senza includere il token di commento e il codice FOURCC). Questo valore può essere **NULL.**

</dd> <dt>

*pSizeInBytes* \[ Cambio\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)\***

Restituisce le dimensioni in byte dei dati di commento. Questo valore può essere **NULL.**

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se la funzione ha esito positivo, il valore restituito è D3D \_ OK. Se il commento non viene trovato e non si è verificato alcun altro errore, viene restituito S \_ FALSE.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Shader.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni shader](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> </dl>

 

 

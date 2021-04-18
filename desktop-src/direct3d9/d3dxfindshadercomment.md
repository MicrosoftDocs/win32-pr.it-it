---
description: Cerca uno shader per un commento specifico. Il commento è identificato da un codice di quattro caratteri (FOURCC) nel primo valore DWORD del commento.
ms.assetid: 86ab8330-fd48-4d14-835c-92399c6c8a38
title: Funzione D3DXFindShaderComment (D3DX9Shader. h)
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
ms.openlocfilehash: 394c72bcf7076075318cd664cf56bbb464d7e3cf
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322693"
---
# <a name="d3dxfindshadercomment-function"></a>D3DXFindShaderComment (funzione)

Cerca uno shader per un commento specifico. Il commento è identificato da un codice di quattro caratteri (FOURCC) nel primo valore DWORD del commento.

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

*pFunction* \[ in\]
</dt> <dd>

Tipo: **const [**DWORD**](../winprog/windows-data-types.md) \***

Puntatore al flusso DWORD della funzione shader.

</dd> <dt>

*Fourcc* \[ in\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Codice FOURCC che identifica il blocco di commento. Vedere [formati FourCC](d3dformat.md).

</dd> <dt>

*ppData* \[ in\]
</dt> <dd>

Tipo: **[ **LPCVOID**](../winprog/windows-data-types.md)\***

Restituisce un puntatore ai dati di commento, escluso il token di commento e il codice FOURCC. Questo valore può essere **null**.

</dd> <dt>

*pSizeInBytes* \[ out\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)\***

Restituisce le dimensioni in byte dei dati di commento. Questo valore può essere **null**.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se la funzione ha esito positivo, il valore restituito è D3D \_ OK. Se il commento non viene trovato e non si sono verificati altri errori, \_ viene restituito S false.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Shader. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni shader](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> </dl>

 

 

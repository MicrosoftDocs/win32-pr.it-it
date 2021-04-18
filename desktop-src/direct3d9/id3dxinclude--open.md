---
description: Metodo implementato dall'utente per l'apertura e la lettura del contenuto di un \# file di inclusione dello shader.
ms.assetid: ad0105f7-042d-4e96-ad4a-1ece08e519af
title: 'Metodo ID3DXInclude:: Open (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXInclude.Open
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 313b3f4845f9a46f758a40b6b315cc5b5eeecb29
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323532"
---
# <a name="id3dxincludeopen-method"></a>Metodo ID3DXInclude:: Open

Metodo implementato dall'utente per l'apertura e la lettura del contenuto di un \# file di inclusione dello shader.

## <a name="syntax"></a>Sintassi


```C++
HRESULT Open(
  [in]  D3DXINCLUDE_TYPE IncludeType,
  [in]  LPCSTR           pFileName,
  [in]  LPCVOID          pParentData,
  [out] LPCVOID          *ppData,
  [out] UINT             *pBytes
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*IncludeType* \[ in\]
</dt> <dd>

Tipo: **[ **D3DXINCLUDE \_**](./d3dxinclude-type.md)**

Percorso del file di \# inclusione. Vedere [**D3DXINCLUDE \_ Type**](./d3dxinclude-type.md).

</dd> <dt>

*pFileName* \[ in\]
</dt> <dd>

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Nome del \# file di inclusione.

</dd> <dt>

*pParentData* \[ in\]
</dt> <dd>

Tipo: **[ **LPCVOID**](../winprog/windows-data-types.md)**

Puntatore al contenitore che include il \# file di inclusione. Il compilatore potrebbe passare NULL in *pParentData*. Per ulteriori informazioni, vedere la sezione "ricerca di file di inclusione" in [compilare un effetto (Direct3D 11)](../direct3d11/d3d11-graphics-programming-guide-effects-compile.md).

</dd> <dt>

*ppData* \[ out\]
</dt> <dd>

Tipo: **[ **LPCVOID**](../winprog/windows-data-types.md)\***

Puntatore al buffer restituito che contiene le direttive include. Questo puntatore rimane valido fino a quando non viene chiamato [**ID3DXInclude:: Close**](id3dxinclude--close.md) .

</dd> <dt>

*pBytes* \[ out\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)\***

Numero di byte restituiti in ppData.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Il metodo implementato dall'utente deve restituire S \_ OK. Se il callback ha esito negativo durante la lettura del \# file di inclusione, l'API che ha causato la chiamata al callback avrà esito negativo. I possibili valori sono i seguenti:

-   Lo shader HLSL non riuscirà a eseguire una delle \* \* \* funzioni D3DXCompileShader.
-   L'assembly shader non riuscirà a eseguire una delle \* \* \* funzioni D3DXAssembleShader.
-   L'effetto avrà esito negativo per una delle \* \* \* funzioni D3DXCreateEffect o D3DXCreateEffectCompiler \* \* \* .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Shader. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXInclude](id3dxinclude.md)
</dt> <dt>

[**ID3DXInclude:: Close**](id3dxinclude--close.md)
</dt> </dl>

 

 

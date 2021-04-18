---
description: Ottiene una costante cercando il relativo indice.
ms.assetid: 7d3ab655-b50d-41ab-a4ca-c7b534e00e3f
title: 'Metodo ID3DXTextureShader:: getconstant (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureShader.GetConstant
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 24f3f78d5970d5e3beda119ca40a565f45d0d950
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323362"
---
# <a name="id3dxtextureshadergetconstant-method"></a>Metodo ID3DXTextureShader:: getconstant

Ottiene una costante cercando il relativo indice.

## <a name="syntax"></a>Sintassi


```C++
D3DXHANDLE GetConstant(
  [in] D3DXHANDLE hConstant,
  [in] UINT       Index
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hConstant* \[ in\]
</dt> <dd>

Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

[Handle](handles.md) per la struttura dei dati padre. Se la costante è un parametro di primo livello (non esiste una struttura di dati padre), usare **null**.

</dd> <dt>

*Indice* \[ di in\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Indice in base zero della costante.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Restituisce un identificatore univoco alla costante.

## <a name="remarks"></a>Commenti

Per ottenere una costante da una matrice di costanti, usare [**ID3DXTextureShader:: Getconstantelement**](id3dxtextureshader--getconstantelement.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Shader. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXTextureShader](id3dxtextureshader.md)
</dt> </dl>

 

 

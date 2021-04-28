---
description: "Metodo ID3DXTextureShader::GetConstant: ottiene una costante cercandone l'indice."
ms.assetid: 7d3ab655-b50d-41ab-a4ca-c7b534e00e3f
title: Metodo ID3DXTextureShader::GetConstant (D3DX9Shader.h)
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
ms.openlocfilehash: edcc4b6a7f34c12be7013f2ae1e0b2e6d991a5d6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108117669"
---
# <a name="id3dxtextureshadergetconstant-method"></a>Metodo ID3DXTextureShader::GetConstant

Ottiene una costante cercandone l'indice.

## <a name="syntax"></a>Sintassi


```C++
D3DXHANDLE GetConstant(
  [in] D3DXHANDLE hConstant,
  [in] UINT       Index
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hConstant* \[ Pollici\]
</dt> <dd>

Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Handle [per](handles.md) la struttura dei dati padre. Se la costante è un parametro di primo livello (non è presente alcuna struttura di dati padre), usare **NULL.**

</dd> <dt>

*Indice* \[ Pollici\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Indice in base zero della costante.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Restituisce un identificatore univoco per la costante.

## <a name="remarks"></a>Commenti

Per ottenere una costante da una matrice di costanti, usare [**ID3DXTextureShader::GetConstantElement**](id3dxtextureshader--getconstantelement.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Shader.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXTextureShader](id3dxtextureshader.md)
</dt> </dl>

 

 

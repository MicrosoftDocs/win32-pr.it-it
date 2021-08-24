---
description: Ottenere una costante dalla tabella delle costanti.
ms.assetid: ebb05a09-af20-4c71-8594-940fce3a97e7
title: Metodo ID3DXTextureShader::GetConstantElement (D3DX9Shader.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureShader.GetConstantElement
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 02d21efb3ef0ed5d4602833571b2b1a32e73df73b76f82a357cda574e93e84ce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119747390"
---
# <a name="id3dxtextureshadergetconstantelement-method"></a>Metodo ID3DXTextureShader::GetConstantElement

Ottenere una costante dalla tabella delle costanti.

## <a name="syntax"></a>Sintassi


```C++
D3DXHANDLE GetConstantElement(
  [in] D3DXHANDLE hConstant,
  [in] UINT       Index
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hConstant* \[ Pollici\]
</dt> <dd>

Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Handle [per](handles.md) la matrice di costanti. Questo valore non può essere **NULL.**

</dd> <dt>

*Indice* \[ Pollici\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Indice in base zero dell'elemento nella tabella delle costanti.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Restituisce un identificatore univoco per la costante.

## <a name="remarks"></a>Commenti

Per ottenere una costante che non fa parte di una matrice, usare [**ID3DXTextureShader::GetConstant**](id3dxtextureshader--getconstant.md) o [**ID3DXTextureShader::GetConstantByName**](id3dxtextureshader--getconstantbyname.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Shader.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXTextureShader](id3dxtextureshader.md)
</dt> </dl>

 

 

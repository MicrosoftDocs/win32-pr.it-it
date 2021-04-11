---
description: Ottenere una costante dalla tabella delle costanti.
ms.assetid: ebb05a09-af20-4c71-8594-940fce3a97e7
title: 'Metodo ID3DXTextureShader:: getconstantelement (D3DX9Shader. h)'
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
ms.openlocfilehash: 44b5089b6e539a8104586e27b58388a324462b37
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104235045"
---
# <a name="id3dxtextureshadergetconstantelement-method"></a>Metodo ID3DXTextureShader:: getconstantelement

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

*hConstant* \[ in\]
</dt> <dd>

Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

[Handle](handles.md) per la matrice di costanti. Questo valore non può essere **null**.

</dd> <dt>

*Indice* \[ di in\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Indice in base zero dell'elemento nella tabella Constant.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Restituisce un identificatore univoco alla costante.

## <a name="remarks"></a>Commenti

Per ottenere una costante che non fa parte di una matrice, usare [**ID3DXTextureShader:: getconstant**](id3dxtextureshader--getconstant.md) o [**ID3DXTextureShader:: GetConstantByName**](id3dxtextureshader--getconstantbyname.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Shader. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXTextureShader](id3dxtextureshader.md)
</dt> </dl>

 

 

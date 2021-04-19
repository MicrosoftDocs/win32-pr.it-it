---
description: Ottiene una costante cercandone il nome.
ms.assetid: 0c57f6ce-ea81-4b34-9251-c385bfe6ebe7
title: 'Metodo ID3DXTextureShader:: GetConstantByName (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureShader.GetConstantByName
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a285da2fa3179f91d34eda8d9ce1f622c86df15b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323360"
---
# <a name="id3dxtextureshadergetconstantbyname-method"></a>Metodo ID3DXTextureShader:: GetConstantByName

Ottiene una costante cercandone il nome.

## <a name="syntax"></a>Sintassi


```C++
D3DXHANDLE GetConstantByName(
  [in] D3DXHANDLE hConstant,
  [in] LPCSTR     pName
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hConstant* \[ in\]
</dt> <dd>

Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

[Handle](handles.md) per la struttura dei dati padre. Se la costante è un parametro di primo livello (non esiste una struttura di dati padre), usare **null**.

</dd> <dt>

*pname* \[ in\]
</dt> <dd>

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Stringa che contiene il nome della costante.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Restituisce un identificatore univoco alla costante.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Shader. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXTextureShader](id3dxtextureshader.md)
</dt> </dl>

 

 

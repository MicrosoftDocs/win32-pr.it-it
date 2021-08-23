---
description: Restituisce l'indice del campionatore.
ms.assetid: vs|directx_sdk|~\id3dxconstanttable__getsamplerindex.htm
title: Metodo ID3DXConstantTable::GetSamplerIndex (D3DX9Shader.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXConstantTable.GetSamplerIndex
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 65dac22cc15e93198e7d494986b2279ae7e1d11fdb3c8cb65b3caddf9b905595
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118987571"
---
# <a name="id3dxconstanttablegetsamplerindex-method"></a>Metodo ID3DXConstantTable::GetSamplerIndex

Restituisce l'indice del campionatore.

## <a name="syntax"></a>Sintassi


```C++
UINT GetSamplerIndex(
  [out] D3DXHANDLE hConstant
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hConstant* \[ Cambio\]
</dt> <dd>

Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Handle del campionatore.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Restituisce il numero di indice del campionatore dalla tabella delle costanti.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Shader.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXConstantTable](id3dxconstanttable.md)
</dt> </dl>

 

 

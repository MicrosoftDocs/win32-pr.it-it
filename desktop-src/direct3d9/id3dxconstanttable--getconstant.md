---
description: "Metodo ID3DXConstantTable::GetConstant: ottiene una costante cercandone l'indice."
ms.assetid: 7db25171-9bda-4db8-b6a8-8a4d60a842f7
title: Metodo ID3DXConstantTable::GetConstant (D3DX9Shader.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXConstantTable.GetConstant
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 2d4c2e268e456f1e4462b033a046ce71f10a8e854e377e4d4104ee5abde3accc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119748881"
---
# <a name="id3dxconstanttablegetconstant-method"></a>Metodo ID3DXConstantTable::GetConstant

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

Identificatore univoco della struttura dei dati padre. Se la costante è un parametro di primo livello (non è presente alcuna struttura di dati padre), usare **NULL.**

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

Per ottenere una costante da una matrice di costanti, usare [**ID3DXConstantTable::GetConstantElement**](id3dxconstanttable--getconstantelement.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Shader.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXConstantTable](id3dxconstanttable.md)
</dt> </dl>

 

 

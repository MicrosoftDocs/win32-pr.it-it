---
description: Ottiene una costante da una matrice di costanti. Una matrice è costituito da elementi .
ms.assetid: 20a61207-b0e1-455d-9b65-0fade543d1cf
title: Metodo ID3DXConstantTable::GetConstantElement (D3DX9Shader.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXConstantTable.GetConstantElement
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9cb1adacadb92cf3a2f9a3e041e4a94a840994db3244233509350448008bd675
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119748781"
---
# <a name="id3dxconstanttablegetconstantelement-method"></a>Metodo ID3DXConstantTable::GetConstantElement

Ottiene una costante da una matrice di costanti. Una matrice è costituito da elementi .

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

Identificatore univoco della matrice di costanti. Questo valore non può essere **NULL.**

</dd> <dt>

*Indice* \[ Pollici\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Indice in base zero dell'elemento nella matrice.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Restituisce un identificatore univoco per la costante dell'elemento.

## <a name="remarks"></a>Commenti

Per ottenere una costante che non fa parte di una matrice, usare [**ID3DXConstantTable::GetConstant**](id3dxconstanttable--getconstant.md) o [**ID3DXConstantTable::GetConstantByName**](id3dxconstanttable--getconstantbyname.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Shader.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXConstantTable](id3dxconstanttable.md)
</dt> </dl>

 

 

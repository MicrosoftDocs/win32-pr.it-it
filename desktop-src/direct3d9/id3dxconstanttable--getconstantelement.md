---
description: Ottiene una costante da una matrice di costanti. Una matrice è costituita da elementi.
ms.assetid: 20a61207-b0e1-455d-9b65-0fade543d1cf
title: 'Metodo ID3DXConstantTable:: getconstantelement (D3DX9Shader. h)'
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
ms.openlocfilehash: 5396c70c1c4286223d9f45fb8ab9b73a019becb1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322823"
---
# <a name="id3dxconstanttablegetconstantelement-method"></a>Metodo ID3DXConstantTable:: getconstantelement

Ottiene una costante da una matrice di costanti. Una matrice è costituita da elementi.

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

Identificatore univoco della matrice di costanti. Questo valore non può essere **null**.

</dd> <dt>

*Indice* \[ di in\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Indice in base zero dell'elemento nella matrice.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Restituisce un identificatore univoco della costante dell'elemento.

## <a name="remarks"></a>Commenti

Per ottenere una costante che non fa parte di una matrice, usare [**ID3DXConstantTable:: getconstant**](id3dxconstanttable--getconstant.md) o [**ID3DXConstantTable:: GetConstantByName**](id3dxconstanttable--getconstantbyname.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Shader. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXConstantTable](id3dxconstanttable.md)
</dt> </dl>

 

 

---
description: Ottiene un puntatore a una matrice di descrizioni costanti nella tabella delle costanti.
ms.assetid: bd407fd6-b1cc-4197-ae98-1c2ca74d2ad0
title: Metodo ID3DXConstantTable::GetConstantDesc (D3DX9Shader.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXConstantTable.GetConstantDesc
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8462ccfbbf306da08c67d460584a470d82301a5bda5f95a1ad09b2062702ee62
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119607211"
---
# <a name="id3dxconstanttablegetconstantdesc-method"></a>Metodo ID3DXConstantTable::GetConstantDesc

Ottiene un puntatore a una matrice di descrizioni costanti nella tabella delle costanti.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetConstantDesc(
  [in]      D3DXHANDLE        hConstant,
  [in, out] D3DXCONSTANT_DESC *pDesc,
  [in, out] UINT              *pCount
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hConstant* \[ Pollici\]
</dt> <dd>

Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Identificatore univoco di una costante. Vedere [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).

</dd> <dt>

*pDesc* \[ in, out\]
</dt> <dd>

Tipo: **[ **D3DXCONSTANT \_ DESC**](d3dxconstant-desc.md)\***

Restituisce un puntatore a una matrice di descrizioni. Vedere [**D3DXCONSTANT \_ DESC**](d3dxconstant-desc.md).

</dd> <dt>

*pCount* \[ in, out\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)\***

L'input fornito deve essere la dimensione massima della matrice. L'output è il numero di elementi che vengono compilati nella matrice quando la funzione restituisce .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è D3D \_ OK. Se il metodo ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.

## <a name="remarks"></a>Commenti

**ID3DXConstantTable::GetConstantDesc** restituisce talvolta un [**D3DXCONSTANT \_ DESC**](d3dxconstant-desc.md) con un numero di registri \_ 0. Questa operazione si verifica quando una costante viene visualizzata in più set di registri, ma non dispone di spazio \_ in tale set di registri allocato.

Poiché un campionatore può essere visualizzato più volte in una tabella costante, questo metodo può restituire una matrice di descrizioni, ognuna con un indice di registro diverso.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Shader.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXConstantTable](id3dxconstanttable.md)
</dt> <dt>

[**ID3DXConstantTable::GetDesc**](id3dxconstanttable--getdesc.md)
</dt> </dl>

 

 

---
description: Ottiene un puntatore a una matrice di descrizioni di costanti nella tabella delle costanti.
ms.assetid: bd407fd6-b1cc-4197-ae98-1c2ca74d2ad0
title: 'Metodo ID3DXConstantTable:: GetConstantDesc (D3DX9Shader. h)'
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
ms.openlocfilehash: e5574c72fabd7561da0c60c903ae815faaebbfd5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103969376"
---
# <a name="id3dxconstanttablegetconstantdesc-method"></a>Metodo ID3DXConstantTable:: GetConstantDesc

Ottiene un puntatore a una matrice di descrizioni di costanti nella tabella delle costanti.

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

*hConstant* \[ in\]
</dt> <dd>

Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Identificatore univoco di una costante. Vedere [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).

</dd> <dt>

*pDesc* \[ in uscita\]
</dt> <dd>

Tipo: **[ **D3DXCONSTANT \_ desc**](d3dxconstant-desc.md)\***

Restituisce un puntatore a una matrice di descrizioni. Vedere [**D3DXCONSTANT \_ desc**](d3dxconstant-desc.md).

</dd> <dt>

*pcount* \[ in uscita\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)\***

L'input specificato deve corrispondere alla dimensione massima della matrice. L'output è il numero di elementi che vengono compilati nella matrice quando la funzione restituisce.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è D3D \_ OK. Se il metodo ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.

## <a name="remarks"></a>Commenti

**ID3DXConstantTable:: GetConstantDesc** a volte restituisce una [**\_ Descrizione D3DXCONSTANT**](d3dxconstant-desc.md) con un \_ conteggio dei registri pari a 0. Questa operazione viene eseguita con una costante presente in più di un \_ set di registri, ma in tale set di registri non è allocato spazio.

Poiché un campionatore può apparire più di una volta in una tabella costante, questo metodo può restituire una matrice di descrizioni, ognuna con un indice di registro diverso.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Shader. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXConstantTable](id3dxconstanttable.md)
</dt> <dt>

[**ID3DXConstantTable:: getdesc**](id3dxconstanttable--getdesc.md)
</dt> </dl>

 

 

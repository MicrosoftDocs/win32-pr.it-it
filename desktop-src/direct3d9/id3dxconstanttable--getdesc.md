---
description: 'Metodo ID3DXConstantTable::GetDesc: ottiene una descrizione della tabella delle costanti.'
ms.assetid: 3a7396c6-3a3e-44c2-96b7-60339015b376
title: Metodo ID3DXConstantTable::GetDesc (D3DX9Shader.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXConstantTable.GetDesc
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9e905eceefec4ea2e057776f1045a8fc7f7f213e38328406935c6095efd9c22c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119607131"
---
# <a name="id3dxconstanttablegetdesc-method"></a>Metodo ID3DXConstantTable::GetDesc

Ottiene una descrizione della tabella delle costanti.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetDesc(
  [in] D3DXCONSTANTTABLE_DESC *pDesc
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pDesc* \[ Pollici\]
</dt> <dd>

Tipo: **[ **D3DXCONSTANTTABLE \_ DESC**](d3dxconstanttable-desc.md)\***

Descrizione della tabella delle costanti. Vedere [**D3DXCONSTANTTABLE \_ DESC.**](d3dxconstanttable-desc.md)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è D3D \_ OK. Se il metodo ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Shader.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXConstantTable](id3dxconstanttable.md)
</dt> <dt>

[**ID3DXConstantTable::GetConstantDesc**](id3dxconstanttable--getconstantdesc.md)
</dt> </dl>

 

 





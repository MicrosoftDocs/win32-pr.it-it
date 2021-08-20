---
description: Limitare il numero di emische che possono influenzare un vertice e/o limitare la quantità di influenza che può avere un recidro su un vertice.
ms.assetid: 75c4d2eb-0a43-494d-9642-4c08aa814794
title: Metodo ID3DX10SkinInfo::Compact (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10SkinInfo.Compact
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 3aab3534ea55d2f6675ef1e65b03d19f4c516562b242e284ee2865f98bc03f18
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119046909"
---
# <a name="id3dx10skininfocompact-method"></a>Metodo ID3DX10SkinInfo::Compact

Limitare il numero di emische che possono influenzare un vertice e/o limitare la quantità di influenza che può avere un recidro su un vertice.

## <a name="syntax"></a>Sintassi


```C++
HRESULT Compact(
  [in] UINT  MaxPerVertexInfluences,
  [in] UINT  ScaleMode,
  [in] float MinWeight
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*MaxPerVertexInfluences* \[ Pollici\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Numero massimo di animali che possono influenzare qualsiasi vertice specificato. Questo valore viene ignorato se è maggiore del valore restituito da [**ID3DX10SkinInfo::GetMaxBoneInfluences**](id3dx10skininfo-getmaxboneinfluences.md).

</dd> <dt>

*ScaleMode* \[ Pollici\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Flag che descrive come ridimensionare i pesi rimanenti su un determinato vertice dopo che alcuni sono stati sfalsati da MinWeight. Se si specifica D3DX10 SKININFO NO SCALING, i pesi non \_ \_ verranno \_ ridimensionati. Se si specifica D3DX10 SKININFO SCALE TO 1, i pesi maggiori di MinWeight verranno ridimensionati in modo da aggiungere fino a \_ \_ \_ \_ 1,0. Se si specifica D3DX10 SKININFO SCALE TO TOTAL, i pesi maggiori di MinWeight verranno ridimensionati in modo da aggiungere fino al totale \_ \_ \_ \_ originale.

</dd> <dt>

*MinWeight* \[ Pollici\]
</dt> <dd>

Tipo: **float**

Percentuale minima di influenza, o peso, che qualsiasi cane può avere su qualsiasi vertice. Questo valore deve essere compreso tra 0 e 1.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è S \_ OK. Se il metodo ha esito negativo, il valore restituito può essere E \_ OUTOFMEMORY o E \_ INVALIDARG.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX10.h</dt> </dl>   |
| Libreria<br/> | <dl> <dt>D3DX10.lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DX10SkinInfo](id3dx10skininfo.md)
</dt> <dt>

[Interfacce D3DX](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 

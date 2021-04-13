---
description: Limitare il numero di ossa che possono influenzare un vertice e/o limitare la quantità di influenza che può avere un osso su un vertice.
ms.assetid: 75c4d2eb-0a43-494d-9642-4c08aa814794
title: 'Metodo ID3DX10SkinInfo:: Compact (D3DX10. h)'
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
ms.openlocfilehash: 379343688a1fd2ffe5ebd968dc984fa09faada7d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104401944"
---
# <a name="id3dx10skininfocompact-method"></a>Metodo ID3DX10SkinInfo:: Compact

Limitare il numero di ossa che possono influenzare un vertice e/o limitare la quantità di influenza che può avere un osso su un vertice.

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

*MaxPerVertexInfluences* \[ in\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Numero massimo di ossa che possono influenzare qualsiasi vertice specificato. Questo valore viene ignorato se è maggiore del valore restituito da [**ID3DX10SkinInfo:: GetMaxBoneInfluences**](id3dx10skininfo-getmaxboneinfluences.md).

</dd> <dt>

*ScaleMode* \[ in\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Flag che descrive come ridimensionare i pesi rimanenti su un determinato vertice dopo che alcuni sono stati tagliati da MinWeight. Se D3DX10 \_ SKININFO \_ non \_ viene specificato alcun ridimensionamento, i pesi non verranno ridimensionati. Se \_ \_ si specifica d3dx10 SKININFO scale \_ a \_ 1, i pesi maggiori di MinWeight verranno scalati in modo da aggiungerli fino a 1,0. Se \_ \_ si specifica d3dx10 SKININFO scale \_ to \_ Total, i pesi maggiori di MinWeight verranno ridimensionati in modo da aggiungerli al totale originale.

</dd> <dt>

*MinWeight* \[ in\]
</dt> <dd>

Tipo: **float**

Percentuale minima di influenza, o peso, che qualsiasi osso può avere su qualsiasi vertice. Questo valore deve essere compreso tra 0 e 1.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è \_ OK. Se il metodo ha esito negativo, il valore restituito può essere: E \_ OutOfMemory o e \_ INVALIDARG.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX10. h</dt> </dl>   |
| Libreria<br/> | <dl> <dt>D3DX10. lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DX10SkinInfo](id3dx10skininfo.md)
</dt> <dt>

[Interfacce D3DX](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 

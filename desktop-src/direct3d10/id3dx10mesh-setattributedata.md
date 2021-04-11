---
description: Imposta i dati dell'attributo della mesh.
ms.assetid: bcf7b1b3-b923-400a-8d12-5094f3844d8f
title: 'Metodo ID3DX10Mesh:: SetAttributeData (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.SetAttributeData
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 19d69f8747196d7b25c85cb04fb173adef193098
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104235114"
---
# <a name="id3dx10meshsetattributedata-method"></a>Metodo ID3DX10Mesh:: SetAttributeData

Imposta i dati dell'attributo della mesh.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetAttributeData(
  [in] const UINT *pData
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pData* \[ in\]
</dt> <dd>

Tipo: **const [**uint**](../winprog/windows-data-types.md) \***

Dati dell'attributo da impostare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Il valore restituito è uno dei valori elencati in [codici restituiti Direct3D 10](d3d10-graphics-reference-returnvalues.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX10. h</dt> </dl>   |
| Libreria<br/> | <dl> <dt>D3DX10. lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DX10Mesh](id3dx10mesh.md)
</dt> <dt>

[Interfacce D3DX](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 

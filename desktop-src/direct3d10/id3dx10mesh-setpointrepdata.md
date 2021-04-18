---
description: Imposta i dati della Rep del punto per la mesh.
ms.assetid: 451a1ff0-68fa-48c4-b3f1-d41d7583cb3f
title: 'Metodo ID3DX10Mesh:: SetPointRepData (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.SetPointRepData
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 65114c5411de7932e9cb71166fcf8554fa0bf7b6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323136"
---
# <a name="id3dx10meshsetpointrepdata-method"></a>Metodo ID3DX10Mesh:: SetPointRepData

Imposta i dati della Rep del punto per la mesh.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetPointRepData(
  [in] const UINT *pPointReps
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pPointReps* \[ in\]
</dt> <dd>

Tipo: **const [**uint**](../winprog/windows-data-types.md) \***

Dati della Rep del punto da impostare.

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

 

 

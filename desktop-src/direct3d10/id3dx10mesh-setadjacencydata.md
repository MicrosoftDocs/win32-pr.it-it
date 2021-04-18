---
description: Imposta i dati adiacenza della mesh.
ms.assetid: 67d51ce0-7fe2-484d-9874-f1fa59632d59
title: 'Metodo ID3DX10Mesh:: SetAdjacencyData (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.SetAdjacencyData
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 6fabced002caf424fa1fcbcefcb3b326b0c71f7c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323140"
---
# <a name="id3dx10meshsetadjacencydata-method"></a>Metodo ID3DX10Mesh:: SetAdjacencyData

Imposta i dati adiacenza della mesh.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetAdjacencyData(
  [in] const UINT *pAdjacency
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pAdjacency* \[ in\]
</dt> <dd>

Tipo: **const [**uint**](../winprog/windows-data-types.md) \***

Dati adiacenza da impostare.

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

 

 

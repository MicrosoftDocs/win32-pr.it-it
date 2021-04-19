---
description: Imposta i dati dell'indice della mesh.
ms.assetid: f3e7e166-94b5-45f6-9d43-8d7e32b7b523
title: 'Metodo ID3DX10Mesh:: SetIndexData (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.SetIndexData
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: f561a4109fbab2163b2ec51e95b45a618da5b6d5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323138"
---
# <a name="id3dx10meshsetindexdata-method"></a>Metodo ID3DX10Mesh:: SetIndexData

Imposta i dati dell'indice della mesh.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetIndexData(
  [in] const void *pData,
  [in]       UINT cIndices
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pData* \[ in\]
</dt> <dd>

Tipo: **const \* void**

Dati dell'indice.

</dd> <dt>

*cIndices* \[ in\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Numero di indici in pData.

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

 

 

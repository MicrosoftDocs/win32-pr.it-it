---
description: Accedere alla descrizione del vertice passata a D3DX10CreateMesh. La descrizione del vertice descrive il layout dei buffer dei vertici della mesh.
ms.assetid: e4a4a98a-e131-414c-ad98-21288ff0c61b
title: 'Metodo ID3DX10Mesh:: GetVertexDescription (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.GetVertexDescription
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 01888ea83f43e37951b48e03916f18af1ec6ddb6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103969365"
---
# <a name="id3dx10meshgetvertexdescription-method"></a>Metodo ID3DX10Mesh:: GetVertexDescription

Accedere alla descrizione del vertice passata a [**D3DX10CreateMesh**](d3d10-d3dx10createmesh.md). La descrizione del vertice descrive il layout dei buffer dei vertici della mesh.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetVertexDescription(
  [out] const D3D10_INPUT_ELEMENT_DESC **ppDesc,
  [in]        UINT                     *pDeclCount
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ppDesc* \[ out\]
</dt> <dd>

Tipo: **const [**D3D10 \_ input \_ elemento \_ desc**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_input_element_desc) \* \***

Matrice di elementi di input che descrivono il layout dei buffer dei vertici della mesh. Vedere [**l' \_ elemento di input D3D10 \_ \_ desc**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_input_element_desc).

</dd> <dt>

*pDeclCount* \[ in\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)\***

Numero di elementi di input in ppDesc.

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

 

 

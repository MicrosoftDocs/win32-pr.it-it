---
description: Crea una nuova mesh e la riempie con i dati di una mesh precedentemente caricata.
ms.assetid: 2ce39982-abc0-444b-bc6f-24508f76fe31
title: 'Metodo ID3DX10Mesh:: CloneMesh (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.CloneMesh
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 0f007475ea9f6aeaa6dc0c01bbd721c4a5103adf
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323161"
---
# <a name="id3dx10meshclonemesh-method"></a>Metodo ID3DX10Mesh:: CloneMesh

Crea una nuova mesh e la riempie con i dati di una mesh precedentemente caricata.

## <a name="syntax"></a>Sintassi


```C++
HRESULT CloneMesh(
  [in]        UINT                     Flags,
  [in]        LPCSTR                   pPosSemantic,
  [in]  const D3D10_INPUT_ELEMENT_DESC *pDesc,
  [in]        UINT                     DeclCount,
  [out]       ID3DX10Mesh              **ppCloneMesh
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Flag* \[ in\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Flag di creazione da applicare alla nuova mesh. Vedere [**d3dx10 \_ mesh**](d3dx10-mesh.md).

</dd> <dt>

*pPosSemantic* \[ in\]
</dt> <dd>

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Nome semantico per i dati di posizione.

</dd> <dt>

*pDesc* \[ in\]
</dt> <dd>

Tipo: **const [**D3D10 \_ input \_ elemento \_ desc**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_input_element_desc) \***

Matrice di \_ \_ strutture desc dell'elemento input D3D10, che \_ descrive il formato del vertice per la mesh restituita. Vedere [**l' \_ elemento di input D3D10 \_ \_ desc**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_input_element_desc).

</dd> <dt>

*DeclCount* \[ in\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Numero di elementi nella matrice pDesc.

</dd> <dt>

*ppCloneMesh* \[ out\]
</dt> <dd>

Tipo: **[ **ID3DX10Mesh**](id3dx10mesh.md)\*\***

Nuova mesh.

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

 

 

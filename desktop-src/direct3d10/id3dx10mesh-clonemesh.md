---
description: Crea una nuova mesh e la riempie con i dati di una mesh caricata in precedenza.
ms.assetid: 2ce39982-abc0-444b-bc6f-24508f76fe31
title: Metodo ID3DX10Mesh::CloneMesh (D3DX10.h)
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
ms.openlocfilehash: 292522e47dbaf6937d871209006134e866e92fdeb27f6edba4f4f71f6d1fad14
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119409131"
---
# <a name="id3dx10meshclonemesh-method"></a>Metodo ID3DX10Mesh::CloneMesh

Crea una nuova mesh e la riempie con i dati di una mesh caricata in precedenza.

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

*Flag* \[ Pollici\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Flag di creazione da applicare alla nuova mesh. Vedere [**D3DX10 \_ MESH.**](d3dx10-mesh.md)

</dd> <dt>

*pPosSemantic* \[ Pollici\]
</dt> <dd>

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Nome semantico per i dati della posizione.

</dd> <dt>

*pDesc* \[ Pollici\]
</dt> <dd>

Tipo: **const [**D3D10 \_ INPUT ELEMENT \_ \_ DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_input_element_desc) \***

Matrice di strutture D3D10 \_ INPUT ELEMENT DESC, che descrive il formato dei vertici per la mesh \_ \_ restituita. Vedere [**D3D10 \_ INPUT ELEMENT DESC (ELEMENTO DI INPUT D3D10 \_ \_ DESC).**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_input_element_desc)

</dd> <dt>

*DeclCount* \[ Pollici\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Numero di elementi nella matrice pDesc.

</dd> <dt>

*ppCloneMesh* \[ Cambio\]
</dt> <dd>

Tipo: **[ **ID3DX10Mesh**](id3dx10mesh.md)\*\***

Nuova mesh.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Il valore restituito è uno dei valori elencati in [Codici restituiti Direct3D 10.](d3d10-graphics-reference-returnvalues.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX10.h</dt> </dl>   |
| Libreria<br/> | <dl> <dt>D3DX10.lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DX10Mesh](id3dx10mesh.md)
</dt> <dt>

[Interfacce D3DX](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 

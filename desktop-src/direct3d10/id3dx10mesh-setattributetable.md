---
description: 'Metodo ID3DX10Mesh::SetAttributeTable: imposta la tabella degli attributi per una mesh e il numero di voci archiviate nella tabella.'
ms.assetid: 629fd31b-d88a-4650-82ed-ab7c40690986
title: Metodo ID3DX10Mesh::SetAttributeTable (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.SetAttributeTable
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 6cdaedef52693810519ebb92e6f523afbfe078df68a2a13b7fae7ce0fad98fb1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119634541"
---
# <a name="id3dx10meshsetattributetable-method"></a>Metodo ID3DX10Mesh::SetAttributeTable

Imposta la tabella degli attributi per una mesh e il numero di voci archiviate nella tabella.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetAttributeTable(
  [in] const D3DX10_ATTRIBUTE_RANGE *pAttribTable,
  [in]       UINT                   cAttribTableSize
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pAttribTable* \[ Pollici\]
</dt> <dd>

Tipo: **const [**D3DX10 \_ ATTRIBUTE \_ RANGE**](d3dx10-attribute-range.md) \***

Puntatore a una matrice di strutture ATTRIBUTE RANGE D3DX10, che rappresenta le voci \_ nella tabella degli attributi \_ mesh.

</dd> <dt>

*cAttribTableSize* \[ Pollici\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Numero di attributi nella tabella degli attributi della mesh.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Il valore restituito è uno dei valori elencati in [Codici restituiti Direct3D 10.](d3d10-graphics-reference-returnvalues.md)

## <a name="remarks"></a>Commenti

Se un'applicazione tiene traccia delle informazioni in una tabella di attributi e riorganizza la tabella in seguito a modifiche agli attributi o ai visi, questo metodo consente all'applicazione di aggiornare le tabelle degli attributi anziché chiamare nuovamente ID3DX10Mesh::Optimize.

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

 

 

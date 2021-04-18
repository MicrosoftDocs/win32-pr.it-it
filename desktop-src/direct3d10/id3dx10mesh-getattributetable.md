---
description: Recupera una tabella di attributi per una mesh o il numero di voci archiviate in una tabella di attributi per una mesh.
ms.assetid: cee49eba-c113-49f5-a702-c366401f1f2d
title: 'Metodo ID3DX10Mesh:: GetAttributeTable (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.GetAttributeTable
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 4ff00f3c5d036b3b463bc7c6622de75361b196e6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323150"
---
# <a name="id3dx10meshgetattributetable-method"></a>Metodo ID3DX10Mesh:: GetAttributeTable

Recupera una tabella di attributi per una mesh o il numero di voci archiviate in una tabella di attributi per una mesh.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetAttributeTable(
  [in] D3DX10_ATTRIBUTE_RANGE *pAttribTable,
  [in] UINT                   *pAttribTableSize
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pAttribTable* \[ in\]
</dt> <dd>

Tipo: **[ **\_ \_ intervallo di attributi di d3dx10**](d3dx10-attribute-range.md)\***

Puntatore a una matrice di \_ strutture di intervalli di attributi d3dx10 \_ , che rappresenta le voci nella tabella degli attributi della mesh. Specificare **null** per recuperare il valore per pAttribTableSize.

</dd> <dt>

*pAttribTableSize* \[ in\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)\***

Puntatore al numero di voci archiviate in pAttribTable o a un valore da compilare con il numero di voci archiviate nella tabella degli attributi per la mesh.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Il valore restituito è uno dei valori elencati in [codici restituiti Direct3D 10](d3d10-graphics-reference-returnvalues.md).

## <a name="remarks"></a>Commenti

Una tabella degli attributi viene utilizzata per identificare le aree della mesh che devono essere disegnate con trame, Stati di rendering, materiali e così via. Inoltre, l'applicazione può usare la tabella attribute per nascondere parti di una mesh senza disegnare un identificatore di attributo specificato durante il disegno del frame.

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

 

 

---
description: 'Metodo ID3DX10Mesh::GetAttributeTable: recupera una tabella di attributi per una mesh o il numero di voci archiviate in una tabella di attributi per una mesh.'
ms.assetid: cee49eba-c113-49f5-a702-c366401f1f2d
title: Metodo ID3DX10Mesh::GetAttributeTable (D3DX10.h)
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
ms.openlocfilehash: e7fc503af1a290b27fea81d0c2aba6b84393323b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108083989"
---
# <a name="id3dx10meshgetattributetable-method"></a>Metodo ID3DX10Mesh::GetAttributeTable

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

*pAttribTable* \[ Pollici\]
</dt> <dd>

Tipo: **[ **D3DX10 \_ ATTRIBUTE \_ RANGE**](d3dx10-attribute-range.md)\***

Puntatore a una matrice di strutture ATTRIBUTE RANGE D3DX10, che rappresenta le voci \_ nella tabella degli attributi della \_ mesh. Specificare **NULL** per recuperare il valore per pAttribTableSize.

</dd> <dt>

*pAttribTableSize* \[ Pollici\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)\***

Puntatore al numero di voci archiviate in pAttribTable o a un valore da riempire con il numero di voci archiviate nella tabella degli attributi per la mesh.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Il valore restituito è uno dei valori elencati in [Codici restituiti Direct3D 10.](d3d10-graphics-reference-returnvalues.md)

## <a name="remarks"></a>Commenti

Una tabella di attributi viene usata per identificare le aree della mesh che devono essere disegnate con trame, stati di rendering, materiali e così via diversi. Inoltre, l'applicazione può usare la tabella degli attributi per nascondere parti di una mesh non disegnando un identificatore di attributo specificato durante il disegno del frame.

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

 

 

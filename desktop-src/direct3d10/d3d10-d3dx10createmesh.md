---
description: 'Funzione D3DX10CreateMesh: crea un oggetto mesh usando un dichiaratore.'
ms.assetid: 50e09378-2935-4b18-8fc9-5e58eaadae44
title: Funzione D3DX10CreateMesh (D3DX10Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateMesh
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: a4f044d3337a2da05eb78b027492b870f450e4309c94faa8c72db935437511dd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119853481"
---
# <a name="d3dx10createmesh-function"></a>Funzione D3DX10CreateMesh

Crea un oggetto mesh usando un dichiaratore.

## <a name="syntax"></a>Sintassi


```C++
HRESULT D3DX10CreateMesh(
  _In_        ID3D10Device             *pDevice,
  _In_  const D3D10_INPUT_ELEMENT_DESC *pDeclaration,
  _In_        UINT                     DeclCount,
  _In_        LPCSTR                   pPositionSemantic,
  _In_        UINT                     VertexCount,
  _In_        UINT                     FaceCount,
  _In_        UINT                     Options,
  _Out_       ID3DX10Mesh              **ppMesh
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pDevice* \[ Pollici\]
</dt> <dd>

Tipo: **[ **ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***

Puntatore a [**un'interfaccia ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device), l'oggetto dispositivo da associare alla mesh.

</dd> <dt>

*pDeclaration* \[ Pollici\]
</dt> <dd>

Tipo: **const [**D3D10 \_ INPUT ELEMENT \_ \_ DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_input_element_desc) \***

Matrice di [**elementi \_ \_ DESC DELL'ELEMENTO INPUT D3D10 \_**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_input_element_desc) che descrivono il formato dei vertici per la mesh restituita. Questo parametro deve essere mappato direttamente a un formato di vertice flessibile (FVF).

</dd> <dt>

*DeclCount* \[ Pollici\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Numero di elementi in pDeclaration.

</dd> <dt>

*pPositionSemantic* \[ Pollici\]
</dt> <dd>

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Semantica che identifica la parte della dichiarazione del vertice che contiene informazioni sulla posizione.

</dd> <dt>

*VertexCount* \[ Pollici\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Numero di vertici per la mesh. Questo parametro deve essere maggiore di 0.

</dd> <dt>

*FaceCount* \[ Pollici\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Numero di visi per la mesh. L'intervallo valido per questo numero è maggiore di 0 e uno minore del valore DWORD massimo (in genere 65534), perché l'ultimo indice è riservato.

</dd> <dt>

*Opzioni* \[ Pollici\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Combinazione di uno o più flag da [**D3DX10 \_ MESH,**](d3dx10-mesh.md)specificando le opzioni per la mesh.

</dd> <dt>

*ppMesh* \[ Cambio\]
</dt> <dd>

Tipo: **[ **ID3DX10Mesh**](id3dx10mesh.md)\*\***

Indirizzo di un puntatore a [**un'interfaccia ID3DX10Mesh**](id3dx10mesh.md)che rappresenta l'oggetto mesh creato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se la funzione ha esito positivo, il valore restituito è D3D \_ OK. Se la funzione ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX10Mesh.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3DX10.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni mesh](d3d10-graphics-reference-d3dx10-functions-mesh.md)
</dt> <dt>

[Funzioni D3DX](d3d10-graphics-reference-d3dx10-functions.md)
</dt> </dl>

 

 

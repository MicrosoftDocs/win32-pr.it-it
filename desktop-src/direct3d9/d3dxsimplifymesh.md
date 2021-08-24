---
description: Genera una mesh semplificata usando i pesi specificati che si avvicinano il più possibile al valore MinValue specificato.
ms.assetid: 589356a9-f272-4851-92ae-54dbecc0b234
title: Funzione D3DXSimplifyMesh (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSimplifyMesh
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 3cc0bfe18afef7b91dbdf887500b485a446b154cb5775cbf950a7e712a332a9f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119749781"
---
# <a name="d3dxsimplifymesh-function"></a>Funzione D3DXSimplifyMesh

Genera una mesh semplificata usando i pesi specificati che si avvicinano il più possibile al valore MinValue specificato.

## <a name="syntax"></a>Sintassi


```C++
HRESULT D3DXSimplifyMesh(
  _In_        LPD3DXMESH           pMesh,
  _In_  const DWORD                *pAdjacency,
  _In_  const D3DXATTRIBUTEWEIGHTS *pVertexAttributeWeights,
  _In_  const FLOAT                *pVertexWeights,
  _In_        DWORD                MinValue,
  _In_        DWORD                Options,
  _Out_       LPD3DXMESH           *ppMesh
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pMesh* \[ Pollici\]
</dt> <dd>

Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)**

Puntatore a [**un'interfaccia ID3DXMesh,**](id3dxmesh.md) che rappresenta la mesh di origine.

</dd> <dt>

*pAdjacency* \[ Pollici\]
</dt> <dd>

Tipo: **const [**DWORD**](../winprog/windows-data-types.md) \***

Puntatore a una matrice di tre DWORD per viso che specificano i tre elementi adiacenti per ogni viso nella mesh da semplificare.

</dd> <dt>

*pVertexAttributeWeights* \[ Pollici\]
</dt> <dd>

Tipo: **const [**D3DXATTRIBUTEWEIGHTS**](d3dxattributeweights.md) \***

Puntatore a [**una struttura D3DXATTRIBUTEWEIGHTS,**](d3dxattributeweights.md) contenente il peso per ogni componente vertice. Se questo parametro è impostato su **NULL,** viene usata una struttura predefinita. Vedere la sezione Osservazioni.

</dd> <dt>

*pVertexWeights* \[ Pollici\]
</dt> <dd>

Tipo: **const [**FLOAT**](../winprog/windows-data-types.md) \***

Puntatore a una matrice di pesi dei vertici. Se questo parametro è impostato su **NULL,** tutti i pesi dei vertici vengono impostati su 1,0.

</dd> <dt>

*MinValue* \[ Pollici\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Numero di vertici o visi, a seconda del flag impostato nel parametro *Options,* in base al quale semplificare la mesh di origine.

</dd> <dt>

*Opzioni* \[ Pollici\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Specifica le opzioni di semplificazione per la mesh. È possibile impostare uno dei flag in [**D3DXMESHSIMP.**](./d3dxmeshsimp.md)

</dd> <dt>

*ppMesh* \[ Cambio\]
</dt> <dd>

Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)\***

Indirizzo di un puntatore a [**un'interfaccia ID3DXMesh,**](id3dxmesh.md) che rappresenta la mesh di semplificazione restituita.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se la funzione ha esito positivo, il valore restituito è D3D \_ OK. Se la funzione ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Commenti

Questa funzione genera una mesh con vertici o visi *MinValue.*

Se il processo di semplificazione non è in grado di ridurre la mesh a *MinValue,* la chiamata ha comunque esito positivo perché *MinValue* è un valore minimo desiderato, non un minimo assoluto.

Se *pVertexAttributeWeights* è impostato su **NULL,** alla struttura [**D3DXATTRIBUTEWEIGHTS**](d3dxattributeweights.md) predefinita vengono assegnati i valori seguenti.


```
D3DXATTRIBUTEWEIGHTS AttributeWeights;
    
AttributeWeights.Position  = 1.0;
AttributeWeights.Boundary =  1.0;
AttributeWeights.Normal   =  1.0;
AttributeWeights.Diffuse  =  0.0;
AttributeWeights.Specular =  0.0;
AttributeWeights.Tex[8]   =  {0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0};
```



Questa struttura predefinita è quella che la maggior parte delle applicazioni deve usare perché considera solo la regolazione geometrica e normale. Solo in casi speciali sarà necessario modificare gli altri campi membro.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni mesh](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 

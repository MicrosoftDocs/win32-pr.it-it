---
description: Usa un sistema di coordinate a sinistra per creare una mesh contenente un toro.
ms.assetid: 68df7650-8a87-4762-8b57-5704c419b0d7
title: Funzione D3DXCreateTorus (D3dx9shape. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateTorus
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 384950ca1f00d0115135cf9ae36a2883ec5470e7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104235024"
---
# <a name="d3dxcreatetorus-function"></a>D3DXCreateTorus (funzione)

Usa un sistema di coordinate a sinistra per creare una mesh contenente un toro.

## <a name="syntax"></a>Sintassi


```C++
HRESULT D3DXCreateTorus(
  _In_  LPDIRECT3DDEVICE9 pDevice,
  _In_  FLOAT             InnerRadius,
  _In_  FLOAT             OuterRadius,
  _In_  UINT              Sides,
  _In_  UINT              Rings,
  _Out_ LPD3DXMESH        *ppMesh,
  _Out_ LPD3DXBUFFER      *ppAdjacency
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*PDEVICE* \[ in\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Puntatore a un'interfaccia [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , che rappresenta il dispositivo associato alla mesh Torus creata.

</dd> <dt>

*InnerRadius* \[ in\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

Raggio interno di torus. Il valore deve essere maggiore o uguale a 0,0 f.

</dd> <dt>

*OuterRadius* \[ in\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

Raggio esterno dei Toru. Il valore deve essere maggiore o uguale a 0,0 f.

</dd> <dt>

*Lati* \[ in\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Numero di lati in una sezione incrociata. Il valore deve essere maggiore o uguale a 3.

</dd> <dt>

*Anelli* \[ in\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Numero di anelli che compongono il toro. Il valore deve essere maggiore o uguale a 3.

</dd> <dt>

*ppMesh* \[ out\]
</dt> <dd>

Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)\***

Indirizzo di un puntatore alla forma di output, un'interfaccia [**ID3DXMesh**](id3dxmesh.md) .

</dd> <dt>

*ppAdjacency* \[ out\]
</dt> <dd>

Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Indirizzo di un puntatore a un'interfaccia [**ID3DXBuffer**](id3dxbuffer.md) . Quando il metodo restituisce un risultato, questo parametro viene riempito con una matrice di tre DWORD per ogni volto che specifica i tre elementi adiacenti per ogni viso nella mesh. È possibile specificare **null** .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se la funzione ha esito positivo, il valore restituito è D3D \_ OK. Se la funzione ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OutOfMemory.

## <a name="remarks"></a>Commenti

I Torus creati sono centrati sull'origine e il relativo asse è allineato all'asse z. Il raggio interno del Toro è il raggio della sezione incrociata (raggio secondario) e il raggio esterno del Toro è il raggio del foro centrale.

Questa funzione restituisce una mesh che può essere usata in un secondo momento per il disegno o la manipolazione da parte dell'applicazione.

Questa funzione crea una mesh con l' \_ opzione di creazione gestita D3DXMESH e [D3DFVF \_ xyz \| D3DFVF \_ Normal](d3dfvf.md) Flexible Vertex Format (FVF).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9shape. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>    |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni di disegno di forme](dx9-graphics-reference-d3dx-functions-shape.md)
</dt> </dl>

 

 

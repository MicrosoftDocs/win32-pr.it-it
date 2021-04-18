---
description: Usa un sistema di coordinate a sinistra per creare una riga.
ms.assetid: 0d2ef331-9edf-4b0a-ace4-ecb8bb2f7352
title: Funzione D3DXCreateLine (D3dx9core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateLine
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5cf7d75ca63d64be39733b36a1b7d7a1b464238e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322447"
---
# <a name="d3dxcreateline-function"></a>D3DXCreateLine (funzione)

Usa un sistema di coordinate a sinistra per creare una riga.

## <a name="syntax"></a>Sintassi


```C++
HRESULT D3DXCreateLine(
  _In_  LPDIRECT3DDEVICE9 pDevice,
  _Out_ LPD3DXLINE        *ppLine
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*PDEVICE* \[ in\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Puntatore a un'interfaccia [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , che rappresenta il dispositivo associato alla Mesh Box creata.

</dd> <dt>

*ppLine* \[ out\]
</dt> <dd>

Tipo: **[ **LPD3DXLINE**](id3dxline.md)\***

Puntatore a un'interfaccia [**ID3DXLine**](id3dxline.md) .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se la funzione ha esito positivo, il valore restituito è D3D \_ OK. Se la funzione ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OutOfMemory.

## <a name="remarks"></a>Commenti

Questa funzione crea una mesh con l' \_ opzione di creazione gestita D3DXMESH e [D3DFVF \_ xyz \| D3DFVF \_ Normal](d3dfvf.md) Flexible Vertex Format (FVF).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9core. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni per utilizzo generico](dx9-graphics-reference-d3dx-functions-general-purpose.md)
</dt> </dl>

 

 

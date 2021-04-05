---
description: Crea una mappa dell'ambiente di rendering.
ms.assetid: 5ca10602-5ab1-4766-a350-706c46c55df2
title: Funzione D3DXCreateRenderToEnvMap (D3dx9core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateRenderToEnvMap
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 6829d53f53bd6a4783f5873eeed614e48bbe1088
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104058608"
---
# <a name="d3dxcreaterendertoenvmap-function"></a>D3DXCreateRenderToEnvMap (funzione)

Crea una mappa dell'ambiente di rendering.

## <a name="syntax"></a>Sintassi


```C++
HRESULT D3DXCreateRenderToEnvMap(
  _In_  LPDIRECT3DDEVICE9    pDevice,
  _In_  UINT                 Size,
  _In_  UINT                 MipLevels,
  _In_  D3DFORMAT            Format,
  _In_  BOOL                 DepthStencil,
  _In_  D3DFORMAT            DepthStencilFormat,
  _Out_ LPD3DXRENDERTOENVMAP *ppRenderToEnvMap
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*PDEVICE* \[ in\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Puntatore a un'interfaccia [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , che è il dispositivo da associare alla superficie di rendering.

</dd> <dt>

*Dimensioni* \[ in\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Dimensione della superficie di rendering.

</dd> <dt>

*MipLevels* \[ in\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Il numero di livelli di mipmap.

</dd> <dt>

*Formato* \[ in\]
</dt> <dd>

Tipo: **[D3DFORMAT](d3dformat.md)**

Membro del tipo enumerato [D3DFORMAT](d3dformat.md) che descrive il formato pixel della mappa dell'ambiente.

</dd> <dt>

*DepthStencil* \[ in\]
</dt> <dd>

Tipo: **[ **bool**](../winprog/windows-data-types.md)**

Se **true**, l'area di rendering supporta una superficie di stencil di profondità. In caso contrario, questo membro è impostato su **false**.

</dd> <dt>

*DepthStencilFormat* \[ in\]
</dt> <dd>

Tipo: **[D3DFORMAT](d3dformat.md)**

Se DepthStencil è impostato su **true**, questo parametro è un membro del tipo enumerato [D3DFORMAT](d3dformat.md) che descrive il formato di stencil depth della mappa dell'ambiente.

</dd> <dt>

*ppRenderToEnvMap* \[ out\]
</dt> <dd>

Tipo: **[ **LPD3DXRENDERTOENVMAP**](id3dxrendertoenvmap.md)\***

Indirizzo di un puntatore a un'interfaccia [**ID3DXRenderToEnvMap**](id3dxrendertoenvmap.md) che rappresenta la mappa dell'ambiente di rendering creata.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se la funzione ha esito positivo, il valore restituito è D3D \_ OK. Se la funzione ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, E \_ OutOfMemory.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9core. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni per utilizzo generico](dx9-graphics-reference-d3dx-functions-general-purpose.md)
</dt> </dl>

 

 

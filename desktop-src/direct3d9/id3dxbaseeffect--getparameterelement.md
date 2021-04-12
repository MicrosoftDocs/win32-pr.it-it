---
description: Ottiene l'handle di un parametro dell'elemento della matrice.
ms.assetid: fe8edbc5-dc1d-4386-8149-489541d55bde
title: 'Metodo ID3DXBaseEffect:: getparameterelement (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetParameterElement
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 5130ccf57634f9b1a569a1dd70833fe2014e1a74
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355874"
---
# <a name="id3dxbaseeffectgetparameterelement-method"></a>Metodo ID3DXBaseEffect:: getparameterelement

Ottiene l'handle di un parametro dell'elemento della matrice.

## <a name="syntax"></a>Sintassi


```C++
D3DXHANDLE GetParameterElement(
  [in] D3DXHANDLE hParameter,
  [in] UINT       ElementIndex
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hParameter* \[ in\]
</dt> <dd>

Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Handle della matrice. Vedere [handle (Direct3D 9)](handles.md).

</dd> <dt>

*ElementIndex* \[ in\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Indice dell'elemento della matrice.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Restituisce l'handle del parametro specificato oppure **null** se HParameter o ElementIndex non è valido. Vedere [handle (Direct3D 9)](handles.md).

## <a name="remarks"></a>Commenti

Questo metodo viene usato per ottenere un elemento di un parametro che è una matrice.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Shader. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXBaseEffect](id3dxbaseeffect.md)
</dt> </dl>

 

 

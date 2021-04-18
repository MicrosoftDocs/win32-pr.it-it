---
description: Ottiene l'handle di un passaggio.
ms.assetid: 71332f6a-18fe-4702-8620-6d16b835ba8f
title: 'Metodo ID3DXBaseEffect:: GETPASS (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetPass
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 5db5c5da16a65b53b6e266886ee6ab8472dc3246
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104402024"
---
# <a name="id3dxbaseeffectgetpass-method"></a>Metodo ID3DXBaseEffect:: GETPASS

Ottiene l'handle di un passaggio.

## <a name="syntax"></a>Sintassi


```C++
D3DXHANDLE GetPass(
  [in] D3DXHANDLE hTechnique,
  [in] UINT       Index
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hTechnique* \[ in\]
</dt> <dd>

Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Handle della tecnica padre. Vedere [handle (Direct3D 9)](handles.md).

</dd> <dt>

*Indice* \[ di in\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Indice per il passaggio.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Restituisce l'handle del passaggio specificato all'interno della tecnica specificata o **null** se l'indice non è valido. Vedere [handle (Direct3D 9)](handles.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Effect. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXBaseEffect](id3dxbaseeffect.md)
</dt> </dl>

 

 

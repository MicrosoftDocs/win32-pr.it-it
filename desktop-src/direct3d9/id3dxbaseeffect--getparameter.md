---
description: Ottiene l'handle di un parametro di primo livello o di un parametro del membro della struttura.
ms.assetid: 940f1bfd-ce62-4c86-88cc-787e62cf6a93
title: 'Metodo ID3DXBaseEffect:: GetParameter (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetParameter
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: b7c96c371b36b8dcfc2e3e64a95798347ca3a6ea
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104058688"
---
# <a name="id3dxbaseeffectgetparameter-method"></a>Metodo ID3DXBaseEffect:: GetParameter

Ottiene l'handle di un parametro di primo livello o di un parametro del membro della struttura.

## <a name="syntax"></a>Sintassi


```C++
D3DXHANDLE GetParameter(
  [in] D3DXHANDLE hParameter,
  [in] UINT       Index
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hParameter* \[ in\]
</dt> <dd>

Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Handle del parametro o **null** per i parametri di primo livello. Vedere [handle (Direct3D 9)](handles.md).

</dd> <dt>

*Indice* \[ di in\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Indice di parametro.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Restituisce l'handle del parametro specificato o **null** se l'indice non è valido. Vedere [handle (Direct3D 9)](handles.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Shader. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXBaseEffect](id3dxbaseeffect.md)
</dt> </dl>

 

 

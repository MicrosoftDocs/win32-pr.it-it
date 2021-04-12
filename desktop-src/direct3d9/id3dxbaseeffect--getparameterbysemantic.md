---
description: Ottiene l'handle di un parametro di primo livello o di un parametro del membro della struttura cercando la relativa semantica con una ricerca senza distinzione tra maiuscole e minuscole.
ms.assetid: 3de3791a-fe09-4a39-bd6f-0e20a641dd32
title: 'Metodo ID3DXBaseEffect:: GetParameterBySemantic (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetParameterBySemantic
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: c70d30d68d73d6c4dd33d483747be4293a255693
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355879"
---
# <a name="id3dxbaseeffectgetparameterbysemantic-method"></a>Metodo ID3DXBaseEffect:: GetParameterBySemantic

Ottiene l'handle di un parametro di primo livello o di un parametro del membro della struttura cercando la relativa semantica con una ricerca senza distinzione tra maiuscole e minuscole.

## <a name="syntax"></a>Sintassi


```C++
D3DXHANDLE GetParameterBySemantic(
  [in] D3DXHANDLE hParameter,
  [in] LPCSTR     pSemantic
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hParameter* \[ in\]
</dt> <dd>

Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Handle del parametro o **null** per i parametri di primo livello. Vedere [handle (Direct3D 9)](handles.md).

</dd> <dt>

*pSemantic* \[ in\]
</dt> <dd>

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Stringa contenente il nome semantico.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Restituisce l'handle del primo parametro che corrisponde alla semantica specificata o **null** se la semantica non è stata trovata. Vedere [handle (Direct3D 9)](handles.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Shader. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXBaseEffect](id3dxbaseeffect.md)
</dt> </dl>

 

 

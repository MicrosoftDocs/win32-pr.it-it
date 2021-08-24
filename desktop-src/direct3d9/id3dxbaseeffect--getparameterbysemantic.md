---
description: Ottiene l'handle di un parametro di primo livello o di un parametro del membro della struttura cercandone la semantica con una ricerca senza distinzione tra maiuscole e minuscole.
ms.assetid: 3de3791a-fe09-4a39-bd6f-0e20a641dd32
title: Metodo ID3DXBaseEffect::GetParameterBySemantic (D3DX9Shader.h)
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
ms.openlocfilehash: fa00ef4585462f068e95fcefca8332acd46930efaf1bb1c108a471511ab63eb4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119791011"
---
# <a name="id3dxbaseeffectgetparameterbysemantic-method"></a>Metodo ID3DXBaseEffect::GetParameterBySemantic

Ottiene l'handle di un parametro di primo livello o di un parametro del membro della struttura cercandone la semantica con una ricerca senza distinzione tra maiuscole e minuscole.

## <a name="syntax"></a>Sintassi


```C++
D3DXHANDLE GetParameterBySemantic(
  [in] D3DXHANDLE hParameter,
  [in] LPCSTR     pSemantic
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hParameter* \[ Pollici\]
</dt> <dd>

Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Handle del parametro o **NULL per i** parametri di primo livello. Vedere [Handle (Direct3D 9).](handles.md)

</dd> <dt>

*pSemantic* \[ Pollici\]
</dt> <dd>

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Stringa contenente il nome semantico.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Restituisce l'handle del primo parametro che corrisponde alla semantica specificata oppure **NULL se** la semantica non è stata trovata. Vedere [Handle (Direct3D 9).](handles.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Shader.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXBaseEffect](id3dxbaseeffect.md)
</dt> </dl>

 

 

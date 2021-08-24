---
description: Ottiene l'handle di un'annotazione cercandone il nome.
ms.assetid: da4e2805-5f06-4a9b-836f-85a8c154c502
title: Metodo ID3DXBaseEffect::GetAnnotationByName (D3DX9Effect.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetAnnotationByName
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: a4a8943248ef2280bdb58c864a44c67a44a12c6f641fc05b74bb0fb28e2e9ba1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119791061"
---
# <a name="id3dxbaseeffectgetannotationbyname-method"></a>Metodo ID3DXBaseEffect::GetAnnotationByName

Ottiene l'handle di un'annotazione cercandone il nome.

## <a name="syntax"></a>Sintassi


```C++
D3DXHANDLE GetAnnotationByName(
  [in] D3DXHANDLE hObject,
  [in] LPCSTR     pName
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hObject* \[ Pollici\]
</dt> <dd>

Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Handle di una tecnica, di un passaggio o di un parametro di primo livello. Vedere [Handle (Direct3D 9)](handles.md).

</dd> <dt>

*pName* \[ Pollici\]
</dt> <dd>

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Stringa contenente il nome dell'annotazione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Restituisce l'handle dell'annotazione specificata oppure **NULL** se il nome non è stato trovato. Vedere [Handle (Direct3D 9)](handles.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Effect.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXBaseEffect](id3dxbaseeffect.md)
</dt> </dl>

 

 

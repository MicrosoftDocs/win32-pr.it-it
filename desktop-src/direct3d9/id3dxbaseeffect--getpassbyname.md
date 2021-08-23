---
description: Ottiene l'handle di un passaggio cercandone il nome.
ms.assetid: 24d043a2-5c87-4a59-80d4-0c81bd7a0b3e
title: Metodo ID3DXBaseEffect::GetPassByName (D3DX9Effect.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetPassByName
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 5837d2b69c793f788c4c89f648402e7924bc2f3af9a92bbbe596c133efe10d1e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118987761"
---
# <a name="id3dxbaseeffectgetpassbyname-method"></a>Metodo ID3DXBaseEffect::GetPassByName

Ottiene l'handle di un passaggio cercandone il nome.

## <a name="syntax"></a>Sintassi


```C++
D3DXHANDLE GetPassByName(
  [in] D3DXHANDLE hTechnique,
  [in] LPCSTR     pName
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hTechnique* \[ Pollici\]
</dt> <dd>

Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Handle della tecnica padre. Vedere [Handle (Direct3D 9).](handles.md)

</dd> <dt>

*pName* \[ Pollici\]
</dt> <dd>

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Stringa contenente il nome del passaggio.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Restituisce l'handle del primo passaggio all'interno della tecnica specificata con il nome specificato oppure **NULL** se il nome non è stato trovato. Vedere [Handle (Direct3D 9).](handles.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Effect.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXBaseEffect](id3dxbaseeffect.md)
</dt> </dl>

 

 

---
description: Ottiene l'handle di una tecnica.
ms.assetid: da139706-734b-4d5e-896d-52f045942218
title: Metodo ID3DXBaseEffect::GetTechnique (D3DX9Shader.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetTechnique
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 6d193e08bf40ac67ba46218e9ce3e11b510d7014239a09b1c1b0000be5ec9420
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118987741"
---
# <a name="id3dxbaseeffectgettechnique-method"></a>Metodo ID3DXBaseEffect::GetTechnique

Ottiene l'handle di una tecnica.

## <a name="syntax"></a>Sintassi


```C++
D3DXHANDLE GetTechnique(
  [in] UINT Index
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Indice* \[ Pollici\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Indice delle tecniche.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Restituisce l'handle della tecnica specificata oppure **NULL se** l'indice non è valido. Vedere [Handle (Direct3D 9).](handles.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Shader.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXBaseEffect](id3dxbaseeffect.md)
</dt> </dl>

 

 

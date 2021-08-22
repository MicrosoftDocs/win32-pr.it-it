---
description: Arrestare l'acquisizione delle modifiche dello stato dei parametri dell'effetto.
ms.assetid: b6ca2917-2df0-4f3a-9ee3-23e9d2501ff4
title: Metodo ID3DXEffect::EndParameterBlock (D3DX9Effect.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.EndParameterBlock
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: b1d68aa1bd716ee106a5d1588a7a7060adb851185115e97d2f5f2a5d7f857c02
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119494231"
---
# <a name="id3dxeffectendparameterblock-method"></a>Metodo ID3DXEffect::EndParameterBlock

Arrestare l'acquisizione delle modifiche dello stato dei parametri dell'effetto.

## <a name="syntax"></a>Sintassi


```C++
D3DXHANDLE EndParameterBlock();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Restituisce un handle per il blocco di stato del parametro.

## <a name="remarks"></a>Commenti

Tutti i parametri dell'effetto che cambiano stato (dopo aver chiamato BeginParameterBlock e prima di chiamare EndParameterBlock) verranno salvati in un blocco di stato del parametro dell'effetto. Usare ApplyParameterBlock per applicare questo blocco di modifiche di stato al sistema degli effetti. Al termine di un blocco di stato, usare DeleteParameterBlock per liberare la memoria.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Effect.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXEffect](id3dxeffect.md)
</dt> <dt>

[**ID3DXEffect::BeginParameterBlock**](id3dxeffect--beginparameterblock.md)
</dt> <dt>

[**ID3DXEffect::ApplyParameterBlock**](id3dxeffect--applyparameterblock.md)
</dt> <dt>

[**ID3DXEffect::D eleteParameterBlock**](id3dxeffect--deleteparameterblock.md)
</dt> </dl>

 

 





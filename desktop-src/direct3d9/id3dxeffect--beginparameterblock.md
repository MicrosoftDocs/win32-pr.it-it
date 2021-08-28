---
description: Avviare l'acquisizione delle modifiche dello stato in un blocco di parametri.
ms.assetid: cdf6f572-1a21-4c1d-a113-13b48bacd060
title: Metodo ID3DXEffect::BeginParameterBlock (D3DX9Effect.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.BeginParameterBlock
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: b7345a045d152d5637b656bf4e9090b9645baf33645905e5e956737a1e6ede30
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119494281"
---
# <a name="id3dxeffectbeginparameterblock-method"></a>Metodo ID3DXEffect::BeginParameterBlock

Avviare l'acquisizione delle modifiche dello stato in un blocco di parametri.

## <a name="syntax"></a>Sintassi


```C++
HRESULT BeginParameterBlock();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è D3D \_ OK. Se il metodo ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.

## <a name="remarks"></a>Commenti

Acquisisci modifiche dello stato del parametro dell'effetto fino a quando non viene chiamato EndParameterBlock. I parametri dell'effetto includono qualsiasi modifica dello stato all'esterno di un passaggio. Eliminare i blocchi di parametri se non sono più necessari chiamando DeleteParameterBlock.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Effect.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXEffect](id3dxeffect.md)
</dt> <dt>

[**ID3DXEffect::EndParameterBlock**](id3dxeffect--endparameterblock.md)
</dt> <dt>

[**ID3DXEffect::ApplyParameterBlock**](id3dxeffect--applyparameterblock.md)
</dt> <dt>

[**ID3DXEffect::D eleteParameterBlock**](id3dxeffect--deleteparameterblock.md)
</dt> </dl>

 

 





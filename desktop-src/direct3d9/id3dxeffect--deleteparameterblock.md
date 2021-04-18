---
description: Elimina un blocco di parametri.
ms.assetid: 5502dabc-1703-481b-a69d-f6bd8fd01d20
title: Metodo ID3DXEffect::D eleteParameterBlock (D3DX9Effect. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.DeleteParameterBlock
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 483b09ebf308b8cdfa14d714bc74786e5fcb1f83
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322789"
---
# <a name="id3dxeffectdeleteparameterblock-method"></a>ID3DXEffect::D Metodo eleteParameterBlock

Elimina un blocco di parametri.

## <a name="syntax"></a>Sintassi


```C++
HRESULT DeleteParameterBlock(
  [in] D3DXHANDLE  hParameterBlock
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

 *hParameterBlock* \[ in\]
</dt> <dd>

Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Handle per il blocco di parametri. Si tratta dell'handle restituito da [**ID3DXEffect:: EndParameterBlock**](id3dxeffect--endparameterblock.md).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è D3D \_ OK. Se il metodo ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.

## <a name="remarks"></a>Commenti

I blocchi di parametri sono blocchi di Stati effettivi. Usare un blocco di parametri per registrare le modifiche di stato in modo che possano essere applicate in un secondo momento con una singola chiamata API. Quando non è più necessario, eliminare il blocco di parametri per ridurre l'utilizzo della memoria.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Effect. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXEffect](id3dxeffect.md)
</dt> <dt>

[**ID3DXEffect::BeginParameterBlock**](id3dxeffect--beginparameterblock.md)
</dt> <dt>

[**ID3DXEffect::EndParameterBlock**](id3dxeffect--endparameterblock.md)
</dt> </dl>

 

 





---
description: Applicare i valori in un blocco di stato allo stato corrente del sistema degli effetti.
ms.assetid: f228e2a2-64fa-4354-9f49-42d1d3b12d50
title: Metodo ID3DXEffect::ApplyParameterBlock (D3DX9Effect.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.ApplyParameterBlock
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 8f5a382823da73df68ec0c32e120c0e94a2a7deba86e6aac4afe01e4e46acd7a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119951801"
---
# <a name="id3dxeffectapplyparameterblock-method"></a>Metodo ID3DXEffect::ApplyParameterBlock

Applicare i valori in un blocco di stato allo stato corrente del sistema degli effetti.

## <a name="syntax"></a>Sintassi


```C++
HRESULT ApplyParameterBlock(
  [in] D3DXHANDLE  hParameterBlock
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

 *hParameterBlock* \[ Pollici\]
</dt> <dd>

Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Handle per il blocco di parametri. Si tratta dell'handle restituito da [**ID3DXEffect::EndParameterBlock**](id3dxeffect--endparameterblock.md).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è D3D \_ OK. Se il metodo ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.

## <a name="remarks"></a>Commenti

Acquisire le modifiche dello stato dei parametri dell'effetto in un blocco di parametri chiamando BeginParameterBlock; arrestare l'acquisizione delle modifiche di stato chiamando EndParameterBlock. Queste modifiche di stato includono eventuali modifiche dei parametri di effetto che si verificano all'interno di una tecnica (incluse quelle all'esterno di un passaggio). Al termine dell'operazione con il blocco di parametri, chiamare DeleteParameterBlock per recuperare la memoria.

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

[**ID3DXEffect::EndParameterBlock**](id3dxeffect--endparameterblock.md)
</dt> <dt>

[**ID3DXEffect::D eleteParameterBlock**](id3dxeffect--deleteparameterblock.md)
</dt> </dl>

 

 





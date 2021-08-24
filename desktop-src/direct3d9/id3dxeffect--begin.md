---
description: Avvia una tecnica attiva.
ms.assetid: 6598d77b-8b53-4f2d-aa43-adf358ad486d
title: Metodo ID3DXEffect::Begin (D3DX9Effect.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.Begin
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 4f4e41830b0bb4507e3969c327c84a85c5336e5f07389fa12e05f3a92f4089a4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119675461"
---
# <a name="id3dxeffectbegin-method"></a>Metodo ID3DXEffect::Begin

Avvia una tecnica attiva.

## <a name="syntax"></a>Sintassi


```C++
HRESULT Begin(
  [out] UINT  *pPasses,
  [in]  DWORD Flags
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pPasses* \[ Cambio\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)\***

Puntatore a un valore restituito che indica il numero di passaggi necessari per eseguire il rendering della tecnica corrente.

</dd> <dt>

*Flag* \[ Pollici\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Valore DWORD che determina se lo stato modificato da un effetto viene salvato e ripristinato. Il valore predefinito 0 specifica che **ID3DXEffect::Begin** e [**ID3DXEffect::End**](id3dxeffect--end.md) salvano e ripristinano tutto lo stato modificato dall'effetto (incluse le costanti pixel e vertex shader). I flag validi sono visibili in Flag di salvataggio e ripristino dello [stato dell'effetto.](d3dxfx.md)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è D3D \_ OK. Se il metodo ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.

## <a name="remarks"></a>Commenti

Un'applicazione imposta una tecnica attiva nel sistema di effetti chiamando **ID3DXEffect::Begin**. Il sistema degli effetti risponde acquisendo tutto lo stato della pipeline che può essere modificato dalla tecnica in un blocco di stato. Un'applicazione segnala la fine di una tecnica chiamando [**ID3DXEffect::End,**](id3dxeffect--end.md)che usa il blocco di stato per ripristinare lo stato originale. Il sistema di effetti, pertanto, si occupa del salvataggio dello stato quando una tecnica diventa attiva e del ripristino dello stato al termine di una tecnica. Se si sceglie di disabilitare questa funzionalità di salvataggio e ripristino, vedere [D3DXFX \_ DONOTSAVESAMPLERSTATE.](d3dxfx.md)

All'interno della coppia **ID3DXEffect::Begin** e [**ID3DXEffect::End,**](id3dxeffect--end.md) un'applicazione usa [**ID3DXEffect::BeginPass**](id3dxeffect--beginpass.md) per impostare il passaggio attivo, [**ID3DXEffect::CommitChanges**](id3dxeffect--commitchanges.md) se si sono verificate modifiche di stato dopo l'attivazione del passaggio e [**ID3DXEffect::EndPass**](id3dxeffect--endpass.md) per terminare il passaggio attivo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Effect.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXEffect](id3dxeffect.md)
</dt> </dl>

 

 

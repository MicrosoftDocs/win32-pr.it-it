---
description: Avvia un passaggio, all'interno della tecnica attiva.
ms.assetid: fbb2bf1c-e37a-4117-8c3c-5f5b6a267301
title: Metodo ID3DXEffect::BeginPass (D3DX9Effect.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.BeginPass
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 9013a67c2d4e0e9760167bc979ac05edd4879c5414ce5c9b9c55528baf3f6a18
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118987547"
---
# <a name="id3dxeffectbeginpass-method"></a>Metodo ID3DXEffect::BeginPass

Avvia un passaggio, all'interno della tecnica attiva.

## <a name="syntax"></a>Sintassi


```C++
HRESULT BeginPass(
  [in] UINT Pass
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Passaggio* \[ Pollici\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Indice integer in base zero nella tecnica.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è D3D \_ OK. Se il metodo ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.

## <a name="remarks"></a>Commenti

Un'applicazione imposta un passaggio attivo (all'interno di una tecnica attiva) nel sistema degli effetti chiamando **ID3DXEffect::BeginPass**. Un'applicazione segnala la fine del passaggio attivo chiamando [**ID3DXEffect::EndPass**](id3dxeffect--endpass.md). **ID3DXEffect::BeginPass** e **ID3DXEffect::EndPass** devono essere presenti in una coppia corrispondente, all'interno di una coppia corrispondente di [**chiamate ID3DXEffect::Begin**](id3dxeffect--begin.md) e [**ID3DXEffect::End.**](id3dxeffect--end.md)

Se l'applicazione modifica uno stato di effetto usando uno dei metodi [**Effect::Setx**](id3dxeffect.md) all'interno di una coppia **id3DXEffect::BeginPass** / [**ID3DXEffect::EndPass**](id3dxeffect--endpass.md) corrispondente, l'applicazione deve chiamare [**ID3DXEffect::CommitChanges**](id3dxeffect--commitchanges.md) per impostare l'aggiornamento del dispositivo con le modifiche dello stato. Se non si verificano modifiche di stato all'interno di una coppia **id3DXEffect::BeginPass** e **ID3DXEffect::EndPass** corrispondente, non è necessario chiamare **ID3DXEffect::CommitChanges**.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Effect.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXEffect](id3dxeffect.md)
</dt> </dl>

 

 

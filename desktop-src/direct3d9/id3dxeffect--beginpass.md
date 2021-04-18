---
description: Inizia un passaggio, all'interno della tecnica attiva.
ms.assetid: fbb2bf1c-e37a-4117-8c3c-5f5b6a267301
title: 'Metodo ID3DXEffect:: BeginPass (D3DX9Effect. h)'
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
ms.openlocfilehash: 56a2648f65c3747f8a98fc0cdbd3ed06cea560b9
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322791"
---
# <a name="id3dxeffectbeginpass-method"></a>Metodo ID3DXEffect:: BeginPass

Inizia un passaggio, all'interno della tecnica attiva.

## <a name="syntax"></a>Sintassi


```C++
HRESULT BeginPass(
  [in] UINT Pass
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Passa* \[ in\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Indice integer in base zero nella tecnica.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è D3D \_ OK. Se il metodo ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.

## <a name="remarks"></a>Commenti

Un'applicazione imposta un passaggio attivo (all'interno di una tecnica attiva) nel sistema di effetti chiamando **ID3DXEffect:: BeginPass**. Un'applicazione segnala la fine del passaggio attivo chiamando [**ID3DXEffect:: EndPass**](id3dxeffect--endpass.md). **ID3DXEffect:: BeginPass** e **ID3DXEffect:: EndPass** devono essere presenti in una coppia corrispondente, all'interno di una coppia corrispondente di chiamate a [**ID3DXEffect:: Begin**](id3dxeffect--begin.md) e [**ID3DXEffect:: end**](id3dxeffect--end.md) .

Se l'applicazione modifica uno stato di effetto usando uno dei metodi [**Effect:: SETX**](id3dxeffect.md) all'interno di una coppia **ID3DXEffect:: BeginPass** / [**ID3DXEffect:: EndPass**](id3dxeffect--endpass.md) matching, l'applicazione deve chiamare [**ID3DXEffect:: CommitChanges**](id3dxeffect--commitchanges.md) per impostare l'aggiornamento del dispositivo con le modifiche dello stato. Se non vengono apportate modifiche allo stato all'interno di una coppia di **ID3DXEffect:: BeginPass** e **ID3DXEffect:: EndPass** , non è necessario chiamare **ID3DXEffect:: CommitChanges**.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Effect. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXEffect](id3dxeffect.md)
</dt> </dl>

 

 

---
description: Propagare le modifiche di stato che si verificano all'interno di un passaggio attivo al dispositivo prima del rendering.
ms.assetid: 3a779b63-c106-4a81-afeb-82bd6e556de4
title: 'Metodo ID3DXEffect:: CommitChanges (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.CommitChanges
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 41516c52b29dfe277cc857e44003de7783282a3a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104235049"
---
# <a name="id3dxeffectcommitchanges-method"></a>Metodo ID3DXEffect:: CommitChanges

Propagare le modifiche di stato che si verificano all'interno di un passaggio attivo al dispositivo prima del rendering.

## <a name="syntax"></a>Sintassi


```C++
HRESULT CommitChanges();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è D3D \_ OK. Se il metodo ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.

## <a name="remarks"></a>Commenti

Se l'applicazione modifica uno stato di effetto usando uno dei metodi [**ID3DXEffect:: SETX**](id3dxeffect.md) all'interno di una coppia [**ID3DXEffect:: BeginPass**](id3dxeffect--beginpass.md) / [**ID3DXEffect:: EndPass**](id3dxeffect--endpass.md) matching, l'applicazione deve chiamare **ID3DXEffect:: CommitChanges** prima di qualsiasi chiamata DrawxPrimitive per propagare le modifiche di stato al dispositivo prima del rendering. Se non vengono apportate modifiche allo stato all'interno di una coppia di **ID3DXEffect:: BeginPass** e **ID3DXEffect:: EndPass** , non è necessario chiamare **ID3DXEffect:: CommitChanges**.

Si tratta di un valore leggermente diverso per tutti i parametri condivisi in un effetto clonato. Quando una tecnica è attiva in un effetto clonato, ovvero quando [**ID3DXEffect:: Begin**](id3dxeffect--begin.md) è stato chiamato ma e [**ID3DXEffect:: end**](id3dxeffect--end.md) non è stato chiamato, **ID3DXEffect:: CommitChanges** aggiorna i parametri che non sono condivisi come previsto. Per aggiornare un parametro condiviso (solo per un effetto clonato la cui tecnica è attiva), chiamare **ID3DXEffect:: end** per disattivare la tecnica e **ID3DXEffect:: Begin** per riattivare la tecnica prima di chiamare **ID3DXEffect:: CommitChanges**.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Effect. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXEffect](id3dxeffect.md)
</dt> </dl>

 

 





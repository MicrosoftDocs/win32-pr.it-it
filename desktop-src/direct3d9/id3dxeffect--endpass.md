---
description: Termina un passaggio attivo.
ms.assetid: e20b3e0f-db9f-48e8-ab4e-761a5861f3ce
title: 'Metodo ID3DXEffect:: EndPass (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.EndPass
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 5cdba799f282e56bbe4565a4792906fd835e5c6c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355009"
---
# <a name="id3dxeffectendpass-method"></a>Metodo ID3DXEffect:: EndPass

Termina un passaggio attivo.

## <a name="syntax"></a>Sintassi


```C++
HRESULT EndPass();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Questo metodo restituisce sempre il valore S \_ OK.

## <a name="remarks"></a>Commenti

Un'applicazione segnala la fine del rendering di un passaggio attivo chiamando **ID3DXEffect:: EndPass**. Ogni **ID3DXEffect:: EndPass** deve far parte di una coppia corrispondente di chiamate a [**ID3DXEffect:: BeginPass**](id3dxeffect--beginpass.md) e **ID3DXEffect:: EndPass** .

Ogni coppia corrispondente di chiamate [**ID3DXEffect:: BeginPass**](id3dxeffect--beginpass.md) e **ID3DXEffect:: EndPass** deve trovarsi all'interno di una coppia corrispondente di chiamate a [**ID3DXEffect:: Begin**](id3dxeffect--begin.md) e [**ID3DXEffect:: end**](id3dxeffect--end.md) .

Se l'applicazione modifica uno stato di effetto usando uno dei metodi [**Effect:: SETX**](id3dxeffect.md) all'interno di una coppia [**ID3DXEffect:: BeginPass**](id3dxeffect--beginpass.md) / **ID3DXEffect:: EndPass** matching, l'applicazione deve chiamare [**ID3DXEffect:: CommitChanges**](id3dxeffect--commitchanges.md) prima di qualsiasi chiamata DrawxPrimitive per propagare le modifiche di stato al dispositivo prima del rendering.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Effect. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXEffect](id3dxeffect.md)
</dt> </dl>

 

 





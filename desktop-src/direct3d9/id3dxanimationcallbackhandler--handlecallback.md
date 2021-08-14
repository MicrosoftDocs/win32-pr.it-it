---
description: L'applicazione implementa questo metodo. Questo metodo viene chiamato quando si verifica un callback per un set di animazioni in una delle tracce durante una chiamata a ID3DXAnimationController::AdvanceTime.
ms.assetid: eb606fb0-d6b9-456d-97e1-b595306e6463
title: Metodo ID3DXAnimationCallbackHandler::HandleCallback (D3dx9anim.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationCallbackHandler.HandleCallback
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 12fcfa0feba1d239cf72c37e78fec63140dda4f954e7c48dffd643dcca4400c9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119279211"
---
# <a name="id3dxanimationcallbackhandlerhandlecallback-method"></a>Metodo ID3DXAnimationCallbackHandler::HandleCallback

L'applicazione implementa questo metodo. Questo metodo viene chiamato quando si verifica un callback per un set di animazioni in una delle tracce durante una chiamata a [**ID3DXAnimationController::AdvanceTime**](id3dxanimationcontroller--advancetime.md).

## <a name="syntax"></a>Sintassi


```C++
HRESULT HandleCallback(
  [in] UINT   Track,
  [in] LPVOID pCallbackData
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Tenere traccia* \[ Pollici\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Identificatore della traccia in cui si verifica il callback.

</dd> <dt>

*pCallbackData* \[ Pollici\]
</dt> <dd>

Tipo: **[ **LPVOID**](../winprog/windows-data-types.md)**

Puntatore ai dati di callback di proprietà dell'utente.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

I valori restituiti di questo metodo vengono implementati da un programmatore di applicazioni. In generale, se non si verifica alcun errore, programmare il metodo per restituire D3D \_ OK. In caso contrario, programmare il metodo per restituire un messaggio di errore appropriato da [D3DERR](d3derr.md) o [**D3DXERR**](./d3dxerr.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9anim.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXAnimationCallbackHandler](id3dxanimationcallbackhandler.md)
</dt> </dl>

 

 

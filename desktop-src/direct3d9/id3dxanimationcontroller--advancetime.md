---
description: Aggiunge un'animazione alla mesh e fa avanzare il tempo di animazione globale di una quantità specificata.
ms.assetid: a822d92a-c301-4289-b67b-1df99808c79d
title: Metodo ID3DXAnimationController::AdvanceTime (D3dx9anim.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.AdvanceTime
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 6c11a3b356fb0f09cc3372db3ccebd824b4dc8290ff586eed9de3b9fa2ea13ae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118987961"
---
# <a name="id3dxanimationcontrolleradvancetime-method"></a>Metodo ID3DXAnimationController::AdvanceTime

Aggiunge un'animazione alla mesh e fa avanzare il tempo di animazione globale di una quantità specificata.

## <a name="syntax"></a>Sintassi


```C++
HRESULT AdvanceTime(
  [in] DOUBLE                         TimeDelta,
  [in] LPD3DXANIMATIONCALLBACKHANDLER pCallbackHandler
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*TimeDelta* \[ Pollici\]
</dt> <dd>

Tipo: **[ **DOUBLE**](../winprog/windows-data-types.md)**

Quantità, in secondi, in base alla quale far avanzare il tempo di animazione globale. Il valore di TimeDelta deve essere non negativo o zero.

</dd> <dt>

*pCallbackHandler* \[ Pollici\]
</dt> <dd>

Tipo: **[ **LPD3DXANIMATIONCALLBACKHANDLER**](id3dxanimationcallbackhandler.md)**

Puntatore a un'interfaccia del gestore di callback dell'animazione definita dall'utente, [**ID3DXAnimationCallbackHandler.**](id3dxanimationcallbackhandler.md)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è S \_ OK. Se il metodo ha esito negativo, il valore restituito può essere uno dei valori seguenti: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9anim.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXAnimationController](id3dxanimationcontroller.md)
</dt> </dl>

 

 

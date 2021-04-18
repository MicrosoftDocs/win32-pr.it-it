---
description: Aggiunge un'animazione alla mesh e sposta in avanti il tempo di animazione globale in base a un importo specificato.
ms.assetid: a822d92a-c301-4289-b67b-1df99808c79d
title: 'Metodo ID3DXAnimationController:: AdvanceTime (D3dx9anim. h)'
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
ms.openlocfilehash: 848e1f8aadd302b9194168e92b2b0abe732a2c2f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323508"
---
# <a name="id3dxanimationcontrolleradvancetime-method"></a>Metodo ID3DXAnimationController:: AdvanceTime

Aggiunge un'animazione alla mesh e sposta in avanti il tempo di animazione globale in base a un importo specificato.

## <a name="syntax"></a>Sintassi


```C++
HRESULT AdvanceTime(
  [in] DOUBLE                         TimeDelta,
  [in] LPD3DXANIMATIONCALLBACKHANDLER pCallbackHandler
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*TimeDelta* \[ in\]
</dt> <dd>

Tipo: **[ **Double**](../winprog/windows-data-types.md)**

Quantità, in secondi, in base alla quale avanzare il tempo di animazione globale. Il valore di TimeDelta deve essere non negativo o zero.

</dd> <dt>

*pCallbackHandler* \[ in\]
</dt> <dd>

Tipo: **[ **LPD3DXANIMATIONCALLBACKHANDLER**](id3dxanimationcallbackhandler.md)**

Puntatore a un'interfaccia del gestore di callback di animazione definita dall'utente, [**ID3DXAnimationCallbackHandler**](id3dxanimationcallbackhandler.md).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è \_ OK. Se il metodo ha esito negativo, il valore restituito può essere uno dei valori seguenti: D3DERR \_ INVALIDCALL, E \_ OutOfMemory.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXAnimationController](id3dxanimationcontroller.md)
</dt> </dl>

 

 

---
description: Clona, o copia, un controller di animazione.
ms.assetid: 9836653c-9ea5-4fbc-89ac-0b46054a12d7
title: 'Metodo ID3DXAnimationController:: CloneAnimationController (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.CloneAnimationController
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 49c4a1c000df469c72a5e5538237e7110ded126f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355799"
---
# <a name="id3dxanimationcontrollercloneanimationcontroller-method"></a>Metodo ID3DXAnimationController:: CloneAnimationController

Clona, o copia, un controller di animazione.

## <a name="syntax"></a>Sintassi


```C++
HRESULT CloneAnimationController(
  [in] UINT                      MaxNumAnimationOutputs,
  [in] UINT                      MaxNumAnimationSets,
  [in] UINT                      MaxNumTracks,
  [in] UINT                      MaxNumEvents,
  [in] LPD3DXANIMATIONCONTROLLER *ppAnimController
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*MaxNumAnimationOutputs* \[ in\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Numero massimo di output di animazione che il controller può supportare.

</dd> <dt>

*MaxNumAnimationSets* \[ in\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Numero massimo di set di animazioni che il controller può supportare.

</dd> <dt>

*MaxNumTracks* \[ in\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Numero massimo di tracce che il controller può supportare.

</dd> <dt>

*MaxNumEvents* \[ in\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Numero massimo di eventi che il controller può supportare.

</dd> <dt>

*ppAnimController* \[ in\]
</dt> <dd>

Tipo: **[ **LPD3DXANIMATIONCONTROLLER**](id3dxanimationcontroller.md)\***

Indirizzo di un puntatore al controller di animazione [**ID3DXAnimationController**](id3dxanimationcontroller.md) clonato.

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

 

 

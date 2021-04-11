---
description: Attiva o disattiva l'output di debug di D3DX.
ms.assetid: e35cbfd2-401e-47ec-9f5b-e2ed63ea1fcd
title: Funzione D3DXDebugMute (D3dx9core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXDebugMute
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9259fa43a6a64829e42cbaa661aa7223a958f22d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104235023"
---
# <a name="d3dxdebugmute-function"></a>D3DXDebugMute (funzione)

Attiva o disattiva l'output di debug di D3DX.

## <a name="syntax"></a>Sintassi


```C++
BOOL D3DXDebugMute(
  _In_ BOOL Mute
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Disattiva* \[ in\]
</dt> <dd>

Tipo: **[ **bool**](../winprog/windows-data-types.md)**

Se **true**, l'output del debugger viene interrotto; Se **false**, l'output di debug è abilitato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **bool**](../winprog/windows-data-types.md)**

Restituisce il valore precedente di mute.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9core. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni per utilizzo generico](dx9-graphics-reference-d3dx-functions-general-purpose.md)
</dt> </dl>

 

 

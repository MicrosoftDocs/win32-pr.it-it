---
description: Abilita o Disabilita i messaggi di debug.
ms.assetid: 5c2aa3cf-ee6a-40fd-b300-67cb6ce691b6
title: Funzione D3DX10DebugMute (D3DX10Core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10DebugMute
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 6f331e3f074a4b77a1f1a7f1a8117cf660940f7d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323182"
---
# <a name="d3dx10debugmute-function"></a>D3DX10DebugMute (funzione)

Abilita o Disabilita i messaggi di debug.

## <a name="syntax"></a>Sintassi


```C++
HRESULT D3DX10DebugMute(
  _In_ BOOL Mute
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Disattiva* \[ in\]
</dt> <dd>

Tipo: **[ **bool**](../winprog/windows-data-types.md)**

Impostare su **true** per abilitare i messaggi di debug; impostare su **false** per disabilitare i messaggi di debug.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Il valore restituito è uno dei valori elencati in [codici restituiti Direct3D 10](d3d10-graphics-reference-returnvalues.md).

## <a name="remarks"></a>Commenti

Usare questa funzione per disabilitare i messaggi di errore per le API D3DX10 durante il debug; l'uso di questa funzione deve essere sorvegliato dall'opzione del \_ compilatore D3D10 debug.


```
#ifdef D3D10_DEBUG
  BOOL WINAPI D3DX10DebugMute(BOOL Mute);  
#endif
```



Lo stato predefinito è **true** per una compilazione di debug.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX10Core. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3DX10. lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni per utilizzo generico](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 

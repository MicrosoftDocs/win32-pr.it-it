---
description: Abilitare o disabilitare i messaggi di debug.
ms.assetid: 5c2aa3cf-ee6a-40fd-b300-67cb6ce691b6
title: Funzione D3DX10DebugMute (D3DX10Core.h)
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
ms.openlocfilehash: f4cd6a7ade60bc59cb1e6cbd9d3a447fac5cb7364db1ca85dcf704acedaa645c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119128383"
---
# <a name="d3dx10debugmute-function"></a>Funzione D3DX10DebugMute

Abilitare o disabilitare i messaggi di debug.

## <a name="syntax"></a>Sintassi


```C++
HRESULT D3DX10DebugMute(
  _In_ BOOL Mute
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Disattiva audio* \[ Pollici\]
</dt> <dd>

Tipo: **[ **BOOL**](../winprog/windows-data-types.md)**

Impostare su **TRUE per** abilitare i messaggi di debug. impostare su **FALSE per** disabilitare i messaggi di debug.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Il valore restituito è uno dei valori elencati in [Codici restituiti Direct3D 10.](d3d10-graphics-reference-returnvalues.md)

## <a name="remarks"></a>Commenti

Usare questa funzione per disabilitare i messaggi di errore per le API D3DX10 durante il debug. L'uso di questa funzione deve essere sorvegliato dall'opzione del compilatore DEBUG D3D10. \_


```
#ifdef D3D10_DEBUG
  BOOL WINAPI D3DX10DebugMute(BOOL Mute);  
#endif
```



Lo stato predefinito è **TRUE per** una compilazione di debug.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX10Core.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3DX10.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Per utilizzo generico funzioni](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 

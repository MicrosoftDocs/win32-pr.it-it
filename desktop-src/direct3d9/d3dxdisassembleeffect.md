---
description: Disassemblare un effetto.
ms.assetid: d95d6e97-2e79-4cd2-965e-483aa1a1ddbc
title: Funzione D3DXDisassembleEffect (D3DX9Effect.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXDisassembleEffect
api_type:
- LibDef
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: e4fa48418513cd9f4f70bc8356965a45499d1c6d822eaa1c1952d25ebe4b1ac2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120119221"
---
# <a name="d3dxdisassembleeffect-function"></a>Funzione D3DXDisassembleEffect

Disassemblare un effetto.

## <a name="syntax"></a>Sintassi


```C++
HRESULT D3DXDisassembleEffect(
  _In_  LPD3DXEFFECT pEffect,
  _In_  BOOL         EnableColorCode,
  _Out_ LPD3DXBUFFER *ppDisassembly
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pEffect* \[ Pollici\]
</dt> <dd>

Tipo: **[ **LPD3DXEFFECT**](id3dxeffect.md)**

Puntatore a [**un'interfaccia ID3DXEffect**](id3dxeffect.md) che contiene l'effetto.

</dd> <dt>

*EnableColorCode* \[ Pollici\]
</dt> <dd>

Tipo: **[ **BOOL**](../winprog/windows-data-types.md)**

Abilitare la codifica a colori per semplificare la lettura del disassembly.

</dd> <dt>

*ppDisassembly* \[ Cambio\]
</dt> <dd>

Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Restituisce un buffer contenente lo shader disassemblato. Vedere [**ID3DXBuffer**](id3dxbuffer.md).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se la funzione ha esito positivo, il valore restituito è D3D \_ OK. Se la funzione ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Effect.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni degli effetti](dx9-graphics-reference-effects-functions.md)
</dt> </dl>

 

 

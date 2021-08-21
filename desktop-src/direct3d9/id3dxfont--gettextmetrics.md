---
description: Recupera le caratteristiche del carattere identificate in una struttura TEXTMETRIC. Questo metodo supporta le impostazioni del compilatore ANSI e Unicode.
ms.assetid: 37788281-5bb0-45bb-b6d4-bdc4d811e3af
title: Metodo ID3DXFont::GetTextMetrics (D3dx9core.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFont.GetTextMetrics
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e9254ec9d5224f9041079f36bc95d68ea7346cf6dac2aecb81e7a6009496675e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118987411"
---
# <a name="id3dxfontgettextmetrics-method"></a>Metodo ID3DXFont::GetTextMetrics

Recupera le caratteristiche del carattere identificate in una [**struttura TEXTMETRIC.**](/windows/win32/api/wingdi/ns-wingdi-textmetrica) Questo metodo supporta le impostazioni del compilatore ANSI e Unicode.

## <a name="syntax"></a>Sintassi


```C++
BOOL GetTextMetrics(
  [out] TEXTMETRIC *pTextMetrics
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pTextMetrics* \[ Cambio\]
</dt> <dd>

Tipo: **[ **TEXTMETRIC**](/windows/win32/api/wingdi/ns-wingdi-textmetrica)\***

Puntatore a una [**struttura TEXTMETRIC**](/windows/win32/api/wingdi/ns-wingdi-textmetrica) che contiene le proprietà del tipo di carattere.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **BOOL**](../winprog/windows-data-types.md)**

Diverso da zero se la funzione ha esito positivo; in caso contrario, 0.

## <a name="remarks"></a>Commenti

L'impostazione del compilatore determina anche il tipo di struttura. Se è definito Unicode, la funzione restituisce una struttura TEXTMETRICW. In caso contrario, la chiamata di funzione restituisce una struttura TEXTMETRICA.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9core.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXFont](id3dxfont.md)
</dt> </dl>

 

 

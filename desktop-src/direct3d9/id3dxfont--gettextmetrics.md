---
description: Recupera le caratteristiche dei tipi di carattere identificate in una struttura TEXTMETRIC. Questo metodo supporta le impostazioni del compilatore ANSI e Unicode.
ms.assetid: 37788281-5bb0-45bb-b6d4-bdc4d811e3af
title: 'Metodo ID3DXFont:: GetTextMetrics (D3dx9core. h)'
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
ms.openlocfilehash: 6ce6064804d2aac2846cbea6971f145fc07759f3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354764"
---
# <a name="id3dxfontgettextmetrics-method"></a>Metodo ID3DXFont:: GetTextMetrics

Recupera le caratteristiche dei tipi di carattere identificate in una struttura [**TEXTMETRIC**](/windows/win32/api/wingdi/ns-wingdi-textmetrica) . Questo metodo supporta le impostazioni del compilatore ANSI e Unicode.

## <a name="syntax"></a>Sintassi


```C++
BOOL GetTextMetrics(
  [out] TEXTMETRIC *pTextMetrics
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pTextMetrics* \[ out\]
</dt> <dd>

Tipo: **[ **TEXTMETRIC**](/windows/win32/api/wingdi/ns-wingdi-textmetrica)\***

Puntatore a una struttura [**TEXTMETRIC**](/windows/win32/api/wingdi/ns-wingdi-textmetrica) che contiene le proprietà del tipo di carattere.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **bool**](../winprog/windows-data-types.md)**

Diverso da zero se la funzione ha esito positivo; in caso contrario, 0.

## <a name="remarks"></a>Commenti

L'impostazione del compilatore determina anche il tipo di struttura. Se è definito Unicode, la funzione restituisce una struttura Campo TEXTMETRICW. In caso contrario, la chiamata di funzione restituisce una struttura TEXTMETRICA.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9core. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXFont](id3dxfont.md)
</dt> </dl>

 

 

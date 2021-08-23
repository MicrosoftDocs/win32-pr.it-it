---
description: Recuperare le caratteristiche del tipo di carattere.
ms.assetid: ef7e0d18-492b-476b-945a-bfc0232a939a
title: Metodo ID3DX10Font::GetTextMetrics (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Font.GetTextMetrics
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 97cbddc59dd84d0a5b83610212fe94e87a49757da0430d64cb420280c815d9cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119047049"
---
# <a name="id3dx10fontgettextmetrics-method"></a>Metodo ID3DX10Font::GetTextMetrics

Recuperare le caratteristiche del tipo di carattere.

## <a name="syntax"></a>Sintassi


```C++
BOOL GetTextMetrics(
  [in] TEXTMETRIC *pTextMetrics
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pTextMetrics* \[ Pollici\]
</dt> <dd>

Tipo: **TEXTMETRIC \***

Puntatore a una [struttura TEXTMETRIC,](/previous-versions//ms534202(v=vs.85)) che contiene le proprietà del tipo di carattere. Se unicode è definito, la funzione restituisce una struttura TEXTMETRICW. In caso contrario, la funzione restituisce una struttura TEXTMETRICA.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **BOOL**](../winprog/windows-data-types.md)**

Diverso da zero se la funzione ha esito positivo; in caso contrario, 0.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX10.h</dt> </dl>   |
| Libreria<br/> | <dl> <dt>D3DX10.lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DX10Font](id3dx10font.md)
</dt> <dt>

[Interfacce D3DX](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 

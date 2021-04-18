---
description: Recuperare le caratteristiche dei tipi di carattere.
ms.assetid: ef7e0d18-492b-476b-945a-bfc0232a939a
title: 'Metodo ID3DX10Font:: GetTextMetrics (D3DX10. h)'
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
ms.openlocfilehash: 72decdcf0a9573f7ad8ba0f4e363df6df3599477
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104530937"
---
# <a name="id3dx10fontgettextmetrics-method"></a>Metodo ID3DX10Font:: GetTextMetrics

Recuperare le caratteristiche dei tipi di carattere.

## <a name="syntax"></a>Sintassi


```C++
BOOL GetTextMetrics(
  [in] TEXTMETRIC *pTextMetrics
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pTextMetrics* \[ in\]
</dt> <dd>

Tipo: **TEXTMETRIC \***

Puntatore a una struttura [TEXTMETRIC](/previous-versions//ms534202(v=vs.85)) che contiene le proprietà del tipo di carattere. Se è definito Unicode, la funzione restituisce una struttura Campo TEXTMETRICW. In caso contrario, la funzione restituisce una struttura TEXTMETRICA.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **bool**](../winprog/windows-data-types.md)**

Diverso da zero se la funzione ha esito positivo; in caso contrario, 0.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX10. h</dt> </dl>   |
| Libreria<br/> | <dl> <dt>D3DX10. lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DX10Font](id3dx10font.md)
</dt> <dt>

[Interfacce D3DX](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 

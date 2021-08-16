---
title: EM_SETEDITSTYLEEX messaggio (Richedit.h)
description: Imposta i flag di stile di modifica estesi correnti.
ms.assetid: C5CECC7C-6418-4A72-9F0B-6F55BE89E302
keywords:
- EM_SETEDITSTYLEEX dei messaggi Windows controlli
topic_type:
- apiref
api_name:
- EM_SETEDITSTYLEEX
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b96a353b62dc3a31affd9e827ee803c481bcd806eaad9f8a5d0e9dd35388cf5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117831222"
---
# <a name="em_seteditstyleex-message"></a>Messaggio EM \_ SETEDITSTYLEEX

Imposta i flag di stile di modifica estesi correnti.


```C++
#define EM_SETEDITSTYLEEX       (WM_USER + 275)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Specifica uno o più flag di stile di modifica estesi. Per un elenco dei valori possibili, vedere [**EM \_ GETEDITSTYLEEX**](/windows/desktop/Controls/em-geteditstyleex).

</dd> <dt>

*lParam* 
</dt> <dd>

Maschera costituita da uno o più valori *wParam.* Verranno impostati o cancellati solo i valori specificati in questa maschera. In questo modo è possibile impostare o cancellare un singolo flag senza leggere gli stati del flag corrente.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito è lo stato dei flag di stile di modifica estesi dopo che rich edit ha tentato di implementare le modifiche di stile di modifica. I flag di stile di modifica sono un set di flag che indicano lo stile di modifica corrente.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8 solo app desktop\]<br/>                                            |
| Server minimo supportato<br/> | \[Windows Server 2012 solo app desktop\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**EM \_ GETEDITSTYLEEX**](em-geteditstyleex.md)
</dt> </dl>

 


---
title: Messaggio di EM_SETEDITSTYLEEX (RichEdit. h)
description: Imposta i flag di stile di modifica estesa correnti.
ms.assetid: C5CECC7C-6418-4A72-9F0B-6F55BE89E302
keywords:
- Controlli di Windows Message EM_SETEDITSTYLEEX
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
ms.openlocfilehash: 72fe7a1ff420048f620d69196360678e9718a510
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964755"
---
# <a name="em_seteditstyleex-message"></a>\_Messaggio SETEDITSTYLEEX em

Imposta i flag di stile di modifica estesa correnti.


```C++
#define EM_SETEDITSTYLEEX       (WM_USER + 275)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Specifica uno o più flag di stile di modifica estesa. Per un elenco di valori possibili, vedere [**em \_ GETEDITSTYLEEX**](/windows/desktop/Controls/em-geteditstyleex).

</dd> <dt>

*lParam* 
</dt> <dd>

Maschera costituita da uno o più valori *wParam* . Verranno impostati o cancellati solo i valori specificati in questa maschera. In questo modo è possibile impostare o cancellare un flag singolo senza leggere gli Stati del flag corrente.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito è lo stato dei flag di stile di modifica estesa dopo che Rich Edit ha tentato di implementare le modifiche dello stile di modifica. I flag di stile di modifica sono un set di flag che indicano lo stile di modifica corrente.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 8\]<br/>                                            |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2012\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_GETEDITSTYLEEX em**](em-geteditstyleex.md)
</dt> </dl>

 


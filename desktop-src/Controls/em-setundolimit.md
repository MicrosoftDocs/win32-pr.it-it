---
title: Messaggio di EM_SETUNDOLIMIT (RichEdit. h)
description: Imposta il numero massimo di azioni che possono essere archiviate nella coda di annullamento di un controllo Rich Edit.
ms.assetid: 485dbcda-89f4-40de-ad55-cd524958e910
keywords:
- Controlli di Windows Message EM_SETUNDOLIMIT
topic_type:
- apiref
api_name:
- EM_SETUNDOLIMIT
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c5b668d047f1de6d8720f09af5baf23e7cfc9cc2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964384"
---
# <a name="em_setundolimit-message"></a>\_Messaggio SETUNDOLIMIT em

Imposta il numero massimo di azioni che possono essere archiviate nella coda di annullamento di un controllo Rich Edit.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Specifica il numero massimo di azioni che possono essere archiviate nella coda di annullamento.

</dd> <dt>

*lParam* 
</dt> <dd>

Questo parametro non viene utilizzato. deve essere zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito è il nuovo numero massimo di azioni di annullamento per il controllo Rich Edit. Se la memoria è limitata, questo valore può essere inferiore a *wParam* .

## <a name="remarks"></a>Commenti

Per impostazione predefinita, il numero massimo di azioni nella coda di annullamento è 100. Se si aumenta questo numero, è necessario che la memoria disponibile sia sufficiente per contenere il nuovo numero. Per ottenere prestazioni migliori, impostare il limite sul valore più piccolo possibile.

Se si imposta il limite su zero, la funzionalità di **annullamento** viene disabilitata.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**\_CANREDO em**](em-canredo.md)
</dt> <dt>

[**\_GETredoname em**](em-getredoname.md)
</dt> <dt>

[**EM \_ GETundoname**](em-getundoname.md)
</dt> <dt>

[**\_ripetizione em**](em-redo.md)
</dt> <dt>

[**\_Annulla**](em-undo.md)
</dt> </dl>

 

 






---
title: Messaggio di EM_SETTOUCHOPTIONS (RichEdit. h)
description: Imposta le opzioni di tocco associate a un controllo Rich Edit.
ms.assetid: C15036D6-B74F-414D-B731-F1587B616644
keywords:
- Controlli di Windows Message EM_SETTOUCHOPTIONS
topic_type:
- apiref
api_name:
- EM_SETTOUCHOPTIONS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7613679a574955ef726da9fa10e8d919c8fe53b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477308"
---
# <a name="em_settouchoptions-message"></a>\_Messaggio SETTOUCHOPTIONS em

Imposta le opzioni di tocco associate a un controllo Rich Edit.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Opzione di tocco da impostare. Questo parametro può avere uno dei valori seguenti.



| Valore                                                                                                                                                                        | Significato                                                                                                                                                                                                                                      |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RTO_SHOWHANDLES"></span><span id="rto_showhandles"></span><dl> <dt>**\_SHOWHANDLES RTO**</dt> </dl>          | Mostrare o nascondere i punti di manipolazione del tocco, a seconda del valore di *lParam*.<br/>                                                                                                                                                       |
| <span id="RTO_DISABLEHANDLES"></span><span id="rto_disablehandles"></span><dl> <dt>**\_DISABLEHANDLES RTO**</dt> </dl> | Consente di abilitare o disabilitare gli handle del grip touch, a seconda del valore di *lParam*. Quando gli handle sono disabilitati, vengono nascosti se sono visibili e rimangono nascosti fino a quando un messaggio **\_ SETTOUCHOPTIONS em** non cambia il proprio stato. <br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Impostare su **true** per visualizzare/abilitare gli handle di selezione tocco oppure su **false** per nascondere o disabilitare gli handle di selezione tocco.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo messaggio restituisce zero.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 8\]<br/>                                            |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2012\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_GETTOUCHOPTIONS em**](em-settouchoptions.md)
</dt> </dl>

 

 






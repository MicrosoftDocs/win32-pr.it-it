---
title: EM_SETTOUCHOPTIONS messaggio (Richedit.h)
description: Imposta le opzioni di tocco associate a un controllo Rich Edit.
ms.assetid: C15036D6-B74F-414D-B731-F1587B616644
keywords:
- EM_SETTOUCHOPTIONS di controllo Windows messaggio
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
ms.openlocfilehash: 4ea2f372d1e59a76ea13667e994534df1088fe1c78c51c30ac54db1b4dfeed2d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120048011"
---
# <a name="em_settouchoptions-message"></a>Messaggio \_ EM SETTOUCHOPTIONS

Imposta le opzioni di tocco associate a un controllo Rich Edit.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Opzione di tocco da impostare. Questo parametro può avere uno dei valori seguenti.



| Valore                                                                                                                                                                        | Significato                                                                                                                                                                                                                                      |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RTO_SHOWHANDLES"></span><span id="rto_showhandles"></span><dl> <dt>**RTO \_ SHOWHANDLES**</dt> </dl>          | Mostra o nasconde i quadratini di ridimensionamento del tocco, a seconda del valore di *lParam*.<br/>                                                                                                                                                       |
| <span id="RTO_DISABLEHANDLES"></span><span id="rto_disablehandles"></span><dl> <dt>**RTO \_ DISABLEHANDLES**</dt> </dl> | Abilitare o disabilitare i quadratini di ridimensionamento tocco, a seconda del valore di *lParam*. Quando gli handle sono disabilitati, vengono nascosti se sono visibili e rimangono nascosti fino a quando non viene modificato lo stato di un messaggio **EM \_ SETTOUCHOPTIONS.** <br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Impostare su **TRUE per** visualizzare/abilitare i punti di manipolazione di selezione tocco o **SU FALSE** per nascondere o disabilitare i punti di manipolazione di selezione tocco.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo messaggio restituisce zero.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8 solo app desktop\]<br/>                                            |
| Server minimo supportato<br/> | \[Windows Server 2012 solo app desktop\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**EM \_ GETTOUCHOPTIONS**](em-settouchoptions.md)
</dt> </dl>

 

 






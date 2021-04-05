---
title: Messaggio TB_SETLISTGAP (COMmctrl. h)
description: Imposta la distanza tra i pulsanti della barra degli strumenti su una barra degli strumenti specifica.
ms.assetid: ca8ba6e4-cf70-41ca-ac61-cd13671d4010
keywords:
- Controlli di Windows Message TB_SETLISTGAP
topic_type:
- apiref
api_name:
- TB_SETLISTGAP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 224a709b7beefcfdf49ea7838f905977487aca8d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873281"
---
# <a name="tb_setlistgap-message"></a>TB \_ SETLISTGAP messaggio

Imposta la distanza tra i pulsanti della barra degli strumenti su una barra degli strumenti specifica.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Gap, in pixel, tra i pulsanti sulla barra degli strumenti.

</dd> <dt>

*lParam* 
</dt> <dd>

Ignorato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="remarks"></a>Commenti

Il gap tra i pulsanti si applica solo alla finestra di controllo della barra degli strumenti che riceve questo messaggio. La ricezione di questo messaggio attiva un ridisegno della barra degli strumenti, se la barra degli strumenti è attualmente visibile.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 






---
title: Messaggio PBM_GETRANGE (COMmctrl. h)
description: Recupera le informazioni sui limiti massimo e minimo correnti di un determinato controllo indicatore di stato.
ms.assetid: 676b7a37-bdde-4307-9888-9a0cf40db2db
keywords:
- Controlli di Windows Message PBM_GETRANGE
topic_type:
- apiref
api_name:
- PBM_GETRANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0c4ffe9365686432a5e78cb1540055f41a838fc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964566"
---
# <a name="pbm_getrange-message"></a>Messaggio della gestione della serie di Criteri PBM \_

Recupera le informazioni sui limiti massimo e minimo correnti di un determinato controllo indicatore di stato.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Valore del flag che specifica il valore del limite da utilizzare come valore restituito del messaggio. Questo parametro può essere uno dei valori seguenti:



| Valore                                                                                                                                    | Significato                           |
|------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------|
| <span id="TRUE"></span><span id="true"></span><dl> <dt>TRUE * * * *</dt> </dl>    | Restituisce il limite minimo.<br/>  |
| <span id="FALSE"></span><span id="false"></span><dl> <dt>FALSE * * * *</dt> </dl> | Restituisce il limite massimo.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**PBRANGE**](/windows/desktop/api/Commctrl/ns-commctrl-pbrange) che deve essere riempita con i limiti massimo e minimo del controllo indicatore di stato. Se questo parametro è impostato su **null**, il controllo restituirà solo il limite specificato da *wParam*.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore INT che rappresenta il valore limite specificato da *wParam*. Se *lParam* non è **null**, *lParam* deve puntare a una struttura [**PBRANGE**](/windows/desktop/api/Commctrl/ns-commctrl-pbrange) che deve essere riempita con entrambi i valori limite.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 






---
title: PBM_GETRANGE messaggio (Commctrl.h)
description: Recupera informazioni sui limiti massimo e minimo correnti di un determinato controllo indicatore di stato.
ms.assetid: 676b7a37-bdde-4307-9888-9a0cf40db2db
keywords:
- PBM_GETRANGE controlli Windows messaggio
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
ms.openlocfilehash: 007a62386180e7b47edca201236cd1dacc86df696b5705d02ec1da0acb89761c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119986401"
---
# <a name="pbm_getrange-message"></a>Messaggio \_ GETRANGE PBM

Recupera informazioni sui limiti massimo e minimo correnti di un determinato controllo indicatore di stato.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Valore del flag che specifica il valore limite da usare come valore restituito del messaggio. Questo parametro può essere uno dei valori seguenti:



| Valore                                                                                                                                    | Significato                           |
|------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------|
| <span id="TRUE"></span><span id="true"></span><dl> <dt>TRUE****</dt> </dl>    | Restituisce il limite basso.<br/>  |
| <span id="FALSE"></span><span id="false"></span><dl> <dt>FALSE****</dt> </dl> | Restituisce il limite massimo.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a [**una struttura PBRANGE**](/windows/desktop/api/Commctrl/ns-commctrl-pbrange) che deve essere riempita con i limiti massimo e minimo del controllo indicatore di stato. Se questo parametro è impostato su **NULL,** il controllo restituirà solo il limite specificato da *wParam*.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore INT che rappresenta il valore limite specificato da *wParam.* Se *lParam* non è **NULL,** *lParam* deve puntare a una struttura [**PBRANGE**](/windows/desktop/api/Commctrl/ns-commctrl-pbrange) che deve essere riempita con entrambi i valori limite.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 






---
title: Messaggio DRV_CONFIGURE (mmsystem. h)
description: Indica al driver installabile di visualizzare la finestra di dialogo di configurazione e consentire all'utente di specificare nuove impostazioni per l'istanza del driver installabile specificata.
ms.assetid: 0d99fad7-ce79-4574-9fd8-262f7e758866
keywords:
- DRV_CONFIGURE messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- DRV_CONFIGURE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 30a761e7bda7188e93b02e436f2e952bed61bee9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964921"
---
# <a name="drv_configure-message"></a>\_Messaggio di configurazione DRV

Indica al driver installabile di visualizzare la finestra di dialogo di configurazione e consentire all'utente di specificare nuove impostazioni per l'istanza del driver installabile specificata.

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="dwDriverId"></span><span id="dwdriverid"></span><span id="DWDRIVERID"></span>*dwDriverId*
</dt> <dd>

Identificatore del driver installabile. Si tratta dello stesso valore restituito in precedenza dal driver dal messaggio [**\_ aperto DRV**](drv-open.md) .

</dd> <dt>

<span id="hdrvr"></span><span id="HDRVR"></span>*hdrvr*
</dt> <dd>

Handle dell'istanza del driver installabile.

</dd> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

Handle della finestra padre. Questa finestra viene utilizzata come finestra padre per la finestra di dialogo di configurazione.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Indirizzo di una struttura [**DRVCONFIGINFO**](/windows/win32/api/mmiscapi/ns-mmiscapi-drvconfiginfo) o **null**. Se la struttura è specificata, contiene i nomi della chiave del registro di sistema e il valore associato al driver.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce uno dei valori seguenti:



| Requisito | Valore |
|-----------------|----------------------------------------------------------------------------------------------------|
| DRVCNF \_ OK      | La configurazione è stata completata. non sono necessarie altre azioni.                                    |
| \_annullamento DRVCNF  | L'utente ha annullato la finestra di dialogo; non sono necessarie altre azioni.                                   |
| \_riavvio DRVCNF | La configurazione ha esito positivo, ma le modifiche non diventano effettive fino al riavvio del sistema. |



 

## <a name="remarks"></a>Commenti

Alcuni driver installabili accodano informazioni di configurazione al valore assegnato al valore del registro di sistema associato al driver.

I \_ valori restituiti da DRV Cancel, DRV \_ OK e DRV \_ Restart sono obsoleti e sono stati sostituiti rispettivamente da DRVCNF \_ Cancel, DRVCNF \_ OK e DRVCNF \_ restart.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Mmsystem. h (include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Driver installabili](installable-drivers.md)
</dt> <dt>

[Messaggi di driver installabili](installable-driver-messages.md)
</dt> </dl>

 


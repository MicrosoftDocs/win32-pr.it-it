---
title: Messaggio DRV_INSTALL (mmsystem. h)
description: Notifica al driver che è in fase di installazione. Il driver deve creare e inizializzare le chiavi e i valori del registro di sistema necessari e verificare che i driver e l'hardware di supporto siano installati e configurati correttamente.
ms.assetid: 8ee7b30b-600b-49f3-93a7-8faa7b87cfd8
keywords:
- DRV_INSTALL messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- DRV_INSTALL
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15c91c71a4cb65bfaffa07bf16e09bec0d16b7b4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964918"
---
# <a name="drv_install-message"></a>\_Messaggio di installazione DRV

Notifica al driver che è in fase di installazione. Il driver deve creare e inizializzare le chiavi e i valori del registro di sistema necessari e verificare che i driver e l'hardware di supporto siano installati e configurati correttamente.

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

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Indirizzo di una struttura [**DRVCONFIGINFO**](/windows/win32/api/mmiscapi/ns-mmiscapi-drvconfiginfo) o **null**. Se viene fornita una struttura, contiene i nomi della chiave del registro di sistema e il valore associato al driver.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce uno dei valori seguenti:



| Requisito | Valore |
|-----------------|--------------------------------------------------------------------------------------------|
| DRVCNF \_ OK      | L'installazione è riuscita. non sono necessarie altre azioni.                             |
| \_annullamento DRVCNF  | Installazione non riuscita..                                                                  |
| \_riavvio DRVCNF | L'installazione ha esito positivo, ma non diventa effettiva fino al riavvio del sistema. |



 

## <a name="remarks"></a>Commenti

Il parametro *lParam1* non viene utilizzato.

Alcuni driver installabili accodano informazioni di configurazione al valore assegnato al valore del registro di sistema associato al driver.

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

 


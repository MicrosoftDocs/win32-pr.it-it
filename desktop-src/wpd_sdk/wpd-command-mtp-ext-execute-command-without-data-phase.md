---
description: Il comando WPD \_ COMMAND \_ MTP \_ EXT \_ EXECUTE COMMAND WITHOUT DATA PHASE invia un blocco di comandi \_ \_ \_ \_ MTP. A questo comando non è associata alcuna fase dati successiva.
ms.assetid: 308550d0-1399-4b64-8f8e-dc16d5044086
title: WPD_COMMAND_MTP_EXT_EXECUTE_COMMAND_WITHOUT_DATA_PHASE comando (WpdMtpExtensions.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2c4d1d5af4d1e4e712f3a39dd5cbb296133bb16f4de3b677da4a45fa7bbc204
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119806301"
---
# <a name="wpd_command_mtp_ext_execute_command_without_data_phase-command"></a>COMANDO WPD \_ \_ MTP \_ EXT \_ EXECUTE COMMAND WITHOUT DATA PHASE \_ \_ \_ \_ COMMAND

Il **comando WPD \_ COMMAND \_ MTP \_ EXT EXECUTE COMMAND WITHOUT \_ DATA \_ \_ \_ \_ PHASE** invia un blocco di comandi MTP. A questo comando non è associata alcuna fase dati successiva.

## <a name="command-category"></a>Categoria

**OPERAZIONI DEL FORNITORE EXT DELLA CATEGORIA \_ \_ WPD MTP \_ \_ \_**

## <a name="parameters"></a>Parametri

Per il driver sono previsti i parametri seguenti.



| Parametro                                      | VarType | Descrizione                                                                                                                   |
|------------------------------------------------|---------|-------------------------------------------------------------------------------------------------------------------------------|
| **CODICE DELL'OPERAZIONE \_ \_ MTP \_ EXT \_ DELLA \_ PROPRIETÀ WPD**   | Interfaccia utente \_ VT4 | Obbligatorio. Identifica un codice operazione MTP esteso dal fornitore.                                                                    |
| **PARAMETRI DELL'OPERAZIONE \_ \_ \_ MTP EXT \_ DELLA \_ PROPRIETÀ WPD** | Interfaccia utente \_ VT4 | Obbligatorio. Oggetto **IPortableDevicePropVariantCollection** che identifica i parametri necessari per il codice dell'operazione del fornitore. |



 

## <a name="return-value"></a>Valore restituito

Il driver restituisce i risultati seguenti.



| Risultato                                        | VarType | Descrizione                                                                                                                    |
|-----------------------------------------------|---------|--------------------------------------------------------------------------------------------------------------------------------|
| **CODICE DI RISPOSTA EXT DELLA PROPRIETÀ WPD \_ \_ MTP \_ \_ \_**   | Interfaccia utente \_ VT4 | Obbligatorio. Codice di risposta al codice dell'operazione del fornitore.                                                                      |
| **PARAMETRI DI RISPOSTA \_ \_ MTP \_ EXT \_ DELLA \_ PROPRIETÀ WPD** | Interfaccia utente \_ VT4 | facoltativo. Oggetto **IPortableDevicePropVariantCollection** che identifica i parametri di risposta. Questa raccolta potrebbe essere vuota. |



 

## <a name="calling-methods"></a>Chiamata di metodi

Può essere chiamato direttamente solo tramite [**IPortableDevice::SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-----------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>WpdMtpExtensions.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Supporto delle estensioni MTP](supporting-mtp-extensions.md)
</dt> </dl>

 

 





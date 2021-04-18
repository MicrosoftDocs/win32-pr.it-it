---
description: Il comando \_ WPD \_ MTP \_ ext \_ Execute \_ Command \_ without \_ data \_ Phase Invia un blocco di comandi MTP. A questo comando non è associata alcuna fase di dati successiva.
ms.assetid: 308550d0-1399-4b64-8f8e-dc16d5044086
title: Comando WPD_COMMAND_MTP_EXT_EXECUTE_COMMAND_WITHOUT_DATA_PHASE (WpdMtpExtensions. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b58648547c33206e1de19c14aea48427bc9db0be
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330576"
---
# <a name="wpd_command_mtp_ext_execute_command_without_data_phase-command"></a>Comando \_ WPD \_ MTP \_ ext \_ Execute \_ Command \_ without \_ data \_ fase Command

Il **comando \_ WPD \_ MTP \_ ext \_ Execute \_ Command \_ without \_ data \_ Phase** Invia un blocco di comandi MTP. A questo comando non è associata alcuna fase di dati successiva.

## <a name="command-category"></a>Categoria

**WPD \_ categoria \_ MTP \_ \_ operazioni fornitore \_ ext**

## <a name="parameters"></a>Parametri

Per il driver sono previsti i parametri seguenti.



| Parametro                                      | VarType | Descrizione                                                                                                                   |
|------------------------------------------------|---------|-------------------------------------------------------------------------------------------------------------------------------|
| **\_Proprietà WPD \_ \_ \_ codice operativo MTP \_ ext**   | \_UI4 VT | Obbligatorio. Identifica un codice operativo MTP esteso dal fornitore.                                                                    |
| **\_Proprietà WPD \_ - \_ \_ parametri operazione MTP ext \_** | \_UI4 VT | Obbligatorio. Oggetto **IPortableDevicePropVariantCollection**, che identifica i parametri obbligatori per il codice operativo del fornitore. |



 

## <a name="return-value"></a>Valore restituito

Il driver restituisce i risultati seguenti.



| Risultato                                        | VarType | Descrizione                                                                                                                    |
|-----------------------------------------------|---------|--------------------------------------------------------------------------------------------------------------------------------|
| **\_Proprietà WPD \_ \_ codice di \_ risposta MTP ext \_**   | \_UI4 VT | Obbligatorio. Codice di risposta al codice operativo del fornitore.                                                                      |
| **\_Proprietà WPD \_ \_ parametri di \_ risposta MTP ext \_** | \_UI4 VT | facoltativo. Oggetto **IPortableDevicePropVariantCollection** che identifica i parametri della risposta. Questa raccolta potrebbe essere vuota. |



 

## <a name="calling-methods"></a>Chiamata di metodi

Può essere chiamato solo direttamente tramite [**IPortableDevice:: SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-----------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>WpdMtpExtensions. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Supporto delle estensioni MTP](supporting-mtp-extensions.md)
</dt> </dl>

 

 





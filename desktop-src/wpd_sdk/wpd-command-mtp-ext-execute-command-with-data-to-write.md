---
description: Il comando WPD COMMAND MTP EXT EXECUTE COMMAND WITH DATA TO WRITE invia un blocco di comandi \_ \_ \_ \_ \_ \_ \_ \_ MTP, seguito da una fase \_ dati. I dati vengono inviati dall'host al dispositivo.
ms.assetid: b675fc3c-4d50-429d-9e00-42160d409a2b
title: WPD_COMMAND_MTP_EXT_EXECUTE_COMMAND_WITH_DATA_TO_WRITE comando (WpdMtpExtensions.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b2ae0e50ad2fad9967252d9a21c1e864d056338a3e3a2b82f4c29d951a722953
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119806311"
---
# <a name="wpd_command_mtp_ext_execute_command_with_data_to_write-command"></a>COMANDO WPD \_ \_ MTP \_ EXT \_ EXECUTE CON COMANDO DATA TO \_ \_ \_ \_ \_ WRITE

Il **comando WPD \_ COMMAND \_ MTP \_ EXT EXECUTE COMMAND WITH \_ DATA TO \_ \_ \_ \_ \_ WRITE** invia un blocco di comandi MTP, seguito da una fase dati. I dati vengono inviati dall'host al dispositivo.

## <a name="command-category"></a>Categoria

**OPERAZIONI DEL FORNITORE EXT DELLA CATEGORIA \_ \_ WPD MTP \_ \_ \_**

## <a name="parameters"></a>Parametri

Per il driver sono previsti i parametri seguenti.



| Parametro                                                | VarType | Descrizione                                                                                                                             |
|----------------------------------------------------------|---------|-----------------------------------------------------------------------------------------------------------------------------------------|
| **CODICE DELL'OPERAZIONE \_ \_ MTP \_ EXT \_ DELLA \_ PROPRIETÀ WPD**             | Interfaccia utente \_ VT4 | Obbligatorio. Identifica un codice operazione MTP esteso dal fornitore.                                                                              |
| **PARAMETRI DELL'OPERAZIONE \_ \_ \_ MTP EXT \_ DELLA \_ PROPRIETÀ WPD**           | Interfaccia utente \_ VT4 | Obbligatorio. Raccolta **IPortableDevicePropVariantCollection** che identifica i parametri necessari per il codice dell'operazione del fornitore. |
| **DIMENSIONI TOTALI DEI DATI DI TRASFERIMENTO \_ \_ \_ MTP EXT \_ \_ DELLA \_ \_ PROPRIETÀ WPD** | Interfaccia utente \_ VT8 | Required.Specifica le dimensioni totali dei dati, in byte, escluso l'overhead, da inviare al dispositivo.                                         |



 

## <a name="return-value"></a>Valore restituito

Il driver restituisce i risultati seguenti.



| Risultato                                                       | VarType    | Descrizione                                                                        |
|--------------------------------------------------------------|------------|------------------------------------------------------------------------------------|
| **PROPRIETÀ WPD \_ \_ MTP \_ EXT \_ DIMENSIONI OTTIMALI DEL BUFFER DI \_ \_ \_ TRASFERIMENTO** | Interfaccia utente \_ VT4    | Obbligatorio. Specifica le dimensioni ottimali del buffer di trasferimento.                       |
| **CONTESTO DI TRASFERIMENTO EXT DELLA PROPRIETÀ WPD \_ \_ MTP \_ \_ \_**               | VT \_ LPWSTR | facoltativo. Identificatore di contesto utilizzato dal driver per i trasferimenti di dati successivi. |



 

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

 

 





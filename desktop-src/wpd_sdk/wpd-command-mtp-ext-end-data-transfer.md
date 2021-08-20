---
description: Il comando WPD \_ COMMAND MTP EXT END DATA TRANSFER completa un trasferimento dei dati e la lettura \_ della risposta dal \_ \_ \_ \_ dispositivo.
ms.assetid: df2da2e6-ed5a-41a1-be30-844c0d6b409b
title: WPD_COMMAND_MTP_EXT_END_DATA_TRANSFER comando (WpdMtpExtensions.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc064d1de151e8b3ebd54245249d8bf9ffa8ecbd41bbe61c36768add4329f092
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118026776"
---
# <a name="wpd_command_mtp_ext_end_data_transfer-command"></a>Comando WPD \_ \_ MTP \_ EXT \_ END DATA \_ \_ TRANSFER

Il **comando WPD \_ COMMAND \_ MTP \_ EXT END DATA \_ \_ \_ TRANSFER** completa un trasferimento dei dati e la lettura della risposta dal dispositivo. Il trasferimento viene avviato dal comando [**WPD \_ COMMAND \_ MTP \_ EXT \_ EXECUTE COMMAND WITH DATA TO \_ \_ \_ \_ \_ READ**](/windows/desktop/wpd_sdk/wpd-command-mtp-ext-execute-command-with-data-to-read) o dal comando [**WPD \_ COMMAND \_ MTP \_ EXT EXECUTE COMMAND WITH \_ DATA TO \_ \_ \_ \_ \_ WRITE.**](/windows/desktop/wpd_sdk/wpd-command-mtp-ext-execute-command-with-data-to-write)

## <a name="command-category"></a>Categoria

**WPD \_ CATEGORY \_ MTP \_ EXT \_ VENDOR \_ OPERATIONS**

## <a name="parameters"></a>Parametri

Per il driver sono previsti i parametri seguenti.



| Parametro                                      | VarType    | Descrizione                                                                  |
|------------------------------------------------|------------|------------------------------------------------------------------------------|
| **CONTESTO DI TRASFERIMENTO \_ \_ MTP \_ EXT \_ DELLA PROPRIETÀ \_ WPD** | VT \_ LPWSTR | Obbligatorio. Identifica il contesto restituito da una precedente chiamata al metodo. |



 

## <a name="return-value"></a>Valore restituito

Il driver restituisce i risultati seguenti.



| Risultato                                        | VarType | Descrizione                                                                                                                             |
|-----------------------------------------------|---------|-----------------------------------------------------------------------------------------------------------------------------------------|
| **CODICE DI RISPOSTA \_ \_ MTP \_ EXT DELLA \_ \_ PROPRIETÀ WPD**   | VT \_ UI4 | Obbligatorio. Codice di risposta al codice dell'operazione del fornitore.                                                                                |
| **PARAMETRI DI RISPOSTA \_ \_ MTP \_ EXT \_ DELLA PROPRIETÀ \_ WPD** | VT \_ UI4 | facoltativo. Raccolta **IPortableDevicePropVariantCollection** che identifica i parametri della risposta. Questa raccolta può essere vuota. |



 

## <a name="calling-methods"></a>Chiamata di metodi

Può essere chiamato direttamente solo tramite [**IPortableDevice::SendCommand.**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-----------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>WpdMtpExtensions.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Supporto delle estensioni MTP](supporting-mtp-extensions.md)
</dt> </dl>

 


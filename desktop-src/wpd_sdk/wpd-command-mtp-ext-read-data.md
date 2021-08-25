---
description: Il comando WPD COMMAND MTP EXT READ DATA recupera i dati dal dispositivo dopo l'esecuzione del comando \_ \_ \_ \_ \_ WPD \_ COMMAND \_ MTP \_ EXT \_ EXECUTE WITH DATA \_ TO \_ \_ \_ \_ READ.
ms.assetid: d7acb2cc-28b0-4314-99fd-4e7eded22122
title: WPD_COMMAND_MTP_EXT_READ_DATA comando (WpdMtpExtensions.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c5aeee37e1922f91e9a9fac7881369364d01340893829678a5651f89ed428440
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119927951"
---
# <a name="wpd_command_mtp_ext_read_data-command"></a>Comando WPD \_ \_ MTP \_ EXT \_ READ \_ DATA

Il **comando WPD \_ COMMAND \_ MTP \_ EXT READ \_ \_ DATA** recupera i dati dal dispositivo dopo l'esecuzione del comando **WPD \_ COMMAND \_ MTP \_ EXT EXECUTE WITH DATA \_ \_ \_ \_ \_ TO \_** READ.

## <a name="command-category"></a>Categoria

**WPD \_ CATEGORY \_ MTP \_ EXT \_ VENDOR \_ OPERATIONS**

## <a name="parameters"></a>Parametri

Per il driver sono previsti i parametri seguenti.



| Parametro                                                   | VarType             | Descrizione                                                                            |
|-------------------------------------------------------------|---------------------|----------------------------------------------------------------------------------------|
| **CONTESTO DI TRASFERIMENTO \_ \_ MTP \_ EXT \_ DELLA PROPRIETÀ \_ WPD**              | VT \_ LPWSTR          | Obbligatorio. Identifica il contesto restituito dalla chiamata precedente al dispositivo. |
| **LA PROPRIETÀ WPD \_ \_ MTP \_ EXT \_ TRASFERISCE \_ I BYTE NUM \_ DA \_ \_ LEGGERE** | VT \_ UI4             | Obbligatorio. Specifica il numero di byte da leggere.                                       |
| **PROPRIETÀ WPD \_ \_ MTP \_ EXT \_ TRANSFER \_ DATA**                 | VT \_ VECTOR \| VT \_ UI1 | Obbligatorio. Identifica il buffer in cui vengono copiati i dati del dispositivo.                  |



 

## <a name="return-value"></a>Valore restituito

Il driver restituisce i risultati seguenti.



| Risultato                                                  | VarType             | Descrizione                                                       |
|---------------------------------------------------------|---------------------|-------------------------------------------------------------------|
| **PROPRIETÀ WPD \_ \_ MTP \_ EXT \_ TRANSFER NUM \_ BYTES \_ \_ READ** | VT \_ UI4             | Obbligatorio. Specifica il numero di byte ricevuti dal dispositivo. |
| **PROPRIETÀ WPD \_ \_ MTP \_ EXT \_ TRANSFER \_ DATA**             | VT \_ VECTOR \| VT \_ UI1 | Obbligatorio. Buffer che contiene i dati del dispositivo.               |



 

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

 

 





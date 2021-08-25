---
description: Il comando WPD \_ COMMAND \_ MTP \_ EXT \_ GET SUPPORTED \_ \_ VENDOR \_ OPCODES invia un blocco di comandi MTP. A questo comando non è associata alcuna fase dati successiva.
ms.assetid: 397ae29c-f81c-410e-9670-db69c099a321
title: WPD_COMMAND_MTP_EXT_GET_SUPPORTED_VENDOR_OPCODES comando (WpdMtpExtensions.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45b0ab00fc3ada963e56dced49f97d3c1dbca578dfc5c1cded4735f9df947ff1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119927971"
---
# <a name="wpd_command_mtp_ext_get_supported_vendor_opcodes-command"></a>COMANDO WPD \_ \_ MTP \_ EXT \_ GET SUPPORTED \_ VENDOR \_ \_ OPCODES COMMAND

Il **comando WPD \_ COMMAND \_ MTP \_ EXT GET SUPPORTED VENDOR \_ \_ \_ \_ OPCODES** invia un blocco di comandi MTP. A questo comando non è associata alcuna fase dati successiva.

## <a name="command-category"></a>Categoria

**WPD \_ CATEGORY \_ MTP \_ EXT \_ VENDOR \_ OPERATIONS**

## <a name="parameters"></a>Parametri

Questo comando non ha parametri.

## <a name="return-value"></a>Valore restituito

Il driver restituisce i risultati seguenti.



| Risultato                                                | VarType | Descrizione                                                                                              |
|-------------------------------------------------------|---------|----------------------------------------------------------------------------------------------------------|
| **CODICI DI OPERAZIONE \_ DEL FORNITORE \_ MTP \_ EXT DELLA \_ \_ PROPRIETÀ \_ WPD** | VT \_ UI4 | Obbligatorio. Oggetto **IPortableDevicePropVariantCollection** che contiene tutti i codici di operazione estesi dal fornitore. |



 

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

 

 





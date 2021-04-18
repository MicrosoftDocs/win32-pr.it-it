---
description: Il comando WPD \_ comando \_ MTP \_ ext \_ get \_ supported \_ Vendor \_ OpCodes Invia un blocco di comandi MTP. A questo comando non è associata alcuna fase di dati successiva.
ms.assetid: 397ae29c-f81c-410e-9670-db69c099a321
title: Comando WPD_COMMAND_MTP_EXT_GET_SUPPORTED_VENDOR_OPCODES (WpdMtpExtensions. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8713c739da98c179ecc2b7bf042905e4fd06ad7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330575"
---
# <a name="wpd_command_mtp_ext_get_supported_vendor_opcodes-command"></a>\_Comando WPD \_ MTP \_ ext \_ get \_ supported \_ Vendor \_ OpCodes

Il comando **WPD \_ comando \_ MTP \_ ext \_ get \_ supported \_ Vendor \_ OpCodes** Invia un blocco di comandi MTP. A questo comando non è associata alcuna fase di dati successiva.

## <a name="command-category"></a>Categoria

**WPD \_ categoria \_ MTP \_ \_ operazioni fornitore \_ ext**

## <a name="parameters"></a>Parametri

Questo comando non ha parametri.

## <a name="return-value"></a>Valore restituito

Il driver restituisce i risultati seguenti.



| Risultato                                                | VarType | Descrizione                                                                                              |
|-------------------------------------------------------|---------|----------------------------------------------------------------------------------------------------------|
| **WPD \_ proprietà \_ MTP \_ \_ \_ codici operazione fornitore \_ ext** | \_UI4 VT | Obbligatorio. Oggetto **IPortableDevicePropVariantCollection** che contiene tutti i codici operativi estesi del fornitore. |



 

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

 

 





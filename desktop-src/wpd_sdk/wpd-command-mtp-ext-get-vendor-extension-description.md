---
description: Il \_ comando WPD comando \_ MTP \_ ext \_ get \_ Vendor \_ Extension \_ Description recupera la stringa di descrizione Vendor-Extension. Questa stringa è definita da un set di dati DeviceInfo.
ms.assetid: 3741fc97-bbe6-41f0-9c0f-fb2f22225fa3
title: Comando WPD_COMMAND_MTP_EXT_GET_VENDOR_EXTENSION_DESCRIPTION (WpdMtpExtensions. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e1b98d5b8bce699537bc261e915d8233be6082c8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330569"
---
# <a name="wpd_command_mtp_ext_get_vendor_extension_description-command"></a>\_Comando WPD \_ MTP \_ ext \_ get \_ Vendor \_ Extension \_ Description

Il comando **WPD \_ comando \_ MTP \_ ext \_ get \_ Vendor \_ Extension \_ Description** recupera la stringa di descrizione Vendor-Extension. Questa stringa è definita da un set di dati **deviceInfo** .

## <a name="command-category"></a>Categoria

**WPD \_ categoria \_ MTP \_ \_ operazioni fornitore \_ ext**

## <a name="parameters"></a>Parametri

Questo comando non ha parametri.

## <a name="return-value"></a>Valore restituito

Il driver restituisce i risultati seguenti.



| Risultato                                                      | VarType    | Descrizione                                                  |
|-------------------------------------------------------------|------------|--------------------------------------------------------------|
| **\_Proprietà WPD \_ \_ \_ \_ Descrizione estensione fornitore ext \_** | \_LPWSTR VT | Obbligatorio. Specifica la stringa di descrizione dell'estensione del fornitore. |



 

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

 

 





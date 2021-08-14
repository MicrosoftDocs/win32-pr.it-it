---
description: Il comando WPD \_ COMMAND \_ MTP EXT GET VENDOR EXTENSION DESCRIPTION recupera la stringa di descrizione \_ \_ \_ \_ \_ dell'estensione del fornitore. Questa stringa è definita da un set di dati DeviceInfo.
ms.assetid: 3741fc97-bbe6-41f0-9c0f-fb2f22225fa3
title: WPD_COMMAND_MTP_EXT_GET_VENDOR_EXTENSION_DESCRIPTION comando (WpdMtpExtensions.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 31622676161065ec685640789bc51eef64165542a9ebe4c9367ea1a03195e7cc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118193511"
---
# <a name="wpd_command_mtp_ext_get_vendor_extension_description-command"></a>Comando WPD \_ \_ MTP \_ EXT \_ GET VENDOR EXTENSION DESCRIPTION \_ \_ \_ Comando

Il **comando WPD \_ COMMAND \_ MTP \_ EXT GET VENDOR EXTENSION \_ \_ \_ \_ DESCRIPTION** recupera la stringa di descrizione dell'estensione del fornitore. Questa stringa è definita da un set **di dati DeviceInfo.**

## <a name="command-category"></a>Categoria

**OPERAZIONI DEL FORNITORE EXT DELLA CATEGORIA \_ \_ WPD MTP \_ \_ \_**

## <a name="parameters"></a>Parametri

Questo comando non ha parametri.

## <a name="return-value"></a>Valore restituito

Il driver restituisce i risultati seguenti.



| Risultato                                                      | VarType    | Descrizione                                                  |
|-------------------------------------------------------------|------------|--------------------------------------------------------------|
| **DESCRIZIONE DELL'ESTENSIONE DEL FORNITORE \_ \_ \_ MTP EXT \_ \_ DELLA \_ PROPRIETÀ WPD** | VT \_ LPWSTR | Obbligatorio. Specifica la stringa di descrizione dell'estensione del fornitore. |



 

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

 

 





---
description: Il \_ comando WPD comando \_ MTP \_ ext \_ End \_ data \_ Transfer completa un trasferimento dati e una risposta di lettura dal dispositivo.
ms.assetid: df2da2e6-ed5a-41a1-be30-844c0d6b409b
title: Comando WPD_COMMAND_MTP_EXT_END_DATA_TRANSFER (WpdMtpExtensions. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f13f451c477d5f0003bf34f485407157d527aa7f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331685"
---
# <a name="wpd_command_mtp_ext_end_data_transfer-command"></a>\_Comando WPD comando \_ MTP \_ ext \_ End \_ data \_ Transfer

Il comando **WPD \_ comando \_ MTP \_ ext \_ End \_ data \_ Transfer** completa un trasferimento dati e una risposta di lettura dal dispositivo. Il trasferimento viene avviato tramite il comando [**WPD \_ comando \_ MTP \_ ext \_ Execute \_ \_ con \_ dati \_ da \_ leggere**](/windows/desktop/wpd_sdk/wpd-command-mtp-ext-execute-command-with-data-to-read) oppure il comando [**WPD \_ comando \_ MTP \_ ext \_ Execute \_ \_ con \_ dati \_ da \_ scrivere**](/windows/desktop/wpd_sdk/wpd-command-mtp-ext-execute-command-with-data-to-write) comando.

## <a name="command-category"></a>Categoria

**WPD \_ categoria \_ MTP \_ \_ operazioni fornitore \_ ext**

## <a name="parameters"></a>Parametri

Per il driver sono previsti i parametri seguenti.



| Parametro                                      | VarType    | Descrizione                                                                  |
|------------------------------------------------|------------|------------------------------------------------------------------------------|
| **Proprietà WPD del \_ \_ \_ contesto di trasferimento MTP ext \_ \_** | \_LPWSTR VT | Obbligatorio. Identifica il contesto restituito da una chiamata al metodo precedente. |



 

## <a name="return-value"></a>Valore restituito

Il driver restituisce i risultati seguenti.



| Risultato                                        | VarType | Descrizione                                                                                                                             |
|-----------------------------------------------|---------|-----------------------------------------------------------------------------------------------------------------------------------------|
| **\_Proprietà WPD \_ \_ codice di \_ risposta MTP ext \_**   | \_UI4 VT | Obbligatorio. il codice di risposta per il codice operativo del fornitore.                                                                                |
| **\_Proprietà WPD \_ \_ parametri di \_ risposta MTP ext \_** | \_UI4 VT | facoltativo. Raccolta **IPortableDevicePropVariantCollection** che identifica eventuali parametri di risposta. Questa raccolta può essere vuota. |



 

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

 


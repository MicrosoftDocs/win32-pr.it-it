---
description: Il comando WPD \_ comando \_ MTP \_ ext \_ Execute \_ \_ con \_ dati \_ da \_ scrivere comando Invia un blocco di comandi MTP, seguito da una fase di dati. I dati vengono inviati dall'host al dispositivo.
ms.assetid: b675fc3c-4d50-429d-9e00-42160d409a2b
title: Comando WPD_COMMAND_MTP_EXT_EXECUTE_COMMAND_WITH_DATA_TO_WRITE (WpdMtpExtensions. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6f7c65cad838ded52471b5e0dd8dfad325fb1ea
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330579"
---
# <a name="wpd_command_mtp_ext_execute_command_with_data_to_write-command"></a>Comando WPD \_ comando \_ MTP \_ ext \_ Execute \_ \_ con \_ dati \_ da \_ scrivere comando

Il comando **WPD \_ comando \_ MTP \_ ext \_ Execute \_ \_ con \_ dati \_ da \_ scrivere** comando Invia un blocco di comandi MTP, seguito da una fase di dati. I dati vengono inviati dall'host al dispositivo.

## <a name="command-category"></a>Categoria

**WPD \_ categoria \_ MTP \_ \_ operazioni fornitore \_ ext**

## <a name="parameters"></a>Parametri

Per il driver sono previsti i parametri seguenti.



| Parametro                                                | VarType | Descrizione                                                                                                                             |
|----------------------------------------------------------|---------|-----------------------------------------------------------------------------------------------------------------------------------------|
| **\_Proprietà WPD \_ \_ \_ codice operativo MTP \_ ext**             | \_UI4 VT | Obbligatorio. Identifica un codice operativo MTP esteso dal fornitore.                                                                              |
| **\_Proprietà WPD \_ - \_ \_ parametri operazione MTP ext \_**           | \_UI4 VT | Obbligatorio. Raccolta **IPortableDevicePropVariantCollection** che identifica i parametri obbligatori per il codice operativo del fornitore. |
| **\_Proprietà WPD \_ MTP \_ \_ trasferimento \_ dati totali- \_ \_ dimensioni dati** | \_UI8 VT | Obbligatorio. specifica le dimensioni totali dei dati, in byte, esclusi gli overhead, da inviare al dispositivo.                                         |



 

## <a name="return-value"></a>Valore restituito

Il driver restituisce i risultati seguenti.



| Risultato                                                       | VarType    | Descrizione                                                                        |
|--------------------------------------------------------------|------------|------------------------------------------------------------------------------------|
| **\_Proprietà WPD \_ MTP \_ ext \_ Optimal \_ Transfer \_ buffer \_ size** | \_UI4 VT    | Obbligatorio. Specifica la dimensione ottimale del buffer di trasferimento.                       |
| **Proprietà WPD del \_ \_ \_ contesto di trasferimento MTP ext \_ \_**               | \_LPWSTR VT | facoltativo. Identificatore di contesto utilizzato dal driver per i trasferimenti di dati successivi. |



 

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

 

 





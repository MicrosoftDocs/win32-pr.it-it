---
description: Il comando WPD \_ comando \_ MTP \_ ext \_ Execute \_ \_ con \_ dati \_ da \_ leggere comando Invia un blocco di comandi MTP, che verrà seguito da una fase di dati. I dati vengono inviati dal dispositivo all'host.
ms.assetid: 7a76a601-c051-4c0c-bfeb-24e9dddcb9e0
title: Comando WPD_COMMAND_MTP_EXT_EXECUTE_COMMAND_WITH_DATA_TO_READ (WpdMtpExtensions. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a9be0668f0adc312a63702c570c8818e61ba8f5b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330580"
---
# <a name="wpd_command_mtp_ext_execute_command_with_data_to_read-command"></a>Comando WPD \_ comando \_ MTP \_ ext \_ Execute \_ \_ con \_ dati \_ da \_ leggere comando

Il comando **WPD \_ comando \_ MTP \_ ext \_ Execute \_ \_ con \_ dati \_ da \_ leggere** comando Invia un blocco di comandi MTP, che verrà seguito da una fase di dati. I dati vengono inviati dal dispositivo all'host.

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



| Risultato                                                       | VarType    | Descrizione                                                                                                                                                                                                                         |
|--------------------------------------------------------------|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **\_Proprietà WPD \_ MTP \_ \_ trasferimento \_ dati totali- \_ \_ dimensioni dati**     | \_UI8 VT    | Obbligatorio. Restituisce la dimensione totale dei dati, in byte, esclusi gli overhead provenienti dal dispositivo. Se il dispositivo segnala un valore sconosciuto DataSize (0xFFFFFFFF), il driver chiamerà ripetutamente **ReadData** fino a quando non viene ricevuto un breve blocco |
| **\_Proprietà WPD \_ MTP \_ ext \_ Optimal \_ Transfer \_ buffer \_ size** | \_UI4 VT    | facoltativo. Restituisce la dimensione ottimale del buffer di trasferimento.                                                                                                                                                                          |
| **Proprietà WPD del \_ \_ \_ contesto di trasferimento MTP ext \_ \_**               | \_LPWSTR VT | Obbligatorio. Specifica l'identificatore di contesto per i trasferimenti di dati successivi.                                                                                                                                                           |



 

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

 

 





---
description: Il comando \_ \_ SMS \_ Send di WPD avvia l'invio di un messaggio SMS (Short Message Service) da un oggetto funzionale SMS.
ms.assetid: 507d3237-f2dd-499c-85e4-3c6857a15f6f
title: Comando WPD_COMMAND_SMS_SEND (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_COMMAND_SMS_SEND
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 2378ae2b17102fc2bbee568b7f5baa82da554bbd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325940"
---
# <a name="wpd_command_sms_send-command"></a>\_Comando di \_ invio SMS di comando WPD \_

Il **comando \_ \_ SMS \_ Send di WPD** avvia l'invio di un messaggio SMS (Short Message Service) da un oggetto funzionale SMS.

## <a name="command-category"></a>Categoria

**\_SMS della categoria WPD \_**

## <a name="parameters"></a>Parametri

Per il driver sono previsti i parametri seguenti.



| Parametro                              | VarType             | Descrizione                                                                                                                                                                                                                          |
|----------------------------------------|---------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_ \_ \_ destinazione comando comune della proprietà WPD \_ | \_LPWSTR VT          | Obbligatorio. ID oggetto dell'oggetto funzionale SMS che deve inviare il messaggio. Diversi oggetti funzionali SMS possono avere impostazioni diverse.                                                                                     |
| \_ \_ destinatario SMS della proprietà WPD \_          | \_LPWSTR VT          | Obbligatorio. URI del destinatario.                                                                                                                                                                                                  |
| \_tipo di \_ \_ messaggio SMS della proprietà \_ WPD      | \_UI4 VT             | Obbligatorio. Enumeratore dei [**\_ \_ tipi di messaggio SMS**](sms-message-types.md) che indica il tipo di messaggio (testo o binario).                                                                                                        |
| \_messaggio di \_ \_ testo SMS della proprietà \_ WPD      | \_LPWSTR VT          | facoltativo. Se **il \_ \_ tipo di \_ messaggio \_ SMS della proprietà WPD** indica un messaggio di testo, si tratta della stringa del messaggio; in caso contrario, questo parametro non è incluso.                                                                                  |
| \_ \_ \_ messaggio binario SMS proprietà \_ WPD    | VT \_ vettore \| VT \_ UI1 | facoltativo. Se **il \_ \_ tipo di \_ messaggio \_ SMS della proprietà WPD** indica un messaggio binario, si tratta di un puntatore a una matrice di byte. in caso contrario, questo parametro non è incluso. Il primo valore DWORD del valore è la lunghezza della matrice in byte. |



 

## <a name="return-value"></a>Valore restituito

Il driver dovrebbe restituire i risultati seguenti.



| Risultato                                         | VarType   | Descrizione                                                                                                                                                                                                                                                                                                                                                                            |
|------------------------------------------------|-----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **\_ \_ HRESULT comune della proprietà WPD \_**             | \_errore VT | Obbligatorio. **HRESULT** che indica l'esito positivo o negativo dell'esecuzione del comando. Se il chiamante sta effettuando una richiesta non valida, il driver deve restituire **HRESULT \_ da \_ Win32 (errore \_ non \_ supportato)** e non è necessario per restituire altri valori di risultato. I codici di errore includono i [codici di errore dei dispositivi portatili Windows](error-constants.md) o altri codici di errore appropriati. |
| **\_codice di \_ \_ errore del driver comune della proprietà \_ WPD \_** | \_UI4 VT   | facoltativo. Codice di errore specifico del driver. Questa operazione viene in genere usata solo per i test di driver o se il driver, il dispositivo e il client sono tutti progettati insieme.                                                                                                                                                                                                                                |



 

## <a name="calling-methods"></a>Chiamata di metodi

Può essere chiamato solo direttamente usando [**IPortableDevice:: SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>PortableDevice. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Comandi**](commands.md)
</dt> </dl>

 

 





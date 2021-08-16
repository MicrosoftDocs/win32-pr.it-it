---
description: Il comando WPD COMMAND COMMON RESET DEVICE (REIMPOSTA DISPOSITIVO COMUNE WPD) \_ \_ reimposta il \_ \_ dispositivo. Questo non significa riformattazione. equivale a spegnere e accendere di nuovo il dispositivo.
ms.assetid: 7a630cc9-02ea-46be-9645-8a0306606139
title: WPD_COMMAND_COMMON_RESET_DEVICE comando (PortableDevice.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_COMMAND_COMMON_RESET_DEVICE
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: b6a492b7017b8ace6c9118c2f08a1761d7785277fb497474d3e9f39aad60ae8b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119083374"
---
# <a name="wpd_command_common_reset_device-command"></a>COMANDO WPD \_ \_ COMANDO COMUNE RESET \_ \_ DEVICE

Il **comando WPD \_ COMMAND COMMON RESET DEVICE \_ \_ \_ (REIMPOSTA DISPOSITIVO COMUNE WPD)** reimposta il dispositivo. Questo non significa riformattazione. equivale a spegnere e accendere di nuovo il dispositivo.

## <a name="command-category"></a>Categoria

**WPD \_ CATEGORY \_ COMMON**

## <a name="parameters"></a>Parametri

Questo comando non ha parametri.

## <a name="return-value"></a>Valore restituito

Il driver dovrebbe restituire i risultati seguenti.



| Risultato                                         | VarType   | Descrizione                                                                                                                                                                                                                                                                                                                                                                            |
|------------------------------------------------|-----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **HRESULT COMUNE \_ \_ DELLA PROPRIETÀ \_ WPD**             | ERRORE \_ VT | Obbligatorio. HRESULT **che** indica l'esito positivo o negativo dell'esecuzione del comando. Se il chiamante effettua una richiesta non valida, il driver deve restituire **HRESULT \_ FROM \_ WIN32(ERROR \_ NOT \_ SUPPORTED)** e non è necessario per restituire altri valori di risultato. I codici di errore [Windows codici di errore di Dispositivi portatili](error-constants.md) o qualsiasi altro codice di errore appropriato. |
| **CODICE DI ERRORE \_ DEL DRIVER COMUNE DELLE \_ \_ \_ PROPRIETÀ \_ WPD** | VT \_ UI4   | facoltativo. Codice di errore specifico del driver. Viene in genere usato solo per i test dei driver o se il driver, il dispositivo e il client sono tutti progettati insieme.                                                                                                                                                                                                                                |



 

## <a name="calling-methods"></a>Chiamata di metodi

Può essere chiamato direttamente solo usando [**IPortableDevice::SendCommand.**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>PortableDevice.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Comandi**](commands.md)
</dt> </dl>

 

 





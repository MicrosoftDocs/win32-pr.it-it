---
description: Il \_ comando WPD \_ Common \_ Reset \_ Device Reimposta il dispositivo. Questa operazione non significa riformattazione; equivale a spegnere e riaccendere il dispositivo.
ms.assetid: 7a630cc9-02ea-46be-9645-8a0306606139
title: Comando WPD_COMMAND_COMMON_RESET_DEVICE (PortableDevice. h)
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
ms.openlocfilehash: e7ea3fd0088d4997b233670c8ec10bfb16928cb6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333736"
---
# <a name="wpd_command_common_reset_device-command"></a>\_Comando WPD \_ Common \_ Reset \_ Device comando

Il **comando \_ WPD \_ Common \_ Reset \_ Device Reimposta** il dispositivo. Questa operazione non significa riformattazione; equivale a spegnere e riaccendere il dispositivo.

## <a name="command-category"></a>Categoria

**\_categoria WPD \_ comune**

## <a name="parameters"></a>Parametri

Questo comando non ha parametri.

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

 

 





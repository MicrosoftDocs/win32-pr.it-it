---
description: Il \_ comando WPD Command \_ storage \_ format formatta un oggetto funzionale di archiviazione nel dispositivo.
ms.assetid: 5dc06ed3-791f-4c6b-9fb3-42452e948e0d
title: Comando WPD_COMMAND_STORAGE_FORMAT (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_COMMAND_STORAGE_FORMAT
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 763323a8c2a66319ab84636a5d7b2d46a6edb37d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330562"
---
# <a name="wpd_command_storage_format-command"></a>\_Comando WPD Command \_ storage \_ Format

Il comando **WPD \_ Command \_ storage \_ Format** formatta un oggetto funzionale di archiviazione nel dispositivo.

## <a name="command-category"></a>Categoria

**\_archiviazione categoria \_ WPD**

## <a name="parameters"></a>Parametri

Per il driver sono previsti i parametri seguenti.



| Parametro                          | VarType    | Descrizione                                              |
|------------------------------------|------------|----------------------------------------------------------|
| \_ \_ ID oggetto di archiviazione proprietà \_ WPD \_ | \_LPWSTR VT | Obbligatorio. ID oggetto del supporto di archiviazione da formattare. |



 

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

 

 





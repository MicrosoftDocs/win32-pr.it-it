---
description: Il comando WPD \_ COMMAND STORAGE EJECT espelle un supporto di archiviazione che può essere espulso in \_ \_ remoto dal computer.
ms.assetid: 38d4dd56-e898-4890-8328-eb2b03cdbd12
title: WPD_COMMAND_STORAGE_EJECT comando (PortableDevice.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_COMMAND_STORAGE_EJECT
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 2a35b376ed9688217edfde03c76aed962d3e5fb74dc3d8bb7cc927ef1f621c9b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119839011"
---
# <a name="wpd_command_storage_eject-command"></a>Comando WPD \_ \_ COMMAND STORAGE \_ EJECT

Il **comando WPD \_ COMMAND STORAGE \_ \_ EJECT** espelle un supporto di archiviazione che può essere espulso in remoto dal computer.

## <a name="command-category"></a>Categoria

**ARCHIVIAZIONE DI CATEGORIE WPD \_ \_**

## <a name="parameters"></a>Parametri

Per il driver sono previsti i parametri seguenti.



| Parametro                          | VarType    | Descrizione                                             |
|------------------------------------|------------|---------------------------------------------------------|
| ID OGGETTO DI \_ \_ ARCHIVIAZIONE PROPRIETÀ \_ WPD \_ | VT \_ LPWSTR | Obbligatorio. ID oggetto dell'oggetto di archiviazione da espulso. |



 

## <a name="return-value"></a>Valore restituito

Il driver dovrebbe restituire i risultati seguenti.



| Risultato                                         | VarType   | Descrizione                                                                                                                                                                                                                                                                                                                                                                            |
|------------------------------------------------|-----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **HRESULT COMUNE \_ DELLA \_ PROPRIETÀ WPD \_**             | ERRORE \_ VT | Obbligatorio. HRESULT **che** indica l'esito positivo o negativo dell'esecuzione del comando. Se il chiamante effettua una richiesta non valida, il driver deve restituire **HRESULT \_ FROM \_ WIN32(ERROR \_ NOT \_ SUPPORTED)** e non deve restituire altri valori di risultato. I codici di errore [Windows codici di errore di Dispositivi portatili](error-constants.md) o qualsiasi altro codice di errore appropriato. |
| **CODICE DI ERRORE COMUNE \_ \_ DEL DRIVER DELLA \_ \_ PROPRIETÀ \_ WPD** | Interfaccia utente \_ VT4   | facoltativo. Codice di errore specifico del driver. Viene in genere usato solo per i test dei driver o se il driver, il dispositivo e il client sono tutti progettati insieme.                                                                                                                                                                                                                                |



 

## <a name="calling-methods"></a>Chiamata di metodi

Può essere chiamato direttamente solo usando [**IPortableDevice::SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>PortableDevice.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Comandi**](commands.md)
</dt> </dl>

 

 





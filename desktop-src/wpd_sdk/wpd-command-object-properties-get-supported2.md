---
description: Recupera le proprietà supportate da un oggetto .
ms.assetid: 842bd4d6-0824-4597-bb5d-9ef8769055fb
title: WPD_COMMAND_OBJECT_PROPERTIES_GET_SUPPORTED comando (PortableDevice.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_COMMAND_OBJECT_PROPERTIES_GET_SUPPORTED
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 5020494658f380abc465a9059544131174edc8c417f69f6322636e6c9d4170d2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119703981"
---
# <a name="wpd_command_object_properties_get_supported-command"></a>COMANDO GET \_ SUPPORTED PROPERTIES \_ \_ \_ DELL'OGGETTO \_ COMANDO WPD

Il **comando WPD \_ COMMAND OBJECT PROPERTIES GET \_ \_ \_ \_ SUPPORTED** recupera le proprietà supportate da un oggetto.

## <a name="command-category"></a>Categoria di comandi

**PROPRIETÀ DELL'OGGETTO CATEGORIA WPD \_ \_ \_**

## <a name="parameters"></a>Parametri

Il driver prevede il parametro seguente.



| Parametro                                         | VarType        | Descrizione                                                            |
|---------------------------------------------------|----------------|------------------------------------------------------------------------|
| **ID OGGETTO PROPRIETÀ OGGETTO PROPRIETÀ WPD \_ \_ \_ \_ \_** | **VT \_ LPWSTR** | Obbligatorio. ID dell'oggetto che contiene le proprietà richieste. |



 

## <a name="return-value"></a>Valore restituito

Il driver dovrebbe restituire i risultati seguenti.



| Risultato                                                | VarType         | Descrizione                                                                                                                                                                                                                                                                                                                                            |
|-------------------------------------------------------|-----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **CHIAVI DI PROPRIETÀ \_ \_ DELL'OGGETTO \_ PROPRIETÀ \_ \_ WPD** | **VT \_ UNKNOWN** | Obbligatorio. Interfaccia [**IPortableDeviceKeyCollection**](iportabledevicekeycollection.md) che specifica tutte le proprietà supportate.                                                                                                                                                                                                            |
| **HRESULT COMUNE \_ DELLA \_ PROPRIETÀ WPD \_**                    | **ERRORE \_ VT**   | Obbligatorio. Valore **HRESULT** che indica l'esito positivo o negativo complessivo. I possibili valori di risultato [includono Windows di errore di Dispositivi portatili](error-constants.md). Se il chiamante effettua una richiesta non valida, il driver deve restituire **HRESULT \_ FROM \_ WIN32(ERROR \_ NOT \_ SUPPORTED),** ma in caso contrario non è necessario per restituire qualsiasi altro valore di risultato. |
| **CODICE DI ERRORE COMUNE \_ \_ DEL DRIVER DELLA \_ \_ PROPRIETÀ \_ WPD**        | **Interfaccia utente \_ VT4**     | facoltativo. Codice di errore specifico del driver. Viene in genere usato solo per il test del driver o se il driver, il dispositivo e il client sono tutti progettati insieme.                                                                                                                                                                                                |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>PortableDevice.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Comandi**](commands.md)
</dt> </dl>

 

 





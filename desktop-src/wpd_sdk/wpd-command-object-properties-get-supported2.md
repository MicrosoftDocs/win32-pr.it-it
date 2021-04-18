---
description: Recupera le proprietà supportate da un oggetto.
ms.assetid: 842bd4d6-0824-4597-bb5d-9ef8769055fb
title: Comando WPD_COMMAND_OBJECT_PROPERTIES_GET_SUPPORTED (PortableDevice. h)
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
ms.openlocfilehash: bd816e1dc4ce9c3cbb1fb3c0b118004983baea54
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330564"
---
# <a name="wpd_command_object_properties_get_supported-command"></a>\_Comando WPD \_ Proprietà oggetto comando \_ \_ get \_ supported

Il **comando \_ WPD \_ Proprietà oggetto comando \_ \_ get \_ supported** recupera le proprietà supportate da un oggetto.

## <a name="command-category"></a>Categoria comando

**\_proprietà dell' \_ oggetto \_ categoria WPD**

## <a name="parameters"></a>Parametri

Il driver prevede il seguente parametro.



| Parametro                                         | VarType        | Descrizione                                                            |
|---------------------------------------------------|----------------|------------------------------------------------------------------------|
| **\_ \_ \_ \_ ID oggetto proprietà oggetto proprietà \_ WPD** | **\_LPWSTR VT** | Obbligatorio. ID dell'oggetto che contiene le proprietà richieste. |



 

## <a name="return-value"></a>Valore restituito

Il driver dovrebbe restituire i risultati seguenti.



| Risultato                                                | VarType         | Descrizione                                                                                                                                                                                                                                                                                                                                            |
|-------------------------------------------------------|-----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **proprietà \_ \_ oggetto proprietà \_ WPD \_ \_ chiavi proprietà** | **VT \_ sconosciuto** | Obbligatorio. Interfaccia [**IPortableDeviceKeyCollection**](iportabledevicekeycollection.md) che specifica tutte le proprietà supportate.                                                                                                                                                                                                            |
| **\_ \_ HRESULT comune della proprietà WPD \_**                    | **\_errore VT**   | Obbligatorio. Valore **HRESULT** che indica l'esito positivo o negativo complessivo. I possibili valori dei risultati includono i [codici di errore dei dispositivi portatili Windows](error-constants.md). Se il chiamante esegue una richiesta non valida, il driver deve restituire **HRESULT \_ da \_ Win32 (errore \_ non \_ supportato)** , ma in caso contrario non è necessario per restituire altri valori di risultato. |
| **\_codice di \_ \_ errore del driver comune della proprietà \_ WPD \_**        | **\_UI4 VT**     | facoltativo. Codice di errore specifico del driver. Questa operazione viene in genere usata solo per i test di driver o se il driver, il dispositivo e il client sono tutti progettati insieme.                                                                                                                                                                                                |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>PortableDevice. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Comandi**](commands.md)
</dt> </dl>

 

 





---
description: Il comando WPD \_ COMMAND STILL IMAGE CAPTURE INITIATE avvia \_ \_ \_ \_ un'acquisizione di immagini ancorate da un oggetto funzionale dell'immagine. Se viene creato un nuovo oggetto come risultato dell'immagine, il driver deve inviare l'evento WPD \_ EVENT \_ OBJECT \_ ADDED.
ms.assetid: 2968b96e-c9d8-42a7-a32a-dea5fdf064b5
title: WPD_COMMAND_STILL_IMAGE_CAPTURE_INITIATE comando (PortableDevice.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_COMMAND_STILL_IMAGE_CAPTURE_INITIATE
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 5c5490a5af583753f504decacaccf4b4373890fdb7f0e5b099389df29cdc0571
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119806281"
---
# <a name="wpd_command_still_image_capture_initiate-command"></a>Comando WPD \_ COMANDO STILL IMAGE CAPTURE \_ \_ \_ \_ INITIATE

Il **comando WPD \_ COMMAND STILL IMAGE CAPTURE \_ \_ \_ \_ INITIATE** avvia un'acquisizione di immagini ancorate da un oggetto funzionale dell'immagine. Se viene creato un nuovo oggetto come risultato dell'immagine, il driver deve inviare l'evento **WPD \_ EVENT \_ OBJECT \_ ADDED.**

## <a name="command-category"></a>Categoria

**ACQUISIZIONE DI IMMAGINI ANCORA \_ \_ NELLA \_ CATEGORIA \_ WPD**

## <a name="parameters"></a>Parametri

Per il driver sono previsti i parametri seguenti.



| Parametro                              | VarType    | Descrizione                                                                                                                                                                                                                                                                                                                                         |
|----------------------------------------|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| DESTINAZIONE COMANDO COMUNE DELLA PROPRIETÀ WPD \_ \_ \_ \_ | VT \_ LPWSTR | Obbligatorio. ID oggetto dell'oggetto funzionale di acquisizione immagini statiche nel dispositivo che deve acquisire l'immagine. Ogni oggetto funzionale di acquisizione di immagini mobili può avere impostazioni diverse e può fare riferimento a hardware diverso in un dispositivo (ad esempio, una fotocamera anteriore o posteriore di un telefono) e questo parametro indica quale usare.<br/> |



 

## <a name="return-value"></a>Valore restituito

Il driver dovrebbe restituire i risultati seguenti.



| Risultato                                         | VarType   | Descrizione                                                                                                                                                                                                                                                                                                                                                                            |
|------------------------------------------------|-----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **HRESULT COMUNE \_ DELLA \_ PROPRIETÀ WPD \_**             | ERRORE \_ VT | Obbligatorio. HRESULT **che** indica l'esito positivo o negativo dell'esecuzione del comando. Se il chiamante effettua una richiesta non valida, il driver deve restituire **HRESULT \_ FROM \_ WIN32(ERROR \_ NOT \_ SUPPORTED)** e non deve restituire altri valori di risultato. I codici di errore [Windows codici di errore di Dispositivi portatili](error-constants.md) o qualsiasi altro codice di errore appropriato. |
| **CODICE DI ERRORE COMUNE \_ \_ DEL DRIVER DELLA \_ \_ PROPRIETÀ \_ WPD** | Interfaccia utente \_ VT4   | facoltativo. Codice di errore specifico del driver. Questo valore viene in genere usato dai fornitori di dispositivi per migliorare la diagnosi degli errori del dispositivo durante l'uso delle applicazioni. Le applicazioni per utilizzo generico lo ignorano e si basano esclusivamente su \_ \_ HRESULT COMMON WPD \_ PROPERTY.                                                                                                                   |



 

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

 

 





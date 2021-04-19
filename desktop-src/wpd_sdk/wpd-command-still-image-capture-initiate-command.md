---
description: Il comando WPD il comando \_ \_ \_ \_ di avvio dell'acquisizione di immagini continua \_ ad avviare un'acquisizione di immagini ancora da parte di un oggetto funzionale per le immagini. Se viene creato un nuovo oggetto in seguito all'acquisizione di un'immagine, il driver deve inviare l' \_ evento WPD \_ aggiunto all'oggetto evento \_ .
ms.assetid: 2968b96e-c9d8-42a7-a32a-dea5fdf064b5
title: Comando WPD_COMMAND_STILL_IMAGE_CAPTURE_INITIATE (PortableDevice. h)
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
ms.openlocfilehash: c51c2b4a483588389e9986768a2c617e0fd0dd63
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333618"
---
# <a name="wpd_command_still_image_capture_initiate-command"></a>\_Comando di avvio del comando WPD \_ still \_ Image \_ Capture \_

Il comando WPD il comando di **\_ avvio dell' \_ \_ \_ acquisizione \_ di immagini continua** ad avviare un'acquisizione di immagini ancora da parte di un oggetto funzionale per le immagini. Se viene creato un nuovo oggetto in seguito all'acquisizione di un'immagine, il driver deve inviare l' **evento \_ WPD \_ \_ aggiunto all'oggetto evento** .

## <a name="command-category"></a>Categoria

**\_acquisizione di \_ \_ Immagini ancora della categoria \_ WPD**

## <a name="parameters"></a>Parametri

Per il driver sono previsti i parametri seguenti.



| Parametro                              | VarType    | Descrizione                                                                                                                                                                                                                                                                                                                                         |
|----------------------------------------|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_ \_ \_ destinazione comando comune della proprietà WPD \_ | \_LPWSTR VT | Obbligatorio. ID oggetto dell'oggetto funzionale Acquisisci immagine ancora sul dispositivo che dovrebbe scattare l'immagine. Ogni oggetto funzionale Acquisisci immagine può avere impostazioni diverse e può fare riferimento a hardware diverso in un dispositivo (ad esempio, una fotocamera anteriore o posteriore di un telefono) e questo parametro indica quello da usare.<br/> |



 

## <a name="return-value"></a>Valore restituito

Il driver dovrebbe restituire i risultati seguenti.



| Risultato                                         | VarType   | Descrizione                                                                                                                                                                                                                                                                                                                                                                            |
|------------------------------------------------|-----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **\_ \_ HRESULT comune della proprietà WPD \_**             | \_errore VT | Obbligatorio. **HRESULT** che indica l'esito positivo o negativo dell'esecuzione del comando. Se il chiamante sta effettuando una richiesta non valida, il driver deve restituire **HRESULT \_ da \_ Win32 (errore \_ non \_ supportato)** e non è necessario per restituire altri valori di risultato. I codici di errore includono i [codici di errore dei dispositivi portatili Windows](error-constants.md) o altri codici di errore appropriati. |
| **\_codice di \_ \_ errore del driver comune della proprietà \_ WPD \_** | \_UI4 VT   | facoltativo. Codice di errore specifico del driver. Questo valore viene in genere usato dai fornitori di dispositivi per migliorare la diagnosi degli errori del dispositivo durante l'uso delle applicazioni. Le applicazioni per utilizzo generico lo ignorano e si basano invece esclusivamente sulla proprietà WPD, \_ \_ \_ HRESULT comune.                                                                                                                   |



 

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

 

 





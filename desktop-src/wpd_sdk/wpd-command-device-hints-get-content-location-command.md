---
description: Il comando WPD COMMAND DEVICE HINTS GET CONTENT LOCATION recupera gli ID oggetto delle cartelle che possono contenere un oggetto \_ \_ di un tipo \_ \_ \_ \_ specificato.
ms.assetid: 85de64cc-44ee-4536-b658-49d5936351e4
title: WPD_COMMAND_DEVICE_HINTS_GET_CONTENT_LOCATION comando (PortableDevice.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_COMMAND_DEVICE_HINTS_GET_CONTENT_LOCATION
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 7e893df2a67aebcbd271d6df201e7e199b3c3326371e918b02b5c574ebba5763
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118026814"
---
# <a name="wpd_command_device_hints_get_content_location-command"></a>COMANDO WPD \_ COMANDO COMANDO DISPOSITIVO GET CONTENT LOCATION \_ \_ \_ \_ \_ COMANDO

Il **comando WPD \_ COMMAND DEVICE \_ \_ HINTS GET CONTENT \_ \_ \_ LOCATION** recupera gli ID oggetto delle cartelle che possono contenere un oggetto di un tipo specificato. Questo comando viene fornito come modo più rapido per un client per individuare la posizione in cui un dispositivo archivia oggetti specifici rispetto all'enumerazione di oggetti bruti.

## <a name="command-category"></a>Categoria

**HINT DISPOSITIVO CATEGORIA WPD \_ \_ \_**

## <a name="parameters"></a>Parametri

Per il driver sono previsti i parametri seguenti.



| Parametro                                   | VarType   | Descrizione                                                                                                                                                                                                                                                                                                                                     |
|---------------------------------------------|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| TIPO DI CONTENUTO \_ \_ HINT DISPOSITIVO PROPRIETÀ \_ \_ WPD \_ | VT \_ CLSID | Obbligatorio. Tipo di oggetto per cui il chiamante desidera trovare il contenitore. Ad esempio, per trovare le cartelle di primo livello usate per contenere le immagini in una fotocamera digitale, il chiamante invierebbe WPD \_ CONTENT \_ TYPE \_ IMAGE. Vedere [Requisiti per gli oggetti](requirements-for-objects.md) per un elenco dei tipi di oggetto definiti da Windows dispositivi portatili. |



 

## <a name="return-value"></a>Valore restituito

Il driver dovrebbe restituire i risultati seguenti.



| Risultato                                               | VarType     | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|------------------------------------------------------|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **PERCORSI DEL CONTENUTO \_ DEI SUGGERIMENTI DISPOSITIVO PER LE \_ \_ \_ PROPRIETÀ \_ WPD** | VT \_ UNKNOWN | Obbligatorio. [**Oggetto IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) di tipo VT LPWSTR che specifica gli ID oggetto delle cartelle contenenti oggetti del tipo indicato dal parametro \_ chiamante. Se non viene trovata alcuna cartella, deve essere un elenco vuoto. Le cartelle indicate dal risultato possono contenere o meno oggetti di altri tipi di contenuto. Vedere la [proprietà WPD \_ FOLDER CONTENT TYPES \_ \_ \_ ALLOWED](miscellaneous-properties.md) per informazioni sulle restrizioni delle cartelle.<br/> |
| **HRESULT COMUNE \_ \_ DELLA PROPRIETÀ \_ WPD**                   | ERRORE \_ VT   | Obbligatorio. HRESULT **che** indica l'esito positivo o negativo della gestione del comando. Se il chiamante effettua una richiesta non valida, il driver deve restituire **HRESULT \_ FROM \_ WIN32(ERROR \_ NOT \_ SUPPORTED)** e non è necessario per restituire altri valori di risultato. I codici di errore [Windows codici di errore di Dispositivi portatili](error-constants.md) o qualsiasi altro codice di errore appropriato.                                                                                                                                                                            |
| **CODICE DI ERRORE \_ DEL DRIVER COMUNE DELLE \_ \_ \_ PROPRIETÀ \_ WPD**       | VT \_ UI4     | facoltativo. Codice di errore specifico del driver. Viene in genere usato solo per i test dei driver o se il driver, il dispositivo e il client sono tutti progettati insieme.                                                                                                                                                                                                                                                                                                                                                                                                          |



 

## <a name="calling-methods"></a>Chiamata di metodi

Può essere chiamato direttamente solo usando [**IPortableDevice::SendCommand.**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>PortableDevice.h</dt> </dl> |



 

 





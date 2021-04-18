---
description: Il \_ comando WPD comando \_ Device \_ hint \_ get \_ Content \_ percorso recupera gli ID oggetto delle cartelle che possono ospitare un oggetto di un tipo specificato.
ms.assetid: 85de64cc-44ee-4536-b658-49d5936351e4
title: Comando WPD_COMMAND_DEVICE_HINTS_GET_CONTENT_LOCATION (PortableDevice. h)
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
ms.openlocfilehash: 22014925455979a8e84b92f1f641cd839df0b9f1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324805"
---
# <a name="wpd_command_device_hints_get_content_location-command"></a>\_Comando WPD comando per ottenere il \_ \_ \_ \_ percorso del contenuto \_

Il comando **WPD \_ comando \_ Device \_ hint \_ get \_ Content \_ percorso** recupera gli ID oggetto delle cartelle che possono ospitare un oggetto di un tipo specificato. Questo comando viene fornito come modo più rapido per un client di individuare la posizione in cui un dispositivo Archivia oggetti specifici rispetto all'enumerazione di oggetti bruti.

## <a name="command-category"></a>Categoria

**\_hint per \_ dispositivi di categoria WPD \_**

## <a name="parameters"></a>Parametri

Per il driver sono previsti i parametri seguenti.



| Parametro                                   | VarType   | Descrizione                                                                                                                                                                                                                                                                                                                                     |
|---------------------------------------------|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_tipo di \_ \_ contenuto hint \_ del dispositivo della proprietà WPD \_ | \_CLSID VT | Obbligatorio. Il tipo di oggetto per il quale il chiamante desidera trovare il contenitore. Per trovare, ad esempio, le cartelle di primo livello usate per conservare le immagini in una fotocamera digitale, il chiamante invia l' \_ immagine del tipo di contenuto WPD \_ \_ . Vedere [requisiti per gli oggetti](requirements-for-objects.md) per un elenco di tipi di oggetto definiti da dispositivi portatili Windows. |



 

## <a name="return-value"></a>Valore restituito

Il driver dovrebbe restituire i risultati seguenti.



| Risultato                                               | VarType     | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|------------------------------------------------------|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **\_ \_ \_ \_ percorsi contenuto suggerimenti dispositivo proprietà \_ WPD** | VT \_ sconosciuto | Obbligatorio. Un [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) di tipo VT \_ LPWSTR valori che specificano gli ID oggetto delle cartelle contenenti oggetti del tipo indicato dal parametro chiamante. Se non viene trovata alcuna cartella, deve essere un elenco vuoto. Le cartelle indicate dal risultato possono contenere o meno oggetti di altri tipi di contenuto. Per informazioni sulle restrizioni delle cartelle, vedere la proprietà [ \_ tipi di contenuto della cartella WPD \_ \_ \_ consentiti](miscellaneous-properties.md) .<br/> |
| **\_ \_ HRESULT comune della proprietà WPD \_**                   | \_errore VT   | Obbligatorio. **HRESULT** che indica l'esito positivo o negativo della gestione del comando. Se il chiamante sta effettuando una richiesta non valida, il driver deve restituire **HRESULT \_ da \_ Win32 (errore \_ non \_ supportato)** e non è necessario per restituire altri valori di risultato. I codici di errore includono i [codici di errore dei dispositivi portatili Windows](error-constants.md) o altri codici di errore appropriati.                                                                                                                                                                            |
| **\_codice di \_ \_ errore del driver comune della proprietà \_ WPD \_**       | \_UI4 VT     | facoltativo. Codice di errore specifico del driver. Questa operazione viene in genere usata solo per i test di driver o se il driver, il dispositivo e il client sono tutti progettati insieme.                                                                                                                                                                                                                                                                                                                                                                                                          |



 

## <a name="calling-methods"></a>Chiamata di metodi

Può essere chiamato solo direttamente usando [**IPortableDevice:: SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>PortableDevice. h</dt> </dl> |



 

 





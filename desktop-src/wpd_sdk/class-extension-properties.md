---
description: Windows Dispositivi portabili supporta le proprietà di estensione della classe seguenti.
ms.assetid: 9b8983ba-5824-495d-868f-fd22b98e1954
title: Proprietà dell'estensione della classe (PortableDevice.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Class
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 4c7215a383aec582f576cb64a6781068034bb7fa8df03b5a404368482f1c1619
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117843405"
---
# <a name="class-extension-properties"></a>Proprietà dell'estensione della classe

Windows Dispositivi portabili supporta le proprietà di estensione della classe seguenti.



| Proprietà                                                                      | VarType         | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|-------------------------------------------------------------------------------|-----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **OPZIONI DI ESTENSIONE DELLA CLASSE WPD \_ \_ TIPI DI CONTENUTO \_ \_ \_ \_ SUPPORTATI**                 | **VT \_ UNKNOWN** | Valore che specifica l'elenco (superset) dei tipi di contenuto supportati dal driver (simile alla chiamata di WPD \_ COMMAND CAPABILITIES GET SUPPORTED CONTENT TYPES in \_ \_ \_ \_ \_ **WPD \_ FUNCTIONAL CATEGORY \_ \_ ALL).**                                                                                                                                                                                                                                                                                                                                             |
| **LE OPZIONI DI ESTENSIONE DELLA CLASSE WPD \_ \_ NON \_ \_ \_ REGISTRANO \_ L'INTERFACCIA DEL DISPOSITIVO WPD \_ \_**    | **VT \_ BOOL**    | Valore che specifica se il chiamante vuole che la libreria di estensioni di classe WPD registri l'interfaccia della classe di dispositivi WPD. Se questo valore è true, il chiamante si assume la responsabilità della registrazione.<br/> Se questo valore è false, indica che il chiamante si aspetta che la libreria di estensioni di classe eserciti la registrazione.<br/>La maggior parte dei driver deve consentire alla libreria di estensioni di classe di eseguire la registrazione, ad eccezione del caso in cui la registrazione dell'interfaccia WPD Device Class da parte della libreria di estensioni di classe potrebbe causare effetti negativi. |
| **LE OPZIONI DI ESTENSIONE DELLA CLASSE WPD \_ \_ \_ \_ \_ REGISTRANO L'INTERFACCIA DEL DISPOSITIVO PRIVATO WPD \_ \_ \_** | **VT \_ BOOL**    | Indica che il chiamante vuole che la libreria di estensioni di classe WPD registri l'interfaccia della classe di dispositivi WPD privata. Questa operazione non è consigliata per la maggior parte dei driver. Deve essere usato solo nei casi in cui la registrazione dell'interfaccia WPD Device Class dalla libreria di estensioni di classe causerà effetti negativi. Questa opzione viene in genere usata insieme a **WPD \_ CLASS EXTENSION OPTIONS \_ \_ \_ DONT REGISTER \_ \_ WPD \_ DEVICE \_ INTERFACE** impostata su **TRUE**                                                                                          |
| **OPZIONI DI ESTENSIONE DELLA CLASSE WPD \_ VALORI DI IDENTIFICAZIONE DEL \_ \_ \_ \_ \_ DISPOSITIVO**            | **VT \_ UNKNOWN** | Si tratta di [un oggetto IPortableDeviceValues](iportabledevicevalues.md) che contiene i valori di identificazione del dispositivo **(WPD \_ DEVICE \_ MANUFACTURER,** **WPD \_ DEVICE \_ MODEL, WPD DEVICE** FIRMWARE **\_ \_ \_ VERSION** e **WPD \_ DEVICE FUNCTIONAL \_ UNIQUE \_ \_ ID).** Includere questa opzione con altre opzioni di estensione della classe durante l'inizializzazione                                                                                                                                                                                                                               |
| **LARGHEZZA DI BANDA DEL TRASPORTO \_ DELLE OPZIONI DI ESTENSIONE DELLA \_ \_ \_ CLASSE \_ WPD**                      | **VT \_ UI4**     | Indica la larghezza di banda massima teorica del trasporto in kilobit al secondo                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| **OPZIONI DI ESTENSIONE DELLA CLASSE WPD \_ VALORI DI IDENTIFICAZIONE DEL \_ \_ \_ \_ \_ DISPOSITIVO**            | **VT \_ UNKNOWN** | Si tratta di [un oggetto IPortableDeviceValues](iportabledevicevalues.md) che contiene i valori di identificazione del dispositivo **(WPD \_ DEVICE \_ MANUFACTURER,** **WPD \_ DEVICE \_ MODEL, WPD DEVICE** FIRMWARE **\_ \_ \_ VERSION** e **WPD \_ DEVICE FUNCTIONAL \_ UNIQUE \_ \_ ID).** Includere questa opzione con altre opzioni di estensione della classe durante l'inizializzazione.                                                                                                                                                                                                                              |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>PortableDevice.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Proprietà e attributi WPD**](properties-and-attributes.md)
</dt> </dl>

 

 





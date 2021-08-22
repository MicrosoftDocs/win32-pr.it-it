---
description: Windows Dispositivi portatili supporta le proprietà varie seguenti.
ms.assetid: 0f2a5684-a94f-4a51-8f72-527204e4ebfa
title: Proprietà varie (PortableDevice.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Miscellaneous
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: bdc093d877a180f6c7072ff9365e96edfe7d9e2c006fdcb745c58e92df3b179f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119704431"
---
# <a name="miscellaneous-properties"></a>Proprietà varie

Windows Dispositivi portatili supporta le proprietà varie seguenti.



| Proprietà                                       | VarType         | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|------------------------------------------------|-----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **OPZIONE DELL'API WPD \_ USE CLEAR DATA STREAM \_ \_ \_ (USA CLEAR DATA \_ \_ STREAM)** | **VT \_ BOOL**    | Valore booleano che specifica se il flusso di dati creato per il trasferimento dei dati sarà chiaro, ad esempio DRM non è coinvolto. I client possono impostare questa opzione aggiungendola alle proprietà dell'oggetto passate a [**IPortableDeviceContent::CreateObjectWithPropertiesAndData**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecontent-createobjectwithpropertiesanddata).<br/>                                                                                                                                                   |
| **VERSIONE DEL SERVIZIO WPD \_ \_**                      | **VT \_ LPWSTR**  | Stringa che specifica la versione di implementazione di un determinato servizio dispositivo.                                                                                                                                                                                                                                                                                                                                                                                                                        |
| **TIPI DI CONTENUTO DELLA CARTELLA WPD \_ \_ \_ \_ CONSENTITI**       | **VT \_ UNKNOWN** | Valore che specifica i tipi di oggetto che possono essere figli diretti di questa cartella. Le cartelle figlio possono avere funzionalità diverse. Questa proprietà è un [**oggetto IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) che contiene valori CLSID VT \_ che specificano i tipi di oggetto consentiti.<br/> Per un elenco dei tipi di oggetto definiti da Windows dispositivi portatili, vedere [Requisiti per gli oggetti](requirements-for-objects.md).<br/>                                         |
| **CATEGORIA DI OGGETTI FUNZIONALI WPD \_ \_ \_**          | **VT \_ CLSID**   | Valore che specifica la categoria funzionale dell'oggetto.                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| **PROFILI DI INFORMAZIONI SUL RENDERING WPD \_ \_ \_**      | **VT \_ UNKNOWN** | Oggetto [**IPortableDeviceValuesCollection**](iportabledevicevaluescollection.md) che contiene più [**interfacce IPortableDeviceValues,**](iportabledevicevalues.md) ognuna delle quali contiene le impostazioni delle proprietà per un profilo supportate dall'oggetto.                                                                                                                                                                                                                                            |
| **NOME VISUALIZZATO DEL \_ \_ SUGGERIMENTO \_ PER \_ L'OGGETTO WPD \_** | **VT \_ LPWSTR**  | Se un oggetto è una posizione dei suggerimenti, questa proprietà indica il nome specifico del suggerimento da visualizzare all'utente anziché il nome dell'oggetto. I driver possono specificare suggerimenti sulla posizione per vari tipi di oggetto. Si tratta dei percorsi di archiviazione preferiti per le cartelle che contengono un particolare tipo di oggetto. Un equivalente è la cartella Immagini per i file di immagine in Windows. Se questa proprietà non esiste, in genere viene usato [il nome dell'oggetto WPD. \_ \_ ](object-properties.md)<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>PortableDevice.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Proprietà e attributi WPD**](properties-and-attributes.md)
</dt> </dl>

 

 





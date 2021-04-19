---
description: I dispositivi portatili Windows supportano le proprietà varie seguenti.
ms.assetid: 0f2a5684-a94f-4a51-8f72-527204e4ebfa
title: Proprietà varie (PortableDevice. h)
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
ms.openlocfilehash: 6bc5f90bb04c2ee0d018d03ee07b6cd7436e6593
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326292"
---
# <a name="miscellaneous-properties"></a>Proprietà varie

I dispositivi portatili Windows supportano le proprietà varie seguenti.



| Proprietà                                       | VarType         | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|------------------------------------------------|-----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **\_opzione dell'API WPD usare un \_ \_ \_ \_ flusso di dati chiaro \_** | **\_bool VT**    | Valore booleano che specifica se il flusso di dati creato per il trasferimento dei dati sarà chiaro, ovvero se il DRM non è necessario. I client possono impostare questa opzione aggiungendola alle proprietà dell'oggetto passate a [**IPortableDeviceContent:: CreateObjectWithPropertiesAndData**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecontent-createobjectwithpropertiesanddata).<br/>                                                                                                                                                   |
| **\_versione del servizio WPD \_**                      | **\_LPWSTR VT**  | Stringa che specifica la versione di implementazione di un determinato servizio del dispositivo.                                                                                                                                                                                                                                                                                                                                                                                                                        |
| **\_tipi di contenuto della cartella WPD \_ \_ \_ consentiti**       | **VT \_ sconosciuto** | Valore che specifica i tipi di oggetto che possono essere elementi figlio diretti di questa cartella. Le cartelle figlio possono avere diverse funzionalità. Questa proprietà è un [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) che contiene \_ i valori CLSID del VT che specificano i tipi di oggetto consentiti.<br/> Per un elenco di tipi di oggetto definiti da dispositivi portatili Windows, vedere [requisiti per gli oggetti](requirements-for-objects.md).<br/>                                         |
| **\_ \_ categoria oggetto funzionale \_ WPD**          | **\_CLSID VT**   | Valore che specifica la categoria funzionale dell'oggetto.                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| **\_ \_ profili informazioni di rendering WPD \_**      | **VT \_ sconosciuto** | Un [**IPortableDeviceValuesCollection**](iportabledevicevaluescollection.md) che contiene più interfacce [**IPortableDeviceValues**](iportabledevicevalues.md) , ognuna delle quali contiene le impostazioni delle proprietà per un profilo supportato dall'oggetto.                                                                                                                                                                                                                                            |
| **\_ \_ \_ \_ nome visualizzato posizione hint oggetto \_ WPD** | **\_LPWSTR VT**  | Se un oggetto è un percorso di hint, questa proprietà indica il nome specifico dell'hint da visualizzare all'utente anziché il nome dell'oggetto. I driver possono specificare hint di posizione per diversi tipi di oggetto. Si tratta delle posizioni di archiviazione preferite per le cartelle che contengono un particolare tipo di oggetto. Un equivalente è la cartella immagini personali per i file di immagine in Windows. Se questa proprietà non esiste, viene in genere usato il [ \_ \_ nome dell'oggetto WPD](object-properties.md) .<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>PortableDevice. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Proprietà e attributi di WPD**](properties-and-attributes.md)
</dt> </dl>

 

 





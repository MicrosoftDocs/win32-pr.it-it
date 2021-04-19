---
description: I dispositivi portatili Windows supportano le seguenti proprietà di estensione della classe.
ms.assetid: 9b8983ba-5824-495d-868f-fd22b98e1954
title: Proprietà estensione classe (PortableDevice. h)
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
ms.openlocfilehash: c7e961b80ae990653e6c354640b35c28f8bcf8b8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326209"
---
# <a name="class-extension-properties"></a>Proprietà estensione classe

I dispositivi portatili Windows supportano le seguenti proprietà di estensione della classe.



| Proprietà                                                                      | VarType         | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|-------------------------------------------------------------------------------|-----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **\_tipi di \_ \_ \_ contenuto supportati dalle opzioni di \_ estensione \_ della classe WPD**                 | **VT \_ sconosciuto** | Valore che specifica l'elenco (superset) dei tipi di contenuto supportati dal driver (simile alla chiamata delle \_ funzionalità del comando WPD \_ \_ ottenere \_ \_ i tipi di contenuto supportati \_ nella **\_ categoria funzionale WPD \_ \_ tutti**).                                                                                                                                                                                                                                                                                                                                             |
| **le \_ Opzioni di estensione della classe WPD non \_ \_ \_ \_ registrano l' \_ \_ interfaccia del dispositivo WPD \_**    | **\_bool VT**    | Valore che specifica se il chiamante desidera che la libreria di estensioni della classe WPD registri l'interfaccia della classe del dispositivo WPD. Se questo valore è true, il chiamante si assume la responsabilità della registrazione.<br/> Se questo valore è false, indica che il chiamante prevede che la libreria di estensione della classe esegua la registrazione.<br/>La maggior parte dei driver deve consentire alla libreria di estensione della classe di eseguire la registrazione, tranne nel caso in cui la registrazione dell'interfaccia della classe di dispositivi WPD dalla libreria di estensioni della classe possa causare effetti negativi. |
| **\_Opzioni di estensione della classe WPD registrare l' \_ \_ \_ \_ \_ interfaccia del dispositivo privato WPD \_ \_** | **\_bool VT**    | Indica che il chiamante desidera che la libreria di estensioni della classe WPD registri l'interfaccia della classe del dispositivo WPD privata. Questa operazione non è consigliata per la maggior parte dei driver. Deve essere usato solo nei casi in cui la registrazione dell'interfaccia della classe di dispositivi WPD dalla libreria di estensioni della classe provochi effetti negativi. Questa opzione viene in genere usata in combinazione con le **\_ Opzioni di estensione della classe WPD \_ \_ \_ dont \_ Register \_ WPD \_ Device \_ Interface** impostata su **true**                                                                                          |
| **\_Opzioni di estensione della classe WPD \_ \_ \_ valori di identificazione del dispositivo \_ \_**            | **VT \_ sconosciuto** | Si tratta di un [IPortableDeviceValues](iportabledevicevalues.md) che contiene i valori di identificazione del dispositivo (**\_ \_ produttore del dispositivo WPD**, **\_ \_ modello di dispositivo WPD**, **\_ \_ \_ versione del firmware del dispositivo WPD** e **\_ \_ \_ \_ ID univoco funzionale del dispositivo WPD**). Includi questa opzione con altre opzioni di estensione della classe durante l'inizializzazione                                                                                                                                                                                                                               |
| **opzioni di estensione della classe WPD- \_ larghezza di \_ \_ \_ banda del trasporto \_**                      | **\_UI4 VT**     | Indica la larghezza di banda teorica massima del trasporto in kilobit al secondo                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| **\_Opzioni di estensione della classe WPD \_ \_ \_ valori di identificazione del dispositivo \_ \_**            | **VT \_ sconosciuto** | Si tratta di un [IPortableDeviceValues](iportabledevicevalues.md) che contiene i valori di identificazione del dispositivo (**\_ \_ produttore del dispositivo WPD**, **\_ \_ modello di dispositivo WPD**, **\_ \_ \_ versione del firmware del dispositivo WPD** e **\_ \_ \_ \_ ID univoco funzionale del dispositivo WPD**). Includere questa opzione con altre opzioni di estensione della classe durante l'inizializzazione.                                                                                                                                                                                                                              |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>PortableDevice. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Proprietà e attributi di WPD**](properties-and-attributes.md)
</dt> </dl>

 

 





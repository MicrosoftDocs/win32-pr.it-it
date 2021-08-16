---
description: Windows Dispositivi portatili supporta gli attributi di proprietà seguenti.
ms.assetid: 129ee2b8-075c-457a-85ef-658a56eed541
title: Attributi delle proprietà (PortableDevice.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Property
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 85bf37b716349aae164594eeb8085e8c6df9dc5445728bbf7d9222705a9cb8c8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117843564"
---
# <a name="property-attributes-portabledeviceh"></a>Attributi delle proprietà (PortableDevice.h)

Windows Dispositivi portatili supporta gli attributi di proprietà seguenti. Questi attributi vengono restituiti dai metodi seguenti:

-   [**IPortableDeviceCapabilities::GetFixedPropertyAttributes**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecapabilities-getfixedpropertyattributes)
-   [**IPortableDeviceProperties::GetPropertyAttributes**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledeviceproperties-getpropertyattributes)
-   [**IPortableDeviceServiceCapabilities::GetFormatPropertyAttributes**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getformatpropertyattributes)



| Attributo                                           | VarType         | Descrizione                                                                                                                                                                                                                                                                                                                                                                                    |
|-----------------------------------------------------|-----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **L'ATTRIBUTO DELLA PROPRIETÀ WPD \_ \_ PUÒ ESSERE \_ \_ ELIMINATO**           | **VT \_ BOOL**    | Valore booleano che specifica se il client può eliminare la proprietà. Per eliminare una proprietà, impostarne il valore su VT \_ EMPTY.                                                                                                                                                                                                                                                                   |
| **L'ATTRIBUTO DELLA PROPRIETÀ WPD \_ \_ PUÒ \_ \_ LEGGERE**             | **VT \_ BOOL**    | Valore booleano che specifica se il client può leggere la proprietà.                                                                                                                                                                                                                                                                                                                       |
| **L'ATTRIBUTO DELLA PROPRIETÀ WPD \_ \_ PUÒ \_ \_ SCRIVERE**            | **VT \_ BOOL**    | Valore booleano che specifica se il client può modificare la proprietà.                                                                                                                                                                                                                                                                                                                     |
| **VALORE PREDEFINITO \_ \_ DELL'ATTRIBUTO DELLA PROPRIETÀ \_ \_ WPD**        | VT \_ *XXXX*      | Valore definito dal dispositivo che specifica il valore predefinito di una proprietà. Si applica solo alle proprietà scrivibili.                                                                                                                                                                                                                                                               |
| **ELEMENTI DI ENUMERAZIONE DEGLI \_ ATTRIBUTI \_ DELLA PROPRIETÀ \_ \_ WPD** | **VT \_ UNKNOWN** | Interfaccia [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) che contiene una raccolta di valori per una proprietà il cui attributo **WPD \_ PROPERTY ATTRIBUTE \_ \_ FORM** è **WPD \_ PROPERTY ATTRIBUTE FORM \_ \_ \_ ENUMERATION.** Il tipo di dati dipende dalla proprietà su cui viene eseguita la query.                                                                              |
| **ATTRIBUTO DI PROPRIETÀ WPD \_ \_ FAST \_ \_ PROPRIETÀ**        | **VT \_ BOOL**    | Se True, questa proprietà appartiene al gruppo *di proprietà* veloci. Si tratta di proprietà che possono essere recuperate rapidamente dal dispositivo.                                                                                                                                                                                                                                                        |
| **MODULO ATTRIBUTO PROPRIETÀ WPD \_ \_ \_**                  | **Interfaccia utente \_ VT4**     | Valore [**enumerato WpdAttributeForm**](wpdattributeform.md) che specifica il formato dei valori validi consentiti per questa proprietà.                                                                                                                                                                                                                                                         |
| **NOME ATTRIBUTO PROPRIETÀ WPD \_ \_ \_**                  | **VT \_ LPWSTR**  | Stringa che specifica il nome descrittivo dello script della proprietà. I caratteri validi sono alfanumerici \[ a-zA-Z0-9 \] e ' \_ '.                                                                                                                                                                                                                                                                    |
| **INTERVALLO MASSIMO \_ ATTRIBUTI \_ PROPRIETÀ \_ WPD \_**            | VT \_ *XXXX*      | Valore massimo per una proprietà il cui attributo **WPD \_ PROPERTY \_ ATTRIBUTE \_ FORM** è **WPD \_ PROPERTY ATTRIBUTE FORM \_ \_ \_ RANGE.** Il tipo di dati può essere qualsiasi tipo numerico.                                                                                                                                                                                                               |
| **INTERVALLO DI ATTRIBUTI DELLA PROPRIETÀ WPD \_ \_ \_ \_ MIN**            | VT \_ *XXXX*      | Valore minimo per una proprietà il cui attributo **WPD \_ PROPERTY \_ ATTRIBUTE \_ FORM** è **WPD \_ PROPERTY ATTRIBUTE FORM \_ \_ \_ RANGE**. Il tipo di dati può essere qualsiasi tipo numerico.                                                                                                                                                                                                               |
| **PASSAGGIO INTERVALLO \_ ATTRIBUTI \_ PROPRIETÀ \_ WPD \_**           | VT \_ *XXXX*      | Valore del passaggio per una proprietà il cui attributo **WPD \_ PROPERTY \_ ATTRIBUTE \_ FORM** è **WPD \_ PROPERTY ATTRIBUTE FORM \_ \_ \_ RANGE**. Il passaggio specifica in base alla quantità di modifica di una proprietà di intervallo. Ad esempio, una proprietà con un valore minimo di 10, un valore massimo di 20 e un passaggio di 5 può avere i valori seguenti: **10**, **15**, **20**. Il tipo di dati può essere qualsiasi tipo numerico. |
| **ESPRESSIONE REGOLARE \_ DELL'ATTRIBUTO DI PROPRIETÀ \_ WPD \_ \_**   | **VT \_ LPWSTR**  | Stringa di espressione regolare che specifica valori accettabili per le proprietà il cui formato è **WPD \_ PROPERTY ATTRIBUTE FORM REGULAR \_ \_ \_ \_ EXPRESSION**.                                                                                                                                                                                                                                             |
| **VARTYPE \_ \_ DELL'ATTRIBUTO DELLA PROPRIETÀ WPD \_**               | **Interfaccia utente \_ VT4**     | Intero che specifica il VARTYPE della proprietà, ad esempio **VT \_ BOOL.**                                                                                                                                                                                                                                                                                                              |
| **DIMENSIONI MASSIME \_ \_ DELL'ATTRIBUTO DELLA PROPRIETÀ \_ \_ WPD**             | **Interfaccia utente \_ VT8**     | Valore che specifica le dimensioni massime in byte per il valore di questa proprietà.                                                                                                                                                                                                                                                                                                              |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>PortableDevice.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Proprietà**](properties-and-attributes.md)
</dt> </dl>

 

 





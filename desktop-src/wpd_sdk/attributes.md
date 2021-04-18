---
description: I dispositivi portatili Windows supportano gli attributi delle proprietà seguenti.
ms.assetid: 129ee2b8-075c-457a-85ef-658a56eed541
title: Attributi di proprietà (PortableDevice. h)
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
ms.openlocfilehash: 9e48a4f81a6223ed034f6de14fe104a1a2aa4393
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331474"
---
# <a name="property-attributes-portabledeviceh"></a>Attributi di proprietà (PortableDevice. h)

I dispositivi portatili Windows supportano gli attributi delle proprietà seguenti. Questi attributi vengono restituiti dai metodi seguenti:

-   [**IPortableDeviceCapabilities::GetFixedPropertyAttributes**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecapabilities-getfixedpropertyattributes)
-   [**IPortableDeviceProperties::GetPropertyAttributes**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledeviceproperties-getpropertyattributes)
-   [**IPortableDeviceServiceCapabilities::GetFormatPropertyAttributes**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getformatpropertyattributes)



| Attributo                                           | VarType         | Descrizione                                                                                                                                                                                                                                                                                                                                                                                    |
|-----------------------------------------------------|-----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **l' \_ attributo della proprietà WPD \_ \_ può \_ eliminare**           | **\_bool VT**    | Valore booleano che specifica se il client può eliminare la proprietà. Per eliminare una proprietà, impostarne il valore su VT \_ Empty.                                                                                                                                                                                                                                                                   |
| **l'attributo della proprietà WPD è in \_ \_ grado di \_ \_ leggere**             | **\_bool VT**    | Valore booleano che specifica se il client può leggere la proprietà.                                                                                                                                                                                                                                                                                                                       |
| **l' \_ attributo della proprietà WPD \_ \_ può \_ scrivere**            | **\_bool VT**    | Valore booleano che specifica se il client può modificare la proprietà.                                                                                                                                                                                                                                                                                                                     |
| **\_ \_ valore predefinito dell'attributo della proprietà WPD \_ \_**        | VT \_ *xxxx*      | Valore definito dal dispositivo che specifica il valore predefinito di una proprietà. Questo vale solo per le proprietà scrivibili.                                                                                                                                                                                                                                                               |
| **\_elementi di \_ \_ enumerazione \_ degli attributi della proprietà WPD** | **VT \_ sconosciuto** | Interfaccia [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) che contiene una raccolta di valori per una proprietà il cui **attributo \_ \_ \_ form attributo Property WPD** è **WPD \_ Property \_ Attribute \_ form \_ Enumeration**. Il tipo di dati dipende dalla proprietà sottoposta a query.                                                                              |
| **\_ \_ Proprietà rapida dell'attributo della proprietà WPD \_ \_**        | **\_bool VT**    | Se true, questa proprietà appartiene al gruppo di *Proprietà Fast* . Si tratta di proprietà che possono essere recuperate rapidamente dal dispositivo.                                                                                                                                                                                                                                                        |
| **\_form dell' \_ attributo della proprietà WPD \_**                  | **\_UI4 VT**     | Valore enumerato [**WpdAttributeForm**](wpdattributeform.md) che specifica il formato dei valori validi consentiti per questa proprietà.                                                                                                                                                                                                                                                         |
| **\_nome dell' \_ attributo della proprietà WPD \_**                  | **\_LPWSTR VT**  | Stringa che specifica il nome descrittivo per lo script della proprietà. I caratteri validi sono alfanumerici \[ a-Za-z0-9 \] è \_ '.                                                                                                                                                                                                                                                                    |
| **valore \_ \_ \_ massimo intervallo attributi \_ Proprietà WPD**            | VT \_ *xxxx*      | Valore massimo per una proprietà il cui **attributo \_ \_ \_ form** dell'attributo della proprietà WPD è un **intervallo di form dell' \_ attributo della proprietà \_ \_ \_ WPD**. Il tipo di dati può essere uno qualsiasi dei tipi numerici.                                                                                                                                                                                                               |
| **\_ \_ intervallo attributi proprietà \_ WPD \_ min**            | VT \_ *xxxx*      | Valore minimo per una proprietà il cui **attributo \_ \_ \_ form** dell'attributo della proprietà WPD è l' **intervallo di form dell' \_ attributo della proprietà \_ \_ \_ WPD**. Il tipo di dati può essere uno qualsiasi dei tipi numerici.                                                                                                                                                                                                               |
| **\_passaggio dell' \_ intervallo di attributi della proprietà WPD \_ \_**           | VT \_ *xxxx*      | Valore del passaggio per una proprietà il cui attributo **\_ \_ \_ form** dell'attributo della proprietà WPD è un **intervallo di form dell' \_ attributo della proprietà \_ \_ \_ WPD**. Il passaggio specifica la quantità di una proprietà di intervallo che deve essere modificata. Ad esempio, una proprietà con un valore minimo di 10, un valore massimo di 20 e un passaggio di 5 potrebbero avere i valori seguenti: **10**, **15**, **20**. Il tipo di dati può essere uno qualsiasi dei tipi numerici. |
| **\_ \_ \_ espressione regolare attributo proprietà \_ WPD**   | **\_LPWSTR VT**  | Stringa di espressione regolare che specifica i valori accettabili per le proprietà il cui formato è **WPD \_ attributo della proprietà Form \_ \_ \_ \_ espressione regolare**.                                                                                                                                                                                                                                             |
| **\_ \_ VarType attributo proprietà \_ WPD**               | **\_UI4 VT**     | Integer che specifica il VARTYPE della proprietà, ad esempio **VT \_ bool**.                                                                                                                                                                                                                                                                                                              |
| **\_ \_ \_ dimensioni massime attributo proprietà WPD \_**             | **\_UI8 VT**     | Valore che specifica la dimensione massima in byte del valore di questa proprietà.                                                                                                                                                                                                                                                                                                              |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>PortableDevice. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Proprietà**](properties-and-attributes.md)
</dt> </dl>

 

 





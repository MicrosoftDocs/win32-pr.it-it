---
description: Per Windows 7, i dispositivi portatili Windows supportano i seguenti attributi di parametro per i metodi e gli eventi di un servizio dispositivo.
ms.assetid: a7708c60-758a-4fb6-8ef9-074ecdc9cf60
title: Attributi parametro (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Parameter
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 113b2b35a5b6e61cd2cc1d3666d1a13fbade5ec7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324044"
---
# <a name="parameter-attributes"></a>Attributi del parametro

Per Windows 7, i dispositivi portatili Windows supportano i seguenti attributi di parametro per i metodi e gli eventi di un servizio dispositivo. Questi attributi vengono restituiti dai metodi seguenti:

-   [**IPortableDeviceServiceCapabilities::GetMethodParameterAttributes**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getmethodparameterattributes)
-   [**IPortableDeviceServiceCapabilities::GetEventParameterAttributes**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-geteventparameterattributes)




| Attributo                                            | VarType         | Descrizione                                                                                                                                                                                 |
|------------------------------------------------------|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **\_ \_ valore predefinito dell'attributo del parametro WPD \_ \_**        | VT \_ *xxxx*      | Valore predefinito del parametro.                                                                                                                                                         |
| **\_elementi di \_ \_ enumerazione \_ degli attributi di parametro WPD** | **VT \_ sconosciuto** | Interfaccia [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) che contiene i valori di enumerazione per il parametro.                                   |
| **\_ \_ form attributo parametro \_ WPD**                  | **\_UI4 VT**     | Formato dei valori di parametro validi consentiti.                                                                                                                                                 |
| **\_ \_ \_ dimensioni massime attributo parametro WPD \_**             | **\_UI8 VT**     | Dimensione massima, in byte, del parametro.                                                                                                                                               |
| **\_ \_ nome attributo parametro \_ WPD**                  | **\_LPWSTR VT**  | Stringa che specifica il nome descrittivo di un evento o un parametro di metodo. I caratteri validi sono alfanumerici \[ a-Za-z0-9 \] è \_ '.                                                 |
| **\_ \_ ordine attributo parametro \_ WPD**                 | **\_UI4 VT**     | Indice dell'ordine dei parametri in base zero, in modo che un valore di ordine pari a 0 corrisponda al primo parametro.                                                                                       |
| **\_ \_ intervallo attributi parametro \_ WPD \_ min**            | VT \_ *xxxx*      | Il valore massimo per un parametro nell'intervallo del form dell'attributo del parametro del modulo WPD \_ \_ \_ \_ .                                                                                                       |
| **\_ \_ intervallo attributi parametro \_ WPD \_ Max**            | VT \_ *xxxx*      | Il valore minimo per un parametro nell'intervallo del form dell'attributo del parametro del modulo WPD \_ \_ \_ \_ .                                                                                                       |
| **\_passaggio dell' \_ intervallo di attributi del parametro WPD \_ \_**           | VT \_ *xxxx*      | Valore del passaggio per un parametro nell'intervallo del form dell'attributo del parametro del modulo WPD \_ \_ \_ \_ .                                                                                                          |
| **\_ \_ \_ espressione regolare attributo parametro \_ WPD**   | **\_LPWSTR VT**  | Espressione regolare che specifica i valori accettabili per i parametri dell' \_ espressione regolare dell'attributo del parametro form WPD \_ \_ \_ \_ .                                                      |
| **\_tipo di \_ utilizzo dell'attributo del parametro WPD \_ \_**           | **\_UI4 VT**     | Integer che specifica l'utilizzo di un parametro di metodo, ad esempio in/out. I valori validi sono del tipo di enumerazione dei [**\_ tipi di \_ utilizzo \_ del parametro WPD**](wpd-parameter-usage-types.md) . |
| **WPD \_ \_ attributo parametro \_ VarType**               | **\_UI4 VT**     | Il parametro VarType.                                                                                                                                                                      |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>PortableDevice. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Proprietà e attributi**](properties-and-attributes.md)
</dt> </dl>

 

 





---
description: Per Windows 7, Windows dispositivi portatili supporta gli attributi di parametro seguenti per i metodi e gli eventi di un servizio dispositivo.
ms.assetid: a7708c60-758a-4fb6-8ef9-074ecdc9cf60
title: Attributi dei parametri (PortableDevice.h)
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
ms.openlocfilehash: 8004f4e2f9f7c22d795b6ce4e4cb0affac1b55ecd876c21288c02e226ee14262
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120006111"
---
# <a name="parameter-attributes"></a>Attributi del parametro

Per Windows 7, Windows dispositivi portatili supporta gli attributi di parametro seguenti per i metodi e gli eventi di un servizio dispositivo. Questi attributi vengono restituiti dai metodi seguenti:

-   [**IPortableDeviceServiceCapabilities::GetMethodParameterAttributes**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getmethodparameterattributes)
-   [**IPortableDeviceServiceCapabilities::GetEventParameterAttributes**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-geteventparameterattributes)




| Attributo                                            | VarType         | Descrizione                                                                                                                                                                                 |
|------------------------------------------------------|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **VALORE PREDEFINITO \_ DELL'ATTRIBUTO DEL PARAMETRO \_ WPD \_ \_**        | VT \_ *XXXX*      | Valore predefinito del parametro.                                                                                                                                                         |
| **ELEMENTI DI ENUMERAZIONE \_ DEGLI ATTRIBUTI \_ DEI \_ PARAMETRI \_ WPD** | **VT \_ UNKNOWN** | Interfaccia [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) che contiene i valori di enumerazione per il parametro .                                   |
| **MODULO DELL'ATTRIBUTO \_ \_ DEL PARAMETRO WPD \_**                  | **Interfaccia utente \_ VT4**     | Forma di valori di parametro validi consentiti.                                                                                                                                                 |
| **DIMENSIONE MASSIMA \_ \_ DELL'ATTRIBUTO DEL PARAMETRO \_ \_ WPD**             | **Interfaccia utente \_ VT8**     | Dimensioni massime del parametro, in byte.                                                                                                                                               |
| **NOME DELL'ATTRIBUTO \_ \_ DEL PARAMETRO WPD \_**                  | **VT \_ LPWSTR**  | Stringa che specifica il nome descrittivo dello script di un parametro di evento o di metodo. I caratteri validi sono alfanumerici \[ a-zA-Z0-9 \] e ' \_ '.                                                 |
| **ORDINE DEGLI ATTRIBUTI DEI PARAMETRI WPD \_ \_ \_**                 | **Interfaccia utente \_ VT4**     | Indice dell'ordine dei parametri in base zero, in modo che un valore di ordine pari a 0 corrisponda al primo parametro.                                                                                       |
| **INTERVALLO DI ATTRIBUTI DEL PARAMETRO WPD \_ \_ \_ \_ MIN**            | VT \_ *XXXX*      | Valore massimo per un parametro nel formato WPD \_ PARAMETER \_ ATTRIBUTE FORM \_ \_ RANGE.                                                                                                       |
| **INTERVALLO MASSIMO \_ ATTRIBUTI \_ PARAMETRO \_ WPD \_**            | VT \_ *XXXX*      | Valore minimo per un parametro nel formato WPD \_ PARAMETER \_ ATTRIBUTE FORM \_ \_ RANGE.                                                                                                       |
| **PASSAGGIO INTERVALLO ATTRIBUTI PARAMETRO WPD \_ \_ \_ \_**           | VT \_ *XXXX*      | Valore del passaggio per un parametro nel formato WPD \_ PARAMETER \_ ATTRIBUTE FORM \_ \_ RANGE.                                                                                                          |
| **ESPRESSIONE REGOLARE \_ DELL'ATTRIBUTO DEL PARAMETRO \_ WPD \_ \_**   | **VT \_ LPWSTR**  | Espressione regolare che specifica valori accettabili per i parametri nel formato WPD \_ PARAMETER ATTRIBUTE FORM REGULAR \_ \_ \_ \_ EXPRESSION.                                                      |
| **TIPO DI UTILIZZO \_ \_ DELL'ATTRIBUTO \_ DEL PARAMETRO \_ WPD**           | **Interfaccia utente \_ VT4**     | Intero che specifica l'utilizzo di un parametro del metodo, ad esempio in/out. I valori validi sono del [**tipo di enumerazione WPD \_ PARAMETER USAGE \_ \_ TYPES.**](wpd-parameter-usage-types.md) |
| **VARTYPE \_ \_ DELL'ATTRIBUTO DEL PARAMETRO WPD \_**               | **Interfaccia utente \_ VT4**     | Parametro VarType.                                                                                                                                                                      |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>PortableDevice.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Proprietà e attributi**](properties-and-attributes.md)
</dt> </dl>

 

 





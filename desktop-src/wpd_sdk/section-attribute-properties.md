---
description: Windows Dispositivi portatili supporta le proprietà dei dati della sezione seguente.
ms.assetid: 8760d963-fc07-4b54-aa24-5725f4b95ed2
title: Proprietà degli attributi della sezione (PortableDevice.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Section
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 21c2386175fe2c3117afd722bd9a6762b605acbc51e299d33934d161974db796
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119704331"
---
# <a name="section-attribute-properties"></a>Proprietà degli attributi della sezione

Windows Dispositivi portatili supporta le proprietà dei dati della sezione seguente.



| Proprietà                                             | VarType         | Descrizione                                                                                                                                                                                                                                                                                                                                 |
|------------------------------------------------------|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **LUNGHEZZA DEI DATI \_ DELLA SEZIONE \_ \_ WPD**                       | **Interfaccia utente \_ VT8**     | Specifica la lunghezza dell'oggetto a cui si fa riferimento.                                                                                                                                                                                                                                                                                              |
| **OFFSET DEI DATI DELLA SEZIONE WPD \_ \_ \_**                       | **Interfaccia utente \_ VT8**     | Specifica l'offset in base zero dei dati per l'oggetto a cui si fa riferimento.                                                                                                                                                                                                                                                                      |
| **RISORSA OGGETTO DI RIFERIMENTO \_ \_ DEI DATI DELLA \_ \_ SEZIONE \_ WPD** | **VT \_ UNKNOWN** | Oggetto [**IPortableDeviceKeyCollection**](iportabledevicekeycollection.md) contenente un singolo valore che specifica la chiave per una determinata risorsa. Questa risorsa è l'oggetto a cui fanno riferimento WPD \_ SECTION DATA OFFSET e \_ \_ WPD \_ SECTION DATA \_ \_ LENGTH.<br/> Se questa proprietà non esiste, viene presupposto WPD \_ RESOURCE \_ DEFAULT.<br/> |
| **UNITÀ DATI DELLA SEZIONE WPD \_ \_ \_**                        | **VT \_ UI4**     | Specifica le unità utilizzate per questo offset, ad esempio byte, millisecondi e così via. I valori possibili per questa proprietà sono definiti nell'enumerazione **WPD \_ SECTION DATA UNITS \_ \_ \_ VALUES** nel file PortableDevice.h.<br/> Se non viene specificata alcuna unità, vengono utilizzati i byte.<br/>                                          |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>PortableDevice.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Proprietà e attributi WPD**](properties-and-attributes.md)
</dt> </dl>

 

 





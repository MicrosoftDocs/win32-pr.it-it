---
description: I dispositivi portatili Windows supportano le proprietà dei dati della sezione seguente.
ms.assetid: 8760d963-fc07-4b54-aa24-5725f4b95ed2
title: Proprietà dell'attributo Section (PortableDevice. h)
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
ms.openlocfilehash: 383e2e50aa5d2a922ad50609e316b3dc9905cc38
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332372"
---
# <a name="section-attribute-properties"></a>Proprietà dell'attributo Section

I dispositivi portatili Windows supportano le proprietà dei dati della sezione seguente.



| Proprietà                                             | VarType         | Descrizione                                                                                                                                                                                                                                                                                                                                 |
|------------------------------------------------------|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **\_ \_ lunghezza dei dati della sezione WPD \_**                       | **\_UI8 VT**     | Specifica la lunghezza dell'oggetto a cui si fa riferimento.                                                                                                                                                                                                                                                                                              |
| **\_ \_ offset dati della sezione WPD \_**                       | **\_UI8 VT**     | Specifica l'offset in base zero dei dati per l'oggetto a cui si fa riferimento.                                                                                                                                                                                                                                                                      |
| **\_ \_ \_ risorsa oggetto a cui si fa riferimento dati \_ della sezione WPD \_** | **VT \_ sconosciuto** | [**IPortableDeviceKeyCollection**](iportabledevicekeycollection.md) contenente un singolo valore che specifica la chiave per una determinata risorsa. Questa risorsa è l'oggetto a cui fa riferimento \_ l' \_ offset dei dati della sezione WPD \_ e la \_ \_ lunghezza dei dati della sezione WPD \_ .<br/> Se questa proprietà non esiste, \_ \_ viene utilizzata l'impostazione predefinita della risorsa WPD.<br/> |
| **\_ \_ unità dati della sezione WPD \_**                        | **\_UI4 VT**     | Specifica le unità usate per questo offset, ad esempio, byte, millisecondi e così via. I valori possibili per questa proprietà sono definiti nell'enumerazione **WPD \_ Section \_ data \_ unit \_ values** nel file portabledevice. h.<br/> Se non viene specificata alcuna unità, vengono considerati i byte.<br/>                                          |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>PortableDevice. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Proprietà e attributi di WPD**](properties-and-attributes.md)
</dt> </dl>

 

 





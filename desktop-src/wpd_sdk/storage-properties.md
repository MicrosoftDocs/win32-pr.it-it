---
description: I dispositivi portatili Windows supportano le proprietà di archiviazione seguenti.
ms.assetid: 234078c3-e703-41f3-9b18-ae61d8a36784
title: Proprietà di archiviazione (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Storage
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 404b45a6fe5193a0550b3ecc11feeae264125110
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326593"
---
# <a name="storage-properties"></a>Storage Properties

I dispositivi portatili Windows supportano le proprietà di archiviazione seguenti.



| Proprietà                                   | VarType        | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|--------------------------------------------|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **\_capacità di archiviazione WPD \_**                 | **\_UI8 VT**    | Capacità di archiviazione totale, in byte.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| **\_ \_ capacità di archiviazione WPD \_ negli \_ oggetti**    | **\_UI8 VT**    | Indica la capacità di archiviazione totale negli oggetti. ad esempio, gli slot disponibili in una scheda SIM.                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| **\_Descrizione archiviazione \_ WPD**              | **\_LPWSTR VT** | Descrizione leggibile dell'archiviazione.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| **\_tipo di \_ file \_ System di archiviazione \_ WPD**       | **\_LPWSTR VT** | Una descrizione di stringa della file system utilizzata dalla risorsa di archiviazione, ad esempio "FAT32", "NTFS", "Contoso file System" e così via.                                                                                                                                                                                                                                                                                                                                                                                                         |
| **\_ \_ spazio libero di archiviazione WPD \_ \_ in \_ byte**   | **\_UI8 VT**    | Spazio di archiviazione disponibile, in byte.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| **\_ \_ spazio libero di archiviazione WPD \_ \_ negli \_ oggetti** | **\_UI8 VT**    | Il numero di oggetti aggiuntivi che possono essere scritti nel dispositivo. Se, ad esempio, un dispositivo consente un solo oggetto, sarà zero se l'oggetto esisteva già.                                                                                                                                                                                                                                                                                                                                                          |
| **\_numero di \_ serie di archiviazione WPD \_**           | **\_LPWSTR VT** | Numero di serie specifico del fornitore per l'archiviazione.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| **\_ \_ dimensioni massime dell' \_ oggetto di \_ archiviazione WPD**        | **\_UI8 VT**    | Specifica la dimensione massima di un singolo oggetto, in byte, che può essere inserito in questa risorsa di archiviazione.                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| **\_tipo di archiviazione WPD \_**                     | **\_UI4 VT**    | Descrive il tipo fisico di un supporto di archiviazione di memoria.                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| **\_funzionalità di \_ accesso alle risorse di archiviazione \_ WPD**       | **\_UI4 VT**    | Identifica le protezioni di scrittura che influiscono a livello globale su questa risorsa di archiviazione. Ha la precedenza sull'accesso specificato nei singoli oggetti. I valori possibili sono delineati dall'enumerazione **WPD \_ storage \_ Access \_ Capability \_ values** definita in portabledevice. h. Se, ad esempio, il **\_ \_ tipo di archiviazione WPD** è ROM (ovvero un tipo di **archiviazione WPD ROM \_ \_ \_ fisso \_** o un **tipo di \_ archiviazione \_ \_ \_ WPD**), il valore della **funzionalità di \_ \_ accesso alle \_ risorse di archiviazione WPD** deve essere la **funzionalità di accesso alle risorse di archiviazione WPD di \_ \_ \_ \_ sola lettura \_ \_ senza \_ \_ eliminazione di oggetti**. |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>PortableDevice. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Proprietà e attributi di WPD**](properties-and-attributes.md)
</dt> </dl>

 

 





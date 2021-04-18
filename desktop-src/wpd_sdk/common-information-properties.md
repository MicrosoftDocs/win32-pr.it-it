---
description: I dispositivi portatili Windows supportano le seguenti proprietà delle informazioni comuni.
ms.assetid: eaae7431-d53d-42a1-9286-001c6f5b1641
title: Proprietà informazioni comuni (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Common
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: b773d8404997da20b4196c802ba12286679af683
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330495"
---
# <a name="common-information-properties"></a>Proprietà informazioni comuni

I dispositivi portatili Windows supportano le seguenti proprietà delle informazioni comuni.



| Proprietà                                      | VarType        | Descrizione                                                                                              |
|-----------------------------------------------|----------------|----------------------------------------------------------------------------------------------------------|
| **\_ \_ Note informative comuni di WPD \_**           | **\_LPWSTR VT** | Per gli appuntamenti, le attività e gli oggetti simili, questa proprietà contiene le note per l'oggetto specificato.     |
| **\_ \_ oggetto informazioni comuni \_ WPD**         | **\_LPWSTR VT** | Valore che specifica il campo dell'oggetto di questo oggetto.                                                 |
| **\_testo del \_ corpo delle informazioni comuni \_ WPD \_**      | **\_LPWSTR VT** | Questa proprietà contiene il testo del corpo di un oggetto, in formato testo non crittografato o HTML.                          |
| **\_ \_ priorità delle informazioni comuni di WPD \_**        | **\_UI4 VT**    | Valore che specifica la priorità di questo oggetto. 0 indica la priorità più alta.                    |
| **Data/ora di \_ \_ inizio informazioni comuni \_ WPD \_** | **\_Data VT**   | Valore che specifica la data e l'ora in cui è pianificato l'avvio di un appuntamento, un'attività o un oggetto simile. |
| **Data/ora di \_ \_ fine informazioni comuni \_ WPD \_**   | **\_Data VT**   | Valore che specifica la data e l'ora di fine pianificata per un appuntamento, un'attività o un oggetto simile.   |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>PortableDevice. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Proprietà e attributi di WPD**](properties-and-attributes.md)
</dt> </dl>

 

 





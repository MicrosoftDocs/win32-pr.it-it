---
description: Windows Dispositivi portatili supporta le proprietà di informazioni comuni seguenti.
ms.assetid: eaae7431-d53d-42a1-9286-001c6f5b1641
title: Proprietà relative alle informazioni comuni (PortableDevice.h)
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
ms.openlocfilehash: 41a8845a41714ed1a775d19e14f0996aad698aaf99de18da4eceb4df92688409
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118431104"
---
# <a name="common-information-properties"></a>Proprietà comuni delle informazioni

Windows Dispositivi portatili supporta le proprietà di informazioni comuni seguenti.



| Proprietà                                      | VarType        | Descrizione                                                                                              |
|-----------------------------------------------|----------------|----------------------------------------------------------------------------------------------------------|
| **NOTE SULLE INFORMAZIONI \_ COMUNI WPD \_ \_**           | **VT \_ LPWSTR** | Per gli appuntamenti, le attività e gli oggetti simili, questa proprietà contiene tutte le note per l'oggetto specificato.     |
| **WPD \_ COMMON \_ INFORMATION \_ SUBJECT**         | **VT \_ LPWSTR** | Valore che specifica il campo dell'oggetto .                                                 |
| **TESTO DEL CORPO \_ DELLE INFORMAZIONI COMUNI \_ WPD \_ \_**      | **VT \_ LPWSTR** | Questa proprietà contiene il testo del corpo di un oggetto, in formato testo non crittografato o HTML.                          |
| **PRIORITÀ DELLE INFORMAZIONI COMUNI WPD \_ \_ \_**        | **Interfaccia utente \_ VT4**    | Valore che specifica la priorità di questo oggetto. 0 indica la priorità più alta.                    |
| **DATETIME DI \_ INIZIO DELLE INFORMAZIONI COMUNI \_ \_ \_ WPD** | **DATA \_ VT**   | Valore che specifica la data/ora di inizio di un appuntamento, un'attività o un oggetto simile. |
| **DATETIME DI \_ FINE DELLE INFORMAZIONI COMUNI \_ \_ \_ WPD**   | **DATA \_ VT**   | Valore che specifica la data/ora in cui è pianificata la fine di un appuntamento, un'attività o un oggetto simile.   |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>PortableDevice.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Proprietà e attributi WPD**](properties-and-attributes.md)
</dt> </dl>

 

 





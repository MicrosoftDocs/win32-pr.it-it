---
description: I dispositivi portatili Windows supportano le proprietà SMS seguenti.
ms.assetid: d821f378-522f-4f0a-825b-6b15295e7b12
title: Proprietà SMS (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SMS
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: c43917c8c26027713b4e5076e8eb3789b95f08e6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326595"
---
# <a name="sms-properties"></a>Proprietà SMS

I dispositivi portatili Windows supportano le proprietà SMS seguenti.



| Proprietà                   | VarType        | Descrizione                                                                                                                                                                                                                                                                                                 |
|----------------------------|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **\_codifica SMS \_ WPD**     | **\_LPWSTR VT** | Valore che specifica il modo in cui il driver codificherà il messaggio di testo inviato dal client. Si tratta di una proprietà di sola lettura. il client non è in grado di specificare il tipo di codifica utilizzato da un dispositivo per l'invio di messaggi. Questi valori duplicano i valori enumerati dei [**\_ \_ \_ tipi di codifica SMS di WPD**](wpd-sms-encoding-types.md) . |
| **\_ \_ payload max SMS \_ WPD** | **\_UI4 VT**    | Numero massimo di byte che possono essere contenuti in un messaggio.                                                                                                                                                                                                                                             |
| **\_provider SMS \_ WPD**     | **\_LPWSTR VT** | Nome del provider di servizi.                                                                                                                                                                                                                                                                                |
| **\_timeout SMS \_ WPD**      | **\_UI4 VT**    | Numero di millisecondi fino alla restituzione di un timeout.                                                                                                                                                                                                                                                     |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>PortableDevice. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Proprietà e attributi di WPD**](properties-and-attributes.md)
</dt> </dl>

 

 





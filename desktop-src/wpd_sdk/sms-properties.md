---
description: Windows Dispositivi portatili supporta le proprietà SMS seguenti.
ms.assetid: d821f378-522f-4f0a-825b-6b15295e7b12
title: Proprietà SMS (PortableDevice.h)
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
ms.openlocfilehash: 12b68a962fc79dd75d6ff90635be5dbe99f36c3170f06cd7d79af2eb23317e98
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118193582"
---
# <a name="sms-properties"></a>Proprietà SMS

Windows Dispositivi portatili supporta le proprietà SMS seguenti.



| Proprietà                   | VarType        | Descrizione                                                                                                                                                                                                                                                                                                 |
|----------------------------|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **CODIFICA SMS WPD \_ \_**     | **VT \_ LPWSTR** | Valore che specifica come il driver codifica il messaggio di testo inviato dal client. Si tratta di una proprietà di sola lettura. il client non può specificare il tipo di codifica utilizzato da un dispositivo per inviare messaggi. Questi valori duplicano [**i valori \_ enumerati WPD SMS ENCODING \_ \_ TYPES.**](wpd-sms-encoding-types.md) |
| **PAYLOAD MASSIMO SMS WPD \_ \_ \_** | **VT \_ UI4**    | Numero massimo di byte che possono essere contenuti in un messaggio.                                                                                                                                                                                                                                             |
| **WPD \_ SMS \_ PROVIDER**     | **VT \_ LPWSTR** | Nome del provider di servizi.                                                                                                                                                                                                                                                                                |
| **WPD \_ SMS \_ TIMEOUT**      | **VT \_ UI4**    | Numero di millisecondi prima che sia restituito un timeout.                                                                                                                                                                                                                                                     |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>PortableDevice.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Proprietà e attributi WPD**](properties-and-attributes.md)
</dt> </dl>

 

 





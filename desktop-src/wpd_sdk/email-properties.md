---
description: Windows Dispositivi portatili supporta le proprietà di posta elettronica seguenti.
ms.assetid: c886622e-57e7-4bd1-b645-0e979ee7b66a
title: Proprietà posta elettronica (PortableDevice.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Email
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 4c67a341bcc7fcac041f02cc183c02e024e60b121150aba0ce62da2f973ccbec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117843233"
---
# <a name="email-properties"></a>Proprietà posta elettronica

Windows Dispositivi portatili supporta le proprietà di posta elettronica seguenti.



| Proprietà                         | VarType        | Descrizione                                                                                                                               |
|----------------------------------|----------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| **WPD \_ EMAIL \_ BCC \_ LINE**        | **VT \_ LPWSTR** | Destinatari BCC del messaggio di posta elettronica. I destinatari BCC ricevono una copia del messaggio di posta elettronica, ma i relativi nomi non vengono visualizzati come destinatari.   |
| **WPD \_ EMAIL \_ CC \_ LINE**         | **VT \_ LPWSTR** | Destinatari CC del messaggio di posta elettronica. I destinatari CC ricevono una copia del messaggio di posta elettronica e i relativi nomi vengono visualizzati come destinatari. |
| **LA POSTA ELETTRONICA WPD \_ \_ HA \_ ALLEGATI** | **VT \_ BOOL**   | Valore booleano che specifica se il messaggio di posta elettronica contiene allegati.                                                               |
| **L'INDIRIZZO DI \_ POSTA ELETTRONICA WPD È STATO \_ \_ \_ LETTO**  | **VT \_ BOOL**   | Valore booleano che specifica se il messaggio di posta elettronica è stato letto.                                                                 |
| **ORA DI RICEZIONE \_ DEL MESSAGGIO DI POSTA \_ ELETTRONICA WPD \_**   | **DATA \_ VT**   | Valore che specifica quando è stato ricevuto il messaggio di posta elettronica.                                                                              |
| **INDIRIZZO MITTENTE DI \_ POSTA \_ ELETTRONICA \_ WPD**  | **VT \_ LPWSTR** | Indirizzo di posta elettronica del mittente.                                                                                                         |
| **WPD \_ EMAIL \_ TO \_ LINE**         | **VT \_ LPWSTR** | Destinatari principali del messaggio di posta elettronica.                                                                                                |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>PortableDevice.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Proprietà e attributi WPD**](properties-and-attributes.md)
</dt> </dl>

 

 





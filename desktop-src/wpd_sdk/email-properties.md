---
description: Dispositivi portatili Windows supporta le seguenti proprietà di posta elettronica.
ms.assetid: c886622e-57e7-4bd1-b645-0e979ee7b66a
title: Proprietà posta elettronica (PortableDevice. h)
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
ms.openlocfilehash: de25d73e9fb331538ecdbf5f22306d85c282b338
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328969"
---
# <a name="email-properties"></a>Proprietà posta elettronica

Dispositivi portatili Windows supporta le seguenti proprietà di posta elettronica.



| Proprietà                         | VarType        | Descrizione                                                                                                                               |
|----------------------------------|----------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| **WPD \_ - \_ linea Ccn posta elettronica \_**        | **\_LPWSTR VT** | Destinatari Ccn del messaggio di posta elettronica. I destinatari Ccn ricevono una copia del messaggio di posta elettronica, ma i relativi nomi non vengono visualizzati come destinatari.   |
| **\_linea CC di posta elettronica WPD \_ \_**         | **\_LPWSTR VT** | Destinatari CC del messaggio di posta elettronica. I destinatari CC ricevono una copia del messaggio di posta elettronica e i relativi nomi vengono visualizzati come destinatari. |
| **WPD \_ posta elettronica \_ con \_ allegati** | **\_bool VT**   | Valore booleano che specifica se questo messaggio di posta elettronica contiene allegati.                                                               |
| **il \_ messaggio di posta elettronica WPD \_ è \_ stato \_ letto**  | **\_bool VT**   | Valore booleano che specifica se il messaggio di posta elettronica è stato letto.                                                                 |
| **WPD \_ \_ tempo di ricezione posta elettronica \_**   | **\_Data VT**   | Valore che specifica quando è stato ricevuto il messaggio di posta elettronica.                                                                              |
| **\_indirizzo mittente di posta elettronica WPD \_ \_**  | **\_LPWSTR VT** | Indirizzo di posta elettronica del mittente.                                                                                                         |
| **WPD \_ posta elettronica \_ alla \_ riga**         | **\_LPWSTR VT** | Destinatari principali del messaggio di posta elettronica.                                                                                                |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>PortableDevice. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Proprietà e attributi di WPD**](properties-and-attributes.md)
</dt> </dl>

 

 





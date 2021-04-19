---
description: I dispositivi portatili Windows supportano le proprietà di appuntamento seguenti.
ms.assetid: d7e2130b-722b-46ef-9114-17db9c95d017
title: Proprietà appuntamento (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Appointment
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 542029f9eb698c8093c43cbb8ee309b3d1f9da6a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331829"
---
# <a name="appointment-properties"></a>Proprietà appuntamento

I dispositivi portatili Windows supportano le proprietà di appuntamento seguenti.



| Proprietà                                   | VarType        | Descrizione                                                                          |
|--------------------------------------------|----------------|--------------------------------------------------------------------------------------|
| **\_ \_ partecipanti accettati appuntamento WPD \_**  | **\_LPWSTR VT** | Elenco delimitato da punti e virgola dei partecipanti che hanno accettato l'appuntamento.             |
| **WPD \_ appuntamento \_ rifiutato \_**  | **\_LPWSTR VT** | Elenco delimitato da punti e virgola di partecipanti che hanno rifiutato l'appuntamento.             |
| **\_località appuntamento \_ WPD**             | \_LPWSTR VT     | Posizione descrittiva dell'appuntamento, ad esempio, "Building 5, Room 7".    |
| **\_ \_ partecipanti facoltativi appuntamento WPD \_**  | **\_LPWSTR VT** | Elenco delimitato da punti e virgola di partecipanti facoltativi per l'appuntamento.                  |
| **\_ \_ partecipanti richiesti per l'appuntamento WPD \_**  | **\_LPWSTR VT** | Elenco delimitato da punti e virgola dei partecipanti richiesti per l'appuntamento.                  |
| **\_risorse appuntamento \_ WPD**            | **\_LPWSTR VT** | Elenco delimitato da punti e virgola delle risorse necessarie per l'appuntamento.                  |
| **\_ \_ partecipanti provvisorio di appuntamento WPD \_** | **\_LPWSTR VT** | Elenco delimitato da punti e virgola dei partecipanti che hanno accettato provvisoriamente l'appuntamento. |
| **\_tipo di appuntamento WPD \_**                 | **\_LPWSTR VT** | Tipo di appuntamento, ad esempio, "personale", "business" e così via.              |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>PortableDevice. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Proprietà e attributi di WPD**](properties-and-attributes.md)
</dt> </dl>

 

 





---
description: I dispositivi portatili Windows supportano le seguenti proprietà dell'attività.
ms.assetid: 9bd6c2e1-740a-453d-b390-120700af7c93
title: Proprietà attività (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Task
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 829685ac3fa5737356c172ed9e66303b3d6115ca
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326592"
---
# <a name="task-properties"></a>Proprietà attività

I dispositivi portatili Windows supportano le seguenti proprietà dell'attività.



| Proprietà                         | VarType        | Descrizione                                                                                 |
|----------------------------------|----------------|---------------------------------------------------------------------------------------------|
| **\_proprietario attività \_ WPD**             | **\_LPWSTR VT** | Proprietario dell'attività.                                                                      |
| **\_ \_ percentuale completamento attività \_ WPD** | **\_UI4 VT**    | Numero compreso tra 0 e 100 che specifica la modalità di completamento dell'attività.                         |
| **\_Data di \_ promemoria attività WPD \_**    | **\_Data VT**   | Valore che specifica quando inviare un promemoria per eseguire l'attività, se non è stata completata. |
| **\_stato attività \_ WPD**            | **\_LPWSTR VT** | Una descrizione di stringa dello stato dell'attività, ad esempio "in corso".                 |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>PortableDevice. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Proprietà e attributi di WPD**](properties-and-attributes.md)
</dt> </dl>

 

 





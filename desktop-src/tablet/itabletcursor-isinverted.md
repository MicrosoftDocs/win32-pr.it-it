---
description: Indica se lo stilo è capovolto.
ms.assetid: 04b05287-000d-455f-88e5-821c7fdb8119
title: 'Metodo ITabletCursor:: ininverted'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletCursor.IsInverted
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 041b81c38f3370421c96a4c0d66201254a715e62
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314914"
---
# <a name="itabletcursorisinverted-method"></a>Metodo ITabletCursor:: ininverted

Indica se lo stilo è capovolto.

## <a name="syntax"></a>Sintassi


```C++
HRESULT IsInverted();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Codice restituito                                                                             | Descrizione                               |
|-----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>    | Lo stilo è invertito.<br/>        |
| <dl> <dt>**S \_ false**</dt> </dl> | Lo stilo non è invertito.<br/>    |
| <dl> <dt>**E \_ non riescono**</dt> </dl>  | Si è verificato un errore non specificato.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows XP Tablet PC Edition \[\]<br/>                          |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                              |
| Libreria<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ITabletCursor**](itabletcursor.md)
</dt> <dt>

[**Interfaccia ITabletCursorButton**](itabletcursorbutton.md)
</dt> </dl>

 

 





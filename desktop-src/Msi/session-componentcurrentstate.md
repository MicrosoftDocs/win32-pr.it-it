---
description: La proprietà ComponentCurrentState dell'oggetto Session è una proprietà di sola lettura che restituisce lo stato corrente installato del componente designato. Per i valori di stato, vedere la proprietà ComponentRequestState.
ms.assetid: c8343e90-8867-462d-9844-e547341a590c
title: Session.ComponentCurrentState - proprietà
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.ComponentCurrentState
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: ce060c7eddb76491480f4a1de9f477629da489ae9d8412adc02da25b8d7a0a1e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120039858"
---
# <a name="sessioncomponentcurrentstate-property"></a>Session.ComponentCurrentState - proprietà

La **proprietà ComponentCurrentState** dell'oggetto [**Session**](session-object.md) è una proprietà di sola lettura che restituisce lo stato corrente installato del componente designato. Per i valori di stato, [**vedere la proprietà ComponentRequestState.**](session-componentrequeststate.md)

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```JScript
propVal = Session.ComponentCurrentState
```



## <a name="property-value"></a>Valore proprietà

Nome stringa obbligatorio del componente richiesto, chiave primaria nella tabella Component.

## <a name="remarks"></a>Commenti

Se la proprietà ha esito negativo, è possibile ottenere informazioni estese sull'errore usando il [**metodo LastErrorRecord.**](installer-lasterrorrecord.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Programma di installazione 5.0 Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4.0 o Windows Installer 4.5 in Windows Server 2008 o Windows Vista. Windows Programma di installazione Windows Server 2003 o Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ ISession è definito come 000C109E-0000-0000-C000-000000000046<br/>                                                                                                                                                                             |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Sessione**](session-object.md)
</dt> <dt>

[**ComponentRequestState - proprietà**](session-componentrequeststate.md)
</dt> </dl>

 

 





---
description: La proprietà ComponentCurrentState dell'oggetto Session è una proprietà di sola lettura che restituisce lo stato corrente di installazione del componente designato. Per i valori di stato, vedere la proprietà ComponentRequestState.
ms.assetid: c8343e90-8867-462d-9844-e547341a590c
title: Proprietà Session. ComponentCurrentState
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
ms.openlocfilehash: 8c556dd9656ebced155ef90fe96abd394a32ff1b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329111"
---
# <a name="sessioncomponentcurrentstate-property"></a>Proprietà Session. ComponentCurrentState

La proprietà **ComponentCurrentState** dell'oggetto [**Session**](session-object.md) è una proprietà di sola lettura che restituisce lo stato corrente di installazione del componente designato. Per i valori di stato, vedere la proprietà [**ComponentRequestState**](session-componentrequeststate.md) .

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```JScript
propVal = Session.ComponentCurrentState
```



## <a name="property-value"></a>Valore proprietà

Nome della stringa obbligatoria del componente richiesto, chiave primaria nella tabella dei componenti.

## <a name="remarks"></a>Commenti

Se la proprietà ha esito negativo, è possibile ottenere informazioni estese sugli errori usando il metodo [**LastErrorRecord**](installer-lasterrorrecord.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista. Windows Installer in Windows Server 2003 o Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ ISession è definito come 000C109E-0000-0000-C000-000000000046<br/>                                                                                                                                                                             |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Sessione**](session-object.md)
</dt> <dt>

[**Proprietà ComponentRequestState**](session-componentrequeststate.md)
</dt> </dl>

 

 





---
description: La proprietà ComponentRequestState dell'oggetto Session ottiene o richiede una modifica dello stato Action di una riga nella tabella Component.
ms.assetid: d0b50c25-dca6-4bdf-8ee9-490e436fcc5b
title: Session.ComponentRequestState - proprietà
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.ComponentRequestState
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 3cef17ab3a4781f925e92968bd50dfedddd9a0df8e1781a2f209712fc447ef10
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118625237"
---
# <a name="sessioncomponentrequeststate-property"></a>Session.ComponentRequestState - proprietà

La **proprietà ComponentRequestState** dell'oggetto [**Session**](session-object.md) ottiene o richiede una modifica dello stato Action di una riga nella [tabella Component](component-table.md).

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```JScript
propVal = Session.ComponentRequestState
```



## <a name="property-value"></a>Valore proprietà

Nome stringa obbligatorio dell'elemento del componente, chiave primaria della tabella Component.

## <a name="remarks"></a>Commenti



| Stato di selezione        | Valore | Descrizione                                                    |
|------------------------|-------|----------------------------------------------------------------|
| Null                   | Null  | Richiede che non sia stata eseguita alcuna azione per questo elemento.                |
| msiInstallStateAbsent  | 2     | L'elemento deve essere rimosso.                                         |
| msiInstallStateLocal   | 3     | L'elemento deve essere installato in locale.                               |
| msiInstallStateSource  | 4     | L'elemento deve essere installato ed eseguito dal supporto di origine.         |
| msiInstallStateDefault | 5     | Se installato, l'elemento deve essere reinstallato nello stesso stato. |



 

Se la proprietà ha esito negativo, è possibile ottenere informazioni estese sull'errore usando il [**metodo LastErrorRecord.**](installer-lasterrorrecord.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Programma di installazione 5.0 Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Programma di installazione 4.0 o Windows Installer 4.5 in Windows Server 2008 o Windows Vista. Windows Programma di installazione Windows Server 2003 o Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID ISession è definito \_ come 000C109E-0000-0000-C000-000000000046<br/>                                                                                                                                                                             |



 

 





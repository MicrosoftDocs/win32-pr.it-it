---
description: La proprietà Property dell'oggetto Session è una proprietà di lettura/scrittura che rappresenta il valore stringa di una proprietà del programma di installazione denominata, come gestito dall'oggetto Session.
ms.assetid: 15ce8264-2573-428c-98d9-690cfaae5144
title: Session.Property - proprietà
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.Property
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 7f47efd603f10378e6cf5b09144d57776a42cd515f3bd6194174d94bc2583514
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119628831"
---
# <a name="sessionproperty-property"></a>Session.Property - proprietà

La proprietà **Property** dell'oggetto [**Session**](session-object.md) è una proprietà di lettura/scrittura che rappresenta il valore stringa di una proprietà del programma di installazione denominata, gestita dall'oggetto **Session** nella tabella Property in memoria, oppure, se è preceduta da un segno di percentuale (%), il valore di una variabile di ambiente di sistema per il processo corrente. È possibile specificare valori stringa o interi. Una proprietà o una variabile di ambiente inesistente equivale al valore Null.

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```JScript
propVal = Session.Property
Session.Property = propVal 
```



## <a name="property-value"></a>Valore proprietà

Nome obbligatorio con distinzione tra maiuscole e minuscole di una proprietà o nome senza distinzione tra maiuscole e minuscole di una variabile di ambiente preceduto da un segno di percentuale (%).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Programma di installazione 5.0 Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4.0 o Windows Installer 4.5 in Windows Server 2008 o Windows Vista. Windows Programma di installazione Windows Server 2003 o Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ ISession è definito come 000C109E-0000-0000-C000-000000000046<br/>                                                                                                                                                                             |



 

 





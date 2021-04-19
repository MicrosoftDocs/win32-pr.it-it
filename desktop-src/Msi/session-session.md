---
description: La proprietà Property dell'oggetto Session è una proprietà di lettura/scrittura che rappresenta il valore stringa di una proprietà del programma di installazione denominata gestita dall'oggetto Session.
ms.assetid: 15ce8264-2573-428c-98d9-690cfaae5144
title: Proprietà Session. Property
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
ms.openlocfilehash: 9635d5b9ee093f270e4ee7993f78609d60caa13a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333037"
---
# <a name="sessionproperty-property"></a>Proprietà Session. Property

La proprietà **Property** dell'oggetto [**Session**](session-object.md) è una proprietà di lettura/scrittura che rappresenta il valore stringa di una proprietà del programma di installazione denominata, gestita dall'oggetto **Session** nella tabella delle proprietà in memoria, oppure, se è preceduto da un segno di percentuale (%), il valore di una variabile di ambiente di sistema per il processo corrente. È possibile specificare valori stringa o Integer. Una proprietà o una variabile di ambiente non esistente è equivalente al valore null.

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```JScript
propVal = Session.Property
Session.Property = propVal 
```



## <a name="property-value"></a>Valore proprietà

Nome obbligatorio con distinzione tra maiuscole e minuscole di una proprietà o nome di una variabile di ambiente preceduto da un segno di percentuale (%).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista. Windows Installer in Windows Server 2003 o Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ ISession è definito come 000C109E-0000-0000-C000-000000000046<br/>                                                                                                                                                                             |



 

 





---
description: La proprietà Environment dell'oggetto Installer è una proprietà di lettura/scrittura che rappresenta il valore stringa per una variabile di ambiente del processo corrente.
ms.assetid: f59a270f-9bd8-4d17-96e2-cb3c62a31cad
title: Installer.Environment - proprietà
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.Environment
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 8f24237da6c140ef0d38ff17591bf214698cfa6731bd4e8d3cfcaa613b335404
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118631687"
---
# <a name="installerenvironment-property"></a>Installer.Environment - proprietà

La **proprietà Environment** dell'oggetto [**Installer**](installer-object.md) è una proprietà di lettura/scrittura che rappresenta il valore stringa per una variabile di ambiente del processo corrente.

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```JScript
propVal = Installer.Environment
Installer.Environment = propVal 
```



## <a name="property-value"></a>Valore proprietà

Nome della variabile di ambiente da leggere o scrivere. Questa operazione non fa distinzione tra maiuscole e minuscole.

## <a name="remarks"></a>Commenti

L'impostazione di una variabile **di ambiente con la proprietà Environment** influisce solo sulla sessione attiva. Per apportare modifiche permanenti a una variabile di ambiente, usare la [tabella Environment](environment-table.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Programma di installazione 5.0 Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4.0 o Windows Installer 4.5 in Windows Server 2008 o Windows Vista. Windows Programma di installazione Windows Server 2003 o Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller è definito come 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



 

 





---
description: La proprietà Property dell'oggetto UIPreview è una proprietà di lettura/scrittura che rappresenta il valore stringa di una proprietà del programma di installazione denominata oppure, se è preceduto da un segno di percentuale (%), il valore di una variabile di ambiente di sistema per il processo corrente.
ms.assetid: 92900426-8fb5-4a94-a982-438267ad756e
title: Proprietà UIPreview. Property
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UIPreview.Property
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 430c6f75b03fe69f8054bb2b0a61bab59dcc4d58
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327915"
---
# <a name="uipreviewproperty-property"></a>Proprietà UIPreview. Property

La proprietà **Property** dell'oggetto [**UIPreview**](uipreview-object.md) è una proprietà di lettura/scrittura che rappresenta il valore stringa di una proprietà del programma di installazione denominata oppure, se è preceduto da un segno di percentuale (%), il valore di una variabile di ambiente di sistema per il processo corrente. Questa operazione viene esposta per consentire la visualizzazione corretta delle finestre di dialogo che dipendono dai valori delle proprietà. È possibile specificare valori stringa o Integer. Una proprietà o una variabile di ambiente inesistente è equivalente al valore null.

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```JScript
propVal = UIPreview.Property
UIPreview.Property = propVal 
```



## <a name="property-value"></a>Valore proprietà

Nome obbligatorio con distinzione tra maiuscole e minuscole di una proprietà o nome di una variabile di ambiente preceduto da un segno di percentuale (%).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista. Windows Installer in Windows Server 2003 o Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IUIPreview è definito come 000C109A-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



 

 





---
description: La proprietà Property dell'oggetto UIPreview è una proprietà di lettura/scrittura che rappresenta il valore stringa di una proprietà del programma di installazione denominata oppure, se è preceduta da un segno di percentuale (%), il valore di una variabile di ambiente di sistema per il processo corrente.
ms.assetid: 92900426-8fb5-4a94-a982-438267ad756e
title: UIPreview.Property - proprietà
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
ms.openlocfilehash: 51ef7b4589372006241beff1e9c35180b32c4d358e817b8d380353c324ffd9a7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118623204"
---
# <a name="uipreviewproperty-property"></a>UIPreview.Property - proprietà

La proprietà **Property** dell'oggetto [**UIPreview**](uipreview-object.md) è una proprietà di lettura/scrittura che rappresenta il valore stringa di una proprietà del programma di installazione denominata oppure, se è preceduta da un segno di percentuale (%), il valore di una variabile di ambiente di sistema per il processo corrente. Viene esposto per consentire la visualizzazione corretta delle finestre di dialogo che dipendono dai valori delle proprietà. È possibile specificare valori stringa o interi. Una proprietà o una variabile di ambiente inesistente equivale a essere null.

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```JScript
propVal = UIPreview.Property
UIPreview.Property = propVal 
```



## <a name="property-value"></a>Valore proprietà

Nome obbligatorio con distinzione tra maiuscole e minuscole di una proprietà o nome senza distinzione tra maiuscole e minuscole di una variabile di ambiente preceduto da un segno di percentuale (%).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Programma di installazione 5.0 Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4.0 o Windows Installer 4.5 in Windows Server 2008 o Windows Vista. Windows Programma di installazione Windows Server 2003 o Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IUIPreview è definito come 000C109A-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



 

 





---
description: La proprietà Item è una proprietà di sola lettura che restituisce una stringa nella raccolta di oggetti StringList.
ms.assetid: 5c654927-41cf-4e47-9d4f-76524f8bbc97
title: StringList.Item - proprietà
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- StringList.Item
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 85962aac5e841c929518a7a37fdada647ce4c74baa69be23048f26f5470c91fe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118142019"
---
# <a name="stringlistitem-property"></a>StringList.Item - proprietà

La **proprietà Item** è una proprietà di sola lettura che restituisce una stringa nella raccolta di oggetti [**StringList.**](stringlist-object.md)

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```JScript
propVal = StringList.Item
```



## <a name="property-value"></a>Valore proprietà

Numero di indice dell'elemento con la raccolta di stringhe. Questo parametro è obbligatorio.

## <a name="remarks"></a>Commenti

Il client deve verificare che [**l'oggetto StringList**](stringlist-object.md) esista e non sia vuoto prima di fare riferimento alla **proprietà Item.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Programma di installazione 5.0 Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4.0 o Windows Installer 4.5 in Windows Server 2008 o Windows Vista. Windows Programma di installazione Windows Server 2003 o Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IStringList è definito come 000C1095-0000-0000-C000-000000000046<br/>                                                                                                                                                                          |



 

 





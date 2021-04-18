---
description: La proprietà Item è una proprietà di sola lettura che restituisce una stringa nella raccolta di oggetti String.
ms.assetid: 5c654927-41cf-4e47-9d4f-76524f8bbc97
title: Proprietà String. Item
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
ms.openlocfilehash: ebd32af433fd932cb05d062fbc515a3245113343
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330916"
---
# <a name="stringlistitem-property"></a>Proprietà String. Item

La proprietà **Item** è una proprietà di sola lettura che restituisce una stringa nella raccolta di [**oggetti String**](stringlist-object.md) .

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```JScript
propVal = StringList.Item
```



## <a name="property-value"></a>Valore proprietà

Numero di indice dell'elemento con la raccolta di stringhe. Questo parametro è obbligatorio.

## <a name="remarks"></a>Commenti

Prima di fare riferimento alla proprietà **Item** , il client deve verificare che l' [**oggetto stringa**](stringlist-object.md) esista e non sia vuoto.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista. Windows Installer in Windows Server 2003 o Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ è definito come 000C1095-0000-0000-C000-000000000046<br/>                                                                                                                                                                          |



 

 





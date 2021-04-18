---
description: La proprietà Item è una proprietà di sola lettura che restituisce un record in una raccolta di oggetti di registrazione.
ms.assetid: 59646aa8-811c-4658-8b47-42f70abfdfdb
title: Proprietà Recording. Item
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RecordList.Item
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 4c7b9332393c4055cb8052b2b759b93781c0fd73
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328761"
---
# <a name="recordlistitem-property"></a>Proprietà Recording. Item

La proprietà **Item** è una proprietà di sola lettura che restituisce un record in una raccolta di oggetti di [**registrazione**](recordlist-object.md) .

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```JScript
propVal = RecordList.Item
```



## <a name="property-value"></a>Valore proprietà

Numero di indice dell'elemento con la raccolta di stringhe. L'indice è obbligatorio.

## <a name="remarks"></a>Commenti

Il client deve verificare che l'oggetto di [**registrazione**](recordlist-object.md) esista e non sia vuoto prima di fare riferimento alla proprietà Item.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista. Windows Installer in Windows Server 2003 o Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IRecordList è definito come 000C1096-0000-0000-C000-000000000046<br/>                                                                                                                                                                          |



 

 





---
description: La proprietà VerifyDiskSpace è di sola lettura.
ms.assetid: 62f11f71-00b0-4e04-8c45-d6d670238886
title: Session.VerifyDiskSpace - proprietà
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.VerifyDiskSpace
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 4a50bb96088f2c52673fda9a9ddffd786657376bcb4e4a60d5c6d81cb4fbe5e0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119628761"
---
# <a name="sessionverifydiskspace-property"></a>Session.VerifyDiskSpace - proprietà

La **proprietà VerifyDiskSpace** è di sola lettura. Restituisce true se lo spazio su disco è sufficiente e false se il disco è pieno. Poiché questa proprietà usa le informazioni raccolte dalle azioni di determinazione costi, **VerifyDiskSpace** deve essere chiamato solo dopo l'azione [CostInitialize](costinitialize-action.md), [l'azione FileCost](filecost-action.md)e l'azione [CostFinalize](costfinalize-action.md).

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```JScript
propVal = Session.VerifyDiskSpace
```



## <a name="property-value"></a>Valore proprietà

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Programma di installazione 5.0 Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4.0 o Windows Installer 4.5 in Windows Server 2008 o Windows Vista. Windows Programma di installazione Windows Server 2003 o Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ ISession è definito come 000C109E-0000-0000-C000-000000000046<br/>                                                                                                                                                                             |



 

 





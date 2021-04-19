---
description: La proprietà VerifyDiskSpace è una proprietà di sola lettura.
ms.assetid: 62f11f71-00b0-4e04-8c45-d6d670238886
title: Proprietà Session. VerifyDiskSpace
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
ms.openlocfilehash: a73f2b6f846cb918d5eb10689388a174950c0edc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333031"
---
# <a name="sessionverifydiskspace-property"></a>Proprietà Session. VerifyDiskSpace

La proprietà **VerifyDiskSpace** è una proprietà di sola lettura. Restituisce true se è disponibile spazio su disco sufficiente e false se il disco è pieno. Poiché questa proprietà utilizza le informazioni raccolte dalle azioni di determinazione dei costi, **VerifyDiskSpace** deve essere chiamato solo dopo l' [azione CostInitialize](costinitialize-action.md), l'azione [filecost](filecost-action.md)e l' [azione CostFinalize secondo](costfinalize-action.md).

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```JScript
propVal = Session.VerifyDiskSpace
```



## <a name="property-value"></a>Valore proprietà

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista. Windows Installer in Windows Server 2003 o Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ ISession è definito come 000C109E-0000-0000-C000-000000000046<br/>                                                                                                                                                                             |



 

 





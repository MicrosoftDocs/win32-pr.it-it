---
description: La proprietà di contesto restituisce il contesto di questa patch.
ms.assetid: 09c92b0b-44f3-4355-8171-03da8ba32757
title: Proprietà patch. Context
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Patch.Context
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 7a6495b199046a361910741545a7178050621ccd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324776"
---
# <a name="patchcontext-property"></a>Proprietà patch. Context

La proprietà di **contesto** restituisce il contesto di questa patch.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```JScript
propVal = Patch.Context
```



## <a name="property-value"></a>Valore proprietà

## <a name="remarks"></a>Commenti

Questa proprietà restituisce uno dei valori seguenti.



| Context                        | Valore | Significato                        |
|--------------------------------|-------|--------------------------------|
| \_USERMANAGED MSIINSTALLCONTEXT | 1     | Patch sotto il contesto gestito.   |
| \_utente MSIINSTALLCONTEXT        | 2     | Patch in un contesto non gestito. |
| \_computer MSIINSTALLCONTEXT     | 4     | Patch sotto il contesto del computer.   |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista. Windows Installer 3,0 o versioni successive in Windows Server 2003, Windows XP e Windows 2000<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                                                   |
| IID<br/>     | IID \_ iPatch è definito come 000C10A1-0000-0000-C000-000000000046<br/>                                                                                                                                                                                                            |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Patch (oggetto)**](patch-object.md)
</dt> <dt>

[Non supportato in Windows Installer 2,0 e versioni precedenti](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 





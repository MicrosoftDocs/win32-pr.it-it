---
description: La proprietà Sources enumera tutte le origini per l'istanza della patch. Questa proprietà chiama MsiSourceListEnumSources e restituisce una matrice di stringhe e accetta il tipo di origine come argomento.
ms.assetid: 4a052518-4d76-4a95-be9e-7acae36db626
title: Proprietà patch. Sources
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Patch.Sources
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 18b9e6ab867d68908bc8dd7e7f87f942f8cd015c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325892"
---
# <a name="patchsources-property"></a>Proprietà patch. Sources

La proprietà **Sources** enumera tutte le origini per l'istanza della patch. Questa proprietà chiama [**MsiSourceListEnumSources**](/windows/desktop/api/Msi/nf-msi-msisourcelistenumsourcesa) e restituisce una matrice di stringhe e accetta il tipo di origine come argomento.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```JScript
propVal = Patch.Sources
```



## <a name="property-value"></a>Valore proprietà

Tipo di origine da enumerare. Il valore può essere *msiInstallSourceTypeNetwork* (1) o *msiInstallSourceTypeURL* (2).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista. Windows Installer 3,0 o versioni successive in Windows Server 2003, Windows XP e Windows 2000<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                                                   |
| IID<br/>     | IID \_ iPatch è definito come 000C10A1-0000-0000-C000-000000000046<br/>                                                                                                                                                                                                            |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Patch**](patch-object.md)
</dt> <dt>

[**MsiSourceListEnumSources**](/windows/desktop/api/Msi/nf-msi-msisourcelistenumsourcesa)
</dt> <dt>

[Non supportato in Windows Installer 2,0 e versioni precedenti](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 





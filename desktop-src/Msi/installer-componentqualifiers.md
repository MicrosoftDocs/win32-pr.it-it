---
description: La proprietà ComponentQualifiers è una proprietà di sola lettura che restituisce un oggetto StringList che enumera il set di qualificatori registrati per il componente specificato.
ms.assetid: 49b16c9a-ce84-42ff-af1d-f4ecf7dbe23a
title: Installer.ComponentQualifiers - proprietà
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ComponentQualifiers
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: ff11302b87c144d59129b7041ab75129477e7925b3dd98ce7c740f0c4eda62e1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118632605"
---
# <a name="installercomponentqualifiers-property"></a>Installer.ComponentQualifiers - proprietà

La **proprietà ComponentQualifiers** è una proprietà di sola lettura che restituisce un oggetto [**StringList**](stringlist-object.md) che enumera il set di qualificatori registrati per il componente specificato.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```JScript
propVal = Installer.ComponentQualifiers
```



## <a name="property-value"></a>Valore proprietà

GUID stringa che rappresenta la categoria del [componente](publishcomponent-table.md).

## <a name="remarks"></a>Commenti

Per enumerare i qualificatori, l'applicazione scorre [**l'oggetto StringList**](stringlist-object.md) usando un costrutto For Each. Poiché i qualificatori non sono ordinati, qualsiasi nuovo qualificatore ha un indice arbitrario, ovvero la funzione può restituire qualificatori in qualsiasi ordine.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Programma di installazione 5.0 Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4.0 o Windows Installer 4.5 in Windows Server 2008 o Windows Vista. Windows Programma di installazione Windows Server 2003 o Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller è definito come 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**MsiEnumComponentQualifiers**](/windows/desktop/api/Msi/nf-msi-msienumcomponentqualifiersa)
</dt> </dl>

 

 





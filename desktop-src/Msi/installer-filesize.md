---
description: Il metodo FileSize dell'oggetto Installer usa chiamate api Win32 per restituire le dimensioni del file specificato in Path.
ms.assetid: d7119e5e-9315-4b20-a904-bc1104f3a4e4
title: Metodo Installer.FileSize
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.FileSize
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: f585da776d348e7c774d4671a230881f2ec0e4ddaca8a63842d59a9b77a61972
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118630690"
---
# <a name="installerfilesize-method"></a>Metodo Installer.FileSize

Il **metodo FileSize** dell'oggetto [**Installer**](installer-object.md) usa chiamate api Win32 per restituire le dimensioni del file specificato in *Path*.

## <a name="syntax"></a>Sintassi


```JScript
Installer.FileSize(
  Path
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Percorso* 
</dt> <dd>

Stringa obbligatoria contenente il percorso del file.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Programma di installazione 5.0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Programma di installazione 4.0 o Windows Installer 4.5 in Windows Server 2008 o Windows Vista. Windows Programma di installazione Windows Server 2003 o Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID IInstaller è definito come \_ 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



 

 





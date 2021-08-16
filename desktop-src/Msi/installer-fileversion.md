---
description: Il metodo FileVersion dell'oggetto Installer restituisce la stringa di versione o la stringa di lingua del percorso specificato in Path usando il formato in cui il programma di installazione prevede di trovarli nel database.
ms.assetid: 387cf269-5a7a-476b-811e-d576da1c752f
title: Metodo Installer.FileVersion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.FileVersion
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 492ebb0c7678b7819f3abc423517dcf77d071b81009c3b12017b1b627bb84057
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118630583"
---
# <a name="installerfileversion-method"></a>Metodo Installer.FileVersion

Il **metodo FileVersion** dell'oggetto [**Installer**](installer-object.md) restituisce la stringa di versione o la stringa di lingua del percorso specificato in *Path* usando il formato in cui il programma di installazione prevede di trovarli nel database. Per le versioni, si tratta di una stringa in formato " \# \# . . . \# \# ". Per language, si tratta dell'ID lingua decimale.

## <a name="syntax"></a>Sintassi


```JScript
Installer.FileVersion(
  Path,
  Language
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Percorso* 
</dt> <dd>

Stringa obbligatoria contenente il percorso del file.

</dd> <dt>

*Lingua* 
</dt> <dd>

Flag per indicare se il valore restituito è un ID lingua o una stringa di versione. TRUE restituisce la lingua, FALSE restituisce la versione. Questo parametro è facoltativo e il valore predefinito è FALSE.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Programma di installazione 5.0 Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4.0 o Windows Installer 4.5 in Windows Server 2008 o Windows Vista. Windows Programma di installazione Windows Server 2003 o Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller è definito come 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



 

 





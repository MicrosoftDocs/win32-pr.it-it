---
description: Il metodo FileVersion dell'oggetto Installer restituisce la stringa di versione o la stringa della lingua del percorso specificato nel percorso utilizzando il formato in cui il programma di installazione prevede di trovarle nel database.
ms.assetid: 387cf269-5a7a-476b-811e-d576da1c752f
title: Installer. FileVersion (metodo)
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
ms.openlocfilehash: a36a92b42815a1b2df913ba6bd9f687cdd1b609b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324622"
---
# <a name="installerfileversion-method"></a>Installer. FileVersion (metodo)

Il metodo **fileversion** dell'oggetto [**Installer**](installer-object.md) restituisce la stringa di versione o la stringa della lingua del percorso specificato nel *percorso* utilizzando il formato in cui il programma di installazione prevede di trovarle nel database. Per le versioni, si tratta di una stringa \# nel \# formato ".. \# . \# ". Per la lingua, si tratta dell'ID della lingua decimale.

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

Flag che indica se il valore restituito è un ID lingua o una stringa di versione. TRUE restituisce il linguaggio, FALSE restituisce la versione. Questo parametro è facoltativo e il valore predefinito è FALSE.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista. Windows Installer in Windows Server 2003 o Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller è definito come 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



 

 





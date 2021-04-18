---
description: La proprietà FileAttributes dell'oggetto Installer restituisce un numero che rappresenta gli attributi di file combinati per il percorso designato di un file o di una cartella.
ms.assetid: a09ac346-4e4d-440f-bfbe-ff8fb3f69823
title: Proprietà Installer. FileAttributes (Windows. storage. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.FileAttributes
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: e9a4d2b956c7d325fabcda7d6950274249120a0e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324627"
---
# <a name="installerfileattributes-property"></a>Proprietà Installer. FileAttributes

La proprietà **FileAttributes** dell'oggetto [**Installer**](installer-object.md) restituisce un numero che rappresenta gli attributi di file combinati per il percorso designato di un file o di una cartella.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```JScript
propVal = Installer.FileAttributes
```



## <a name="property-value"></a>Valore proprietà

Percorso necessario del file o della cartella. Un percorso parziale presuppone la directory corrente.

## <a name="remarks"></a>Commenti

La proprietà **FileAttributes** restituisce i valori seguenti.



| Attributo file              | Valore      | Valore |
|-----------------------------|------------|-------|
| FILE\_ATTRIBUTE\_READONLY   | 0x00000001 | 1     |
| FILE\_ATTRIBUTE\_HIDDEN     | 0x00000002 | 2     |
| FILE\_ATTRIBUTE\_SYSTEM     | 0x00000004 | 4     |
| FILE\_ATTRIBUTE\_DIRECTORY  | 0x00000010 | 16    |
| \_attributo file \_ temporaneo  | 0x00000100 | 256   |
| FILE\_ATTRIBUTE\_COMPRESSED | 0x00000800 | 2048  |
| FILE\_ATTRIBUTE\_OFFLINE    | 0x00001000 | 4096  |



 

Restituisce-1 se il file o la cartella non esiste o non è accessibile.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista. Windows Installer in Windows Server 2003 o Windows XP<br/> |
| Intestazione<br/>  | <dl> <dt>Windows. storage. h</dt> </dl>                                                                                                                                                            |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller è definito come 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



 

 





---
description: La proprietà ComponentPath è una proprietà di sola lettura che restituisce il percorso completo di un componente installato. Se il percorso della chiave per il componente è una chiave del registro di sistema, viene restituita la chiave del registro di sistema.
ms.assetid: 6e53419d-f28a-45cd-abc8-0f451177f3fc
title: Proprietà Installer. ComponentPath
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ComponentPath
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: e249290af2477d2dfcbc73f80f80b439f1dd3663
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329027"
---
# <a name="installercomponentpath-property"></a>Proprietà Installer. ComponentPath

La proprietà **ComponentPath** è una proprietà di sola lettura che restituisce il percorso completo di un componente installato. Se il percorso della chiave per il componente è una chiave del registro di sistema, viene restituita la chiave del registro di sistema.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```JScript
propVal = Installer.ComponentPath
```



## <a name="property-value"></a>Valore proprietà

## <a name="remarks"></a>Commenti

Se il componente è una chiave del registro di sistema, le radici del registro di sistema sono rappresentate numericamente. Ad esempio, un percorso del registro di sistema "HKEY \_ Current \_ User \\ software \\ Microsoft" verrebbe restituito come "01: \\ software \\ Microsoft". Le radici del registro di sistema restituite sono definite come segue:



| Radice                    | Valore restituito |
|-------------------------|----------------|
| HKEY\_CLASSI\_RADICE     | 00             |
| HKEY\_CORRENTE\_UTENTE     | 01             |
| HKEY\_LOCALE\_MACCHINA    | 02             |
| HKEY\_UTENTI             | 03             |
| \_dati sulle prestazioni di HKEY \_ | 04             |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista. Windows Installer in Windows Server 2003 o Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller è definito come 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**MsiGetComponentPath**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpatha)
</dt> </dl>

 

 





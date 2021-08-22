---
description: La proprietà ComponentPath è una proprietà di sola lettura che restituisce il percorso completo di un componente installato. Se il percorso della chiave per il componente è una chiave del Registro di sistema, viene restituita la chiave del Registro di sistema.
ms.assetid: 6e53419d-f28a-45cd-abc8-0f451177f3fc
title: Proprietà Installer.ComponentPath
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
ms.openlocfilehash: 88601dc4c65d0d3f69a5386ed62d1523c9fa21723e73b1ad4d208d0eff437658
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118632624"
---
# <a name="installercomponentpath-property"></a>Proprietà Installer.ComponentPath

La **proprietà ComponentPath** è una proprietà di sola lettura che restituisce il percorso completo di un componente installato. Se il percorso della chiave per il componente è una chiave del Registro di sistema, viene restituita la chiave del Registro di sistema.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```JScript
propVal = Installer.ComponentPath
```



## <a name="property-value"></a>Valore proprietà

## <a name="remarks"></a>Commenti

Se il componente è una chiave del Registro di sistema, le radici del Registro di sistema vengono rappresentate numericamente. Ad esempio, un percorso del Registro di sistema "HKEY CURRENT USER SOFTWARE Microsoft" verrebbe restituito \_ \_ come \\ \\ "01: \\ SOFTWARE \\ Microsoft". Le radici del Registro di sistema restituite sono definite come segue:



| Radice                    | Valore restituito |
|-------------------------|----------------|
| HKEY\_CLASSI\_RADICE     | 00             |
| HKEY\_CORRENTE\_UTENTE     | 01             |
| HKEY\_LOCALE\_MACCHINA    | 02             |
| HKEY\_UTENTI             | 03             |
| DATI SULLE PRESTAZIONI DI \_ \_ HKEY | 04             |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Programma di installazione 5.0 Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Programma di installazione 4.0 o Windows Installer 4.5 in Windows Server 2008 o Windows Vista. Windows Programma di installazione Windows Server 2003 o Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID IInstaller è definito come \_ 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**MsiGetComponentPath**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpatha)
</dt> </dl>

 

 





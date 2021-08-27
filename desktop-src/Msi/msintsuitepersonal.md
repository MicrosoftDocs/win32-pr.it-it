---
description: Nei Windows XP e versioni successive, il programma di installazione imposta la proprietà MsiNTSuitePersonal su 1 se il sistema operativo è Windows XP Home Edition.
ms.assetid: 324a4c45-bd64-4361-90ba-6a0554a9c5ef
title: MsiNTSuitePersonal - proprietà
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c946b707e0d66a2c5bd3cd9cb6bf75828be9dd8f21e0e81080910a9fac73d353
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118944495"
---
# <a name="msintsuitepersonal-property"></a>MsiNTSuitePersonal - proprietà

Nei Windows XP e versioni successive, il programma di installazione imposta la proprietà **MsiNTSuitePersonal** su 1 se il sistema operativo è Windows XP Home Edition. Il programma di installazione imposta questa proprietà su 1 solo se il flag VER \_ SUITE PERSONAL è impostato nella struttura \_ [**OSVERSIONINFOEX.**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa) In caso contrario, il programma di installazione non imposta questa proprietà.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Programma di installazione 5.0 Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Programma di installazione 4.0 o Windows Installer 4.5 in Windows Server 2008 o Windows Vista. Windows Programma di installazione Windows Server 2003 o Windows XP. Vedere i [Windows di installazione Run-Time](windows-installer-portal.md) per informazioni sul Service Pack Windows minimo richiesto da una versione Windows Installer.<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà](properties.md)
</dt> </dl>

 

 

---
description: Il programma di installazione imposta la proprietà MsiTabletPC su un valore diverso da zero se il sistema operativo corrente è Windows XP Tablet PC Edition.
ms.assetid: b178a98e-b6f8-4ff8-b554-e47c3b39f892
title: MsiTabletPC - proprietà
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac47dd0d8db3c0e882a965685bb1507dc0103f3e965dfbcb8f4857ada19e17ad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119145611"
---
# <a name="msitabletpc-property"></a>MsiTabletPC - proprietà

Il programma di installazione imposta **la proprietà MsiTabletPC** su un valore diverso da zero se il sistema operativo corrente Windows XP Tablet PC Edition. Il programma di installazione usa la [**funzione GetSystemMetrics**](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) con **SM \_ TABLETPC** e la proprietà riceve il valore diverso da zero restituito da questa funzione. Se il sistema corrente non è Windows XP Tablet PC Edition, la **funzione GetSystemMetrics** restituisce zero e il programma di installazione non imposta questa proprietà.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Programma di installazione 5.0 Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Programma di installazione 4.0 o Windows Installer 4.5 in Windows Server 2008 o Windows Vista. Windows Programma di installazione 4.5 in Windows Server 2003 o Windows XP. Vedere i [Windows di installazione Run-Time](windows-installer-portal.md) per informazioni sul Service Pack Windows minimo richiesto da una versione Windows Installer.<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà](properties.md)
</dt> <dt>

[Non supportato in Windows Installer 3.1 e versioni precedenti](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 

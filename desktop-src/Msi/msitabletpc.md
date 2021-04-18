---
description: Il programma di installazione imposta la proprietà MsiTabletPC su un valore diverso da zero se il sistema operativo corrente è Windows XP Tablet PC Edition.
ms.assetid: b178a98e-b6f8-4ff8-b554-e47c3b39f892
title: Proprietà MsiTabletPC
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0bf2878dbaa895e0924a50900d331db0b879edc1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331075"
---
# <a name="msitabletpc-property"></a>Proprietà MsiTabletPC

Il programma di installazione imposta la proprietà **MsiTabletPC** su un valore diverso da zero se il sistema operativo corrente è Windows XP Tablet PC Edition. Il programma di installazione utilizza la funzione [**GetSystemMetrics**](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) con **SM \_ TABLETPC** e la proprietà riceve il valore diverso da zero restituito da questa funzione. Se il sistema corrente non è Windows XP Tablet PC Edition, la funzione **GetSystemMetrics** restituisce zero e il programma di installazione non imposta questa proprietà.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista. Windows Installer 4,5 in Windows Server 2003 o Windows XP. Vedere i [requisiti di Run-Time Windows Installer](windows-installer-portal.md) per informazioni sul Service Pack minimo di Windows richiesto da una versione Windows Installer.<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà](properties.md)
</dt> <dt>

[Non supportato in Windows Installer 3,1 e versioni precedenti](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 

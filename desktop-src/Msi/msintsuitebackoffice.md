---
description: Nei Windows 2000 e versioni successive, il programma di installazione imposta la proprietà MsiNTSuiteBackOffice su 1 se sono installati i componenti Microsoft BackOffice.
ms.assetid: 31493732-3082-4dd9-9a20-21658f53c8c2
title: MsiNTSuiteBackOffice - proprietà
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5cf3c65e1f5d1d528dd35232900a9aef12bdf344d1d2859eef814d1030e6249d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118944826"
---
# <a name="msintsuitebackoffice-property"></a>MsiNTSuiteBackOffice - proprietà

Nei Windows 2000 e versioni successive, il programma di installazione imposta la proprietà **MsiNTSuiteBackOffice** su 1 se sono installati i componenti Microsoft BackOffice. Il programma di installazione imposta questa proprietà su 1 solo se il \_ flag VER SUITE \_ BACKOFFICE è impostato nella struttura [**OSVERSIONINFOEX.**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa) In caso contrario, il programma di installazione non imposta questa proprietà.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Programma di installazione 5.0 Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4.0 o Windows Installer 4.5 in Windows Server 2008 o Windows Vista. Windows Programma di installazione Windows Server 2003 o Windows XP. Per informazioni [Windows service](windows-installer-portal.md) pack minimo necessario per Run-Time versione del programma di installazione di Windows, vedere i requisiti minimi Windows Service Pack.<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà](properties.md)
</dt> </dl>

 

 

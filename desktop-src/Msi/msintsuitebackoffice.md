---
description: In Windows 2000 e nei sistemi operativi successivi il programma di installazione imposta la proprietà MsiNTSuiteBackOffice su 1 se sono installati i componenti di Microsoft BackOffice.
ms.assetid: 31493732-3082-4dd9-9a20-21658f53c8c2
title: Proprietà MsiNTSuiteBackOffice
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bf2d9f2f1d95446c32b4f2addf520f3d5b4dadc3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332612"
---
# <a name="msintsuitebackoffice-property"></a>Proprietà MsiNTSuiteBackOffice

In Windows 2000 e nei sistemi operativi successivi il programma di installazione imposta la proprietà **MsiNTSuiteBackOffice** su 1 se sono installati i componenti di Microsoft BackOffice. Il programma di installazione imposta questa proprietà su 1 solo se \_ il \_ flag di versione BackOffice di ver Suite è impostato nella struttura [**OSVERSIONINFOEX**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa) . In caso contrario, il programma di installazione non imposta questa proprietà.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista. Windows Installer in Windows Server 2003 o Windows XP. Vedere i [requisiti di Run-Time Windows Installer](windows-installer-portal.md) per informazioni sul Service Pack minimo di Windows richiesto da una versione Windows Installer.<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà](properties.md)
</dt> </dl>

 

 

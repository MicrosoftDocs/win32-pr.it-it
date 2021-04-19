---
description: In Windows 2000 e nei sistemi operativi successivi il programma di installazione imposta la proprietà MsiNTSuiteDataCenter su 1 se è installato Windows 2000 Datacenter Server.
ms.assetid: a777e62a-a360-4d8c-b7a6-00d45c17db66
title: Proprietà MsiNTSuiteDataCenter
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 106b9119885e15b94bf5d8f2cd4b6954d0891d98
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332609"
---
# <a name="msintsuitedatacenter-property"></a>Proprietà MsiNTSuiteDataCenter

In Windows 2000 e nei sistemi operativi successivi il programma di installazione imposta la proprietà **MsiNTSuiteDataCenter** su 1 se è installato Windows 2000 Datacenter Server. Il programma di installazione imposta questa proprietà su 1 solo se \_ il \_ flag del Data Center di ver Suite è impostato nella struttura [**OSVERSIONINFOEX**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa) . In caso contrario, il programma di installazione non imposta questa proprietà.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista. Windows Installer in Windows Server 2003 o Windows XP. Vedere i [requisiti di Run-Time Windows Installer](windows-installer-portal.md) per informazioni sul Service Pack minimo di Windows richiesto da una versione Windows Installer.<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà](properties.md)
</dt> </dl>

 

 

---
description: Nei Windows 2000 e versioni successive il programma di installazione imposta la proprietà MsiNTSuiteSmallBusiness su 1 se è installato Microsoft Small Business Server.
ms.assetid: 9ac578b9-316f-413c-aae0-4f414109583b
title: MsiNTSuiteSmallBusiness - proprietà
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c1e0dab7d024753a30d6a640cefd1652de137b5cd230a772a5041927dc0e725e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120082741"
---
# <a name="msintsuitesmallbusiness-property"></a>MsiNTSuiteSmallBusiness - proprietà

Nei Windows 2000 e versioni successive il programma di installazione imposta la proprietà **MsiNTSuiteSmallBusiness** su 1 se è installato Microsoft Small Business Server. Il programma di installazione imposta questa proprietà su 1 solo se il flag SMALLBUSINESS di VER SUITE è \_ \_ impostato nella struttura [**OSVERSIONINFOEX.**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa) In caso contrario, il programma di installazione non imposta questa proprietà.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Programma di installazione 5.0 Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4.0 o Windows Installer 4.5 in Windows Server 2008 o Windows Vista. Windows Programma di installazione Windows Server 2003 o Windows XP. Per informazioni [Windows service](windows-installer-portal.md) pack minimo necessario per Run-Time versione del programma di installazione di Windows, vedere i requisiti minimi Windows Service Pack.<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà](properties.md)
</dt> </dl>

 

 

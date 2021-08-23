---
description: In Windows 2000 e versioni successive, il programma di installazione imposta la proprietà MsiNTSuiteEnterprise su 1 se Windows 2000 Advanced Server è installato.
ms.assetid: f5384467-3791-4b0b-a70e-b5343c70db46
title: MsiNTSuiteEnterprise - proprietà
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 242bf1c95db7d4101362a7b72b4cfa99009a93cc2fa399d1b4b81d93aabbd16c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118944654"
---
# <a name="msintsuiteenterprise-property"></a>MsiNTSuiteEnterprise - proprietà

Nei Windows 2000 e versioni successive il programma di installazione imposta la proprietà **MsiNTSuiteEnterprise** su 1 se Windows 2000 Advanced Server è installato. Il programma di installazione imposta questa proprietà su 1 solo se il flag VER \_ SUITE ENTERPRISE è impostato nella struttura \_ [**OSVERSIONINFOEX.**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa) In caso contrario, il programma di installazione non imposta questa proprietà.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Programma di installazione 5.0 Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4.0 o Windows Installer 4.5 in Windows Server 2008 o Windows Vista. Windows Programma di installazione Windows Server 2003 o Windows XP. Per informazioni [Windows service](windows-installer-portal.md) pack minimo necessario per Run-Time versione del programma di installazione di Windows, vedere i requisiti minimi Windows Service Pack.<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà](properties.md)
</dt> </dl>

 

 

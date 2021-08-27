---
description: In Windows 2000 e versioni successive il programma di installazione imposta la proprietà MsiNTSuiteWebServer su 1 se il programma di installazione è in esecuzione in un'edizione Web di Windows Server 2003.
ms.assetid: de462ba2-4654-4f47-9dd7-3bc9c6f0af0e
title: MsiNTSuiteWebServer - proprietà
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 60c920dc97733a6a8bc134f2ac0c76d449afd6a5ce39e5f8e0555d30daa78952
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120129221"
---
# <a name="msintsuitewebserver-property"></a>MsiNTSuiteWebServer - proprietà

Nei sistemi operativi Windows 2000 e versioni successive, il programma di installazione imposta la proprietà **MsiNTSuiteWebServer** su 1 se il programma di installazione è in esecuzione in un'edizione Web di Windows Server 2003. Il programma di installazione imposta questa proprietà su 1 solo se il flag BLADE di VER \_ SUITE è impostato nella struttura \_ [**OSVERSIONINFOEX.**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa) In caso contrario, il programma di installazione non imposta questa proprietà.

## <a name="remarks"></a>Commenti

Questa proprietà è disponibile solo con la versione Windows Server 2003 del programma di installazione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Programma di installazione 5.0 Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4.0 o Windows Installer 4.5 in Windows Server 2008 o Windows Vista. Windows Programma di installazione Windows Server 2003 o Windows XP. Per informazioni [Windows service](windows-installer-portal.md) pack minimo necessario per Run-Time versione del programma di installazione di Windows, vedere i requisiti minimi Windows Service Pack.<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà](properties.md)
</dt> <dt>

[Non supportato in Windows Installer 2.0 e versioni precedenti](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 

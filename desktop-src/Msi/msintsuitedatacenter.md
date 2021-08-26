---
description: Nei Windows 2000 e versioni successive, il programma di installazione imposta la proprietà MsiNTSuiteDataCenter su 1 se Windows 2000 Datacenter Server è installato.
ms.assetid: a777e62a-a360-4d8c-b7a6-00d45c17db66
title: MsiNTSuiteDataCenter - proprietà
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b42edc0a4abb544133b4b7fb176988f826c5af172cc4c0d49ca56494ed37672
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120082811"
---
# <a name="msintsuitedatacenter-property"></a>MsiNTSuiteDataCenter - proprietà

Nei Windows 2000 e versioni successive, il programma di installazione imposta la proprietà **MsiNTSuiteDataCenter** su 1 se Windows 2000 Datacenter Server è installato. Il programma di installazione imposta questa proprietà su 1 solo se il flag VER \_ SUITE DATACENTER è impostato nella struttura \_ [**OSVERSIONINFOEX.**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa) In caso contrario, il programma di installazione non imposta questa proprietà.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Programma di installazione 5.0 Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Programma di installazione 4.0 o Windows Installer 4.5 in Windows Server 2008 o Windows Vista. Windows Programma di installazione Windows Server 2003 o Windows XP. Vedere i [Windows di installazione Run-Time](windows-installer-portal.md) per informazioni sul Service Pack Windows minimo richiesto da una versione Windows Installer.<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà](properties.md)
</dt> </dl>

 

 

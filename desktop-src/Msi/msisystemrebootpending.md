---
description: Il programma di installazione imposta il valore della proprietà MsiSystemRebootPending su 1 se è presente un'operazione in sospeso per rinominare un file.
ms.assetid: 8bbbf42e-fb55-4e5d-a574-2c3aaa87a73a
title: MsiSystemRebootPending - proprietà
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b6cab600ca7c0f1bbc240f8fb1a9d93f3da62914e8250863333b75f8973d6c1d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120042651"
---
# <a name="msisystemrebootpending-property"></a>MsiSystemRebootPending - proprietà

Il programma di installazione imposta il valore della **proprietà MsiSystemRebootPending** su 1 se è presente un'operazione in sospeso per rinominare un file.

Gli autori di pacchetti possono basare una condizione nella tabella [LaunchCondition](launchcondition-table.md) su questa proprietà per impedire l'installazione del pacchetto nei casi in cui è in sospeso un'operazione per rinominare un file. Questa operazione può essere eseguita per impedire un riavvio del sistema operativo causato dalla ridenominazione del file. Il programma di installazione non imposta la **proprietà MsiSystemRebootPending** in tutti i casi che richiedono un riavvio del sistema.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Programma di installazione 5.0 Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4.0 o Windows Installer 4.5 in Windows Server 2008 o Windows Vista. Windows Programma di installazione 4.5 Windows Server 2003 o Windows XP. Per informazioni [Windows service](windows-installer-portal.md) pack minimo necessario per Run-Time versione del programma di installazione di Windows, vedere i requisiti minimi Windows Service Pack.<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà](properties.md)
</dt> <dt>

[Riavvii del sistema](system-reboots.md)
</dt> <dt>

[Non supportato in Windows Installer 3.1 e versioni precedenti](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 





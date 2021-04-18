---
description: Il programma di installazione imposta il valore della proprietà MsiSystemRebootPending su 1 se è presente un'operazione in sospeso per rinominare un file.
ms.assetid: 8bbbf42e-fb55-4e5d-a574-2c3aaa87a73a
title: Proprietà MsiSystemRebootPending
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dec5db7550be3fa27b0ed272ff08d88a4cad915a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330484"
---
# <a name="msisystemrebootpending-property"></a>Proprietà MsiSystemRebootPending

Il programma di installazione imposta il valore della proprietà **MsiSystemRebootPending** su 1 se è presente un'operazione in sospeso per rinominare un file.

Gli autori di pacchetti possono basare una condizione nella [tabella LaunchCondition](launchcondition-table.md) in questa proprietà per impedire l'installazione del pacchetto nei casi in cui è presente un'operazione in sospeso per rinominare un file. Questa operazione può essere eseguita per impedire il riavvio del sistema operativo causato dalla ridenominazione del file. Il programma di installazione non imposta la proprietà **MsiSystemRebootPending** in tutti i casi che richiedono il riavvio del sistema.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista. Windows Installer 4,5 in Windows Server 2003 o Windows XP. Vedere i [requisiti di Run-Time Windows Installer](windows-installer-portal.md) per informazioni sul Service Pack minimo di Windows richiesto da una versione Windows Installer.<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà](properties.md)
</dt> <dt>

[Riavvio del sistema](system-reboots.md)
</dt> <dt>

[Non supportato in Windows Installer 3,1 e versioni precedenti](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 





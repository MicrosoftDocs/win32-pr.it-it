---
description: Il programma di installazione imposta la proprietà OutOfNoRbDiskSpace su true se un volume di destinazione dell'installazione non dispone di spazio su disco sufficiente per gestire l'installazione.
ms.assetid: 910d6c1d-38d3-4680-b256-2bf30689ce11
title: Proprietà OutOfNoRbDiskSpace
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8fa9cdd7c1d444e141103ca148344dd26ea1d2a5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330473"
---
# <a name="outofnorbdiskspace-property"></a>Proprietà OutOfNoRbDiskSpace

Il programma di installazione imposta la proprietà **OutOfNoRbDiskSpace** su true se un volume di destinazione dell'installazione non dispone di spazio su disco sufficiente per gestire l'installazione. In questo caso, la proprietà **OutOfNoRbDiskSpace** è impostata su true anche se il rollback è stato disabilitato. Se lo spazio disponibile è sufficiente per tutti i volumi, il valore è false.

Uno sviluppatore di un pacchetto di installazione può gestire la situazione in cui la proprietà [**OutOfDiskSpace**](outofdiskspace.md) è true e la proprietà **OutOfNoRbDiskSpace** è false creando un'interfaccia utente che presenta all'utente l'opzione per disabilitare il rollback e continuare l'installazione. Per informazioni sulla visualizzazione condizionale di una finestra di dialogo, vedere [Panoramica di ControlEvent](controlevent-overview.md). Per informazioni sulla disabilitazione del rollback, vedere [EnableRollback ControlEvent](enablerollback-controlevent.md).

La proprietà **OutOfNoRbDiskSpace** è valida in qualsiasi momento dopo l'esecuzione dell' [azione CostFinalize secondo](costfinalize-action.md) . Lo stato della proprietà **OutOfNoRbDiskSpace** viene aggiornato dinamicamente ogni volta che il costo di installazione totale viene ricalcolato (ad esempio, ogni volta che lo stato di installazione di qualsiasi funzionalità viene modificato tramite la [finestra di dialogo di selezione](selection-dialog.md)). Azioni di risoluzione selezione utilizzare questo valore per annullare un'installazione e generare una finestra di dialogo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista. Windows Installer in Windows Server 2003 o Windows XP. Vedere i [requisiti di Run-Time Windows Installer](windows-installer-portal.md) per informazioni sul Service Pack minimo di Windows richiesto da una versione Windows Installer.<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà](properties.md)
</dt> <dt>

[Panoramica di ControlEvent](controlevent-overview.md)
</dt> <dt>

[**Proprietà OutOfDiskSpace**](outofdiskspace.md)
</dt> <dt>

[ControlEvent EnableRollback](enablerollback-controlevent.md)
</dt> <dt>

[Azione CostFinalize secondo](costfinalize-action.md)
</dt> <dt>

[Finestra di dialogo di selezione](selection-dialog.md)
</dt> </dl>

 

 





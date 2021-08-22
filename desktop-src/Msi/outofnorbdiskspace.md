---
description: Il programma di installazione imposta la proprietà OutOfNoRbDiskSpace su True se qualsiasi volume di destinazione dell'installazione non dispone di spazio su disco sufficiente per supportare l'installazione.
ms.assetid: 910d6c1d-38d3-4680-b256-2bf30689ce11
title: OutOfNoRbDiskSpace - proprietà
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 275eec4c78a1fe0074fe8e91f7dcab3b660cade46eb8810aa992edf6a45fb989
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118942771"
---
# <a name="outofnorbdiskspace-property"></a>OutOfNoRbDiskSpace - proprietà

Il programma di installazione imposta la **proprietà OutOfNoRbDiskSpace** su True se qualsiasi volume di destinazione dell'installazione non dispone di spazio su disco sufficiente per supportare l'installazione. In questo caso, la **proprietà OutOfNoRbDiskSpace** è impostata su True anche se il rollback è stato disabilitato. Se tutti i volumi hanno spazio sufficiente, il valore è False.

Uno sviluppatore di un pacchetto di installazione può gestire la situazione quando la proprietà [**OutOfDiskSpace**](outofdiskspace.md) è True e la **proprietà OutOfNoRbDiskSpace** è False tramite la creazione di un'interfaccia utente che presenta all'utente un'opzione per disabilitare il rollback e continuare l'installazione. Per informazioni sulla visualizzazione condizionale di una finestra di dialogo, vedere [Cenni preliminari su ControlEvent](controlevent-overview.md). Per informazioni sulla disabilitazione del rollback, vedere [EnableRollback ControlEvent](enablerollback-controlevent.md).

La **proprietà OutOfNoRbDiskSpace** è valida in qualsiasi momento dopo l'esecuzione dell'azione [CostFinalize.](costfinalize-action.md) Lo stato della proprietà **OutOfNoRbDiskSpace** viene aggiornato dinamicamente ogni volta che viene ricalcolato il costo totale di installazione, ad esempio ogni volta che lo stato di installazione di qualsiasi funzionalità viene modificato tramite la finestra di dialogo Selezione [.](selection-dialog.md) Le azioni di risoluzione della selezione usano questo valore per annullare un'installazione e generare una finestra di dialogo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Programma di installazione 5.0 Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Programma di installazione 4.0 o Windows Installer 4.5 in Windows Server 2008 o Windows Vista. Windows Programma di installazione Windows Server 2003 o Windows XP. Vedere i [Windows di installazione Run-Time](windows-installer-portal.md) per informazioni sul Service Pack Windows minimo richiesto da una versione Windows Installer.<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà](properties.md)
</dt> <dt>

[Cenni preliminari su ControlEvent](controlevent-overview.md)
</dt> <dt>

[**OutOfDiskSpace - proprietà**](outofdiskspace.md)
</dt> <dt>

[EnableRollback ControlEvent](enablerollback-controlevent.md)
</dt> <dt>

[Azione CostFinalize](costfinalize-action.md)
</dt> <dt>

[Finestra di dialogo Di selezione](selection-dialog.md)
</dt> </dl>

 

 





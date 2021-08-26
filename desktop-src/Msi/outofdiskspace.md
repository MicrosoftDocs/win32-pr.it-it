---
description: Il programma di installazione imposta la proprietà OutOfDiskSpace su TRUE se uno dei volumi di destinazione dell'installazione corrente non dispone di spazio su disco sufficiente per supportare l'installazione.
ms.assetid: fb1e3be7-12dd-4036-b657-b91b480fca4a
title: OutOfDiskSpace - proprietà
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a99146d08722038bbc2d9b1e0d7b32fd8b587126b0fc942e14823909a2aef79
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120042581"
---
# <a name="outofdiskspace-property"></a>OutOfDiskSpace - proprietà

Il programma di installazione imposta la **proprietà OutOfDiskSpace** su TRUE se uno dei volumi di destinazione dell'installazione corrente non dispone di spazio su disco sufficiente per supportare l'installazione. Se tutti i volumi hanno spazio sufficiente, il valore è FALSE. Le azioni di risoluzione della selezione usano questo valore per annullare un'installazione e generare una finestra di dialogo.

Questa proprietà è valida in qualsiasi momento dopo [l'esecuzione dell'azione CostFinalize.](costfinalize-action.md) Lo stato della proprietà [**OutOfNoRbDiskSpace**](outofnorbdiskspace.md) viene aggiornato dinamicamente ogni volta che viene ricalcolato il costo totale di installazione, ad esempio ogni volta che lo stato di installazione di qualsiasi funzionalità viene modificato tramite la finestra di dialogo [Selezione.](selection-dialog.md)

## <a name="remarks"></a>Commenti

Qualsiasi finestra di dialogo che si basa sulla proprietà **OutOfDiskSpace** per determinare se visualizzare una finestra di dialogo deve impostare Il bit di stile della finestra di dialogo [TrackDiskSpace](trackdiskspace-dialog-style-bit.md) per aggiornare dinamicamente lo spazio nei volumi di destinazione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Programma di installazione 5.0 Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4.0 o Windows Installer 4.5 in Windows Server 2008 o Windows Vista. Windows Programma di installazione Windows Server 2003 o Windows XP. Vedere i [Windows di installazione Run-Time](windows-installer-portal.md) per informazioni sul Service Pack minimo Windows richiesto da una versione Windows Installer.<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà](properties.md)
</dt> </dl>

 

 





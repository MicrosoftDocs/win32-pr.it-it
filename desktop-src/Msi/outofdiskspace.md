---
description: Il programma di installazione imposta la proprietà OutOfDiskSpace su TRUE se un volume di destinazione dell'installazione corrente non dispone di spazio su disco sufficiente per gestire l'installazione.
ms.assetid: fb1e3be7-12dd-4036-b657-b91b480fca4a
title: Proprietà OutOfDiskSpace
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b3a438661e931547b0025f2bf85a2ccc03899f5a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327803"
---
# <a name="outofdiskspace-property"></a>Proprietà OutOfDiskSpace

Il programma di installazione imposta la proprietà **OutOfDiskSpace** su true se un volume di destinazione dell'installazione corrente non dispone di spazio su disco sufficiente per gestire l'installazione. Se lo spazio disponibile è sufficiente per tutti i volumi, il valore è FALSE. Azioni di risoluzione selezione utilizzare questo valore per annullare un'installazione e generare una finestra di dialogo.

Questa proprietà è valida in qualsiasi momento dopo l'esecuzione dell' [azione CostFinalize secondo](costfinalize-action.md) . Lo stato della proprietà [**OutOfNoRbDiskSpace**](outofnorbdiskspace.md) viene aggiornato dinamicamente ogni volta che il costo di installazione totale viene ricalcolato (ad esempio, ogni volta che lo stato di installazione di qualsiasi funzionalità viene modificato tramite la finestra di dialogo di [selezione](selection-dialog.md) ).

## <a name="remarks"></a>Commenti

Qualsiasi finestra di dialogo che si basa sulla proprietà **OutOfDiskSpace** per determinare se visualizzare una finestra di dialogo deve impostare il [bit di stile della finestra](trackdiskspace-dialog-style-bit.md) di dialogo TrackDiskSpace per la finestra di dialogo per aggiornare in modo dinamico lo spazio sui volumi di destinazione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista. Windows Installer in Windows Server 2003 o Windows XP. Vedere i [requisiti di Run-Time Windows Installer](windows-installer-portal.md) per informazioni sul Service Pack minimo di Windows richiesto da una versione Windows Installer.<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà](properties.md)
</dt> </dl>

 

 





---
description: La proprietà CostingComplete indica se il programma di installazione ha completato la determinazione dei costi dello spazio su disco.
ms.assetid: 23688f1e-3ae8-4cd9-824c-36077cc7838f
title: CostingComplete - proprietà
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5a512621e187be9897c07106ade8c6012d4ac4fa43543d71cb856e90027d549
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118948358"
---
# <a name="costingcomplete-property"></a>CostingComplete - proprietà

La **proprietà CostingComplete** indica se il programma di installazione ha completato la determinazione dei costi dello spazio su disco. Questa proprietà può essere usata per creare una finestra di dialogo attivata se la determinazione dei costi non è stata completata. La proprietà viene impostata dinamicamente durante la determinazione dei costi dello spazio su disco e viene impostata su 1 non appena la determinazione dei costi è completa. Questa proprietà viene inizializzata su 0 [dall'azione CostFinalize](costfinalize-action.md).

## <a name="remarks"></a>Commenti

Per un esempio di come creare un oggetto "Attendere. . . " finestra di dialogo che viene visualizzata durante il costo dello spazio su disco, vedere la sezione Creazione di un condizionale ["Attendere. . ." Finestra di messaggio](authoring-a-conditional-please-wait-------message-box.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Programma di installazione 5.0 Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Programma di installazione 4.0 o Windows Installer 4.5 in Windows Server 2008 o Windows Vista. Windows Programma di installazione Windows Server 2003 o Windows XP. Vedere i [Windows di installazione Run-Time](windows-installer-portal.md) per informazioni sul Service Pack Windows minimo richiesto da una versione Windows Installer.<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà](properties.md)
</dt> </dl>

 

 





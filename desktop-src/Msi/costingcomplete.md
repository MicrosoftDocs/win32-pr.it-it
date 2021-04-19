---
description: La proprietà CostingComplete indica se il programma di installazione ha completato il costo dello spazio su disco.
ms.assetid: 23688f1e-3ae8-4cd9-824c-36077cc7838f
title: Proprietà CostingComplete
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 817b4d38b71e377bbf9b51588efef33e4fd6e93e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326773"
---
# <a name="costingcomplete-property"></a>Proprietà CostingComplete

La proprietà **CostingComplete** indica se il programma di installazione ha completato il costo dello spazio su disco. Questa proprietà può essere utilizzata per creare una finestra di dialogo attivata se i costi non sono stati completati. La proprietà viene impostata in modo dinamico durante il costo dello spazio su disco e viene impostata su 1 non appena il costo è completo. Questa proprietà viene inizializzata su 0 dall' [azione CostFinalize secondo](costfinalize-action.md).

## <a name="remarks"></a>Commenti

Per un esempio di come creare un'attesa. . . "la finestra di dialogo visualizzata durante i costi di spazio su disco, vedere la sezione [creazione di un condizionale" attendere... " MessageBox](authoring-a-conditional-please-wait-------message-box.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista. Windows Installer in Windows Server 2003 o Windows XP. Vedere i [requisiti di Run-Time Windows Installer](windows-installer-portal.md) per informazioni sul Service Pack minimo di Windows richiesto da una versione Windows Installer.<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà](properties.md)
</dt> </dl>

 

 





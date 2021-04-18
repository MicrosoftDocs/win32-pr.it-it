---
description: Per disabilitare l'interfaccia utente incorporata per l'installazione definita nella tabella MsiEmbeddedUI, impostare la proprietà MSIDISABLEEEUI su 1 nella riga di comando.
ms.assetid: c5ada690-c5dd-455f-babe-8c09750525c4
title: Proprietà MSIDISABLEEEUI
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d89ce43f649d406e4ae086db236375c02c43e2d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329344"
---
# <a name="msidisableeeui-property"></a>Proprietà MSIDISABLEEEUI

Per disabilitare l'interfaccia utente incorporata per l'installazione definita nella [tabella MsiEmbeddedUI](msiembeddedui-table.md), impostare la proprietà MSIDISABLEEEUI su 1 nella riga di comando.

**[Windows Installer 4,0 e versioni precedenti](not-supported-in-windows-installer-4-0.md):** Non supportato. Le versioni precedenti a Windows Installer 4,5 ignorano la proprietà MSIDISABLEEEUI.

## <a name="remarks"></a>Commenti

In un'installazione a più pacchetti, un pacchetto figlio deve in genere usare l'interfaccia utente del pacchetto padre e non inizializzare la propria interfaccia utente incorporata. Se la proprietà MSIDISABLEEEUI non è impostata nel pacchetto padre, per impostazione predefinita il pacchetto figlio utilizza l'interfaccia utente incorporata del pacchetto padre e ignora la proprietà MSIDISABLEEEUI all'interno del pacchetto figlio.

La proprietà MSIDISABLEEEUI Disabilita l'interfaccia utente incorporata per un singolo pacchetto. È possibile utilizzare il criterio [MsiDisableEmbeddedUI](msidisableembeddedui.md) per disabilitare le interfacce utente incorporate per tutti i pacchetti nel computer.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,5 in Windows Server 2008, Windows Vista, Windows Server 2003 e Windows XP. Vedere i [requisiti di Run-Time Windows Installer](windows-installer-portal.md) per informazioni sul Service Pack minimo di Windows richiesto da una versione Windows Installer.<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà](properties.md)
</dt> </dl>

 

 





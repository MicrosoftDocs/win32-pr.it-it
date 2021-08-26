---
description: Per disabilitare l'interfaccia utente incorporata per l'installazione definita nella tabella MsiEmbeddedUI, impostare la proprietà MSIDISABLEEEUI su 1 nella riga di comando.
ms.assetid: c5ada690-c5dd-455f-babe-8c09750525c4
title: MsiDISABLEEEUI - proprietà
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb1e599ed0786c7d2c55644eb5759db3917757d3b41f6107161d72a3cc559484
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120039951"
---
# <a name="msidisableeeui-property"></a>MsiDISABLEEEUI - proprietà

Per disabilitare l'interfaccia utente incorporata per l'installazione definita nella tabella [MsiEmbeddedUI](msiembeddedui-table.md), impostare la proprietà MSIDISABLEEEUI su 1 nella riga di comando.

**[Windows Installer 4.0 e versioni precedenti:](not-supported-in-windows-installer-4-0.md)** Non supportato. Le versioni precedenti Windows Installer 4.5 ignorano la proprietà MSIDISABLEEEUI.

## <a name="remarks"></a>Commenti

In un'installazione a più pacchetti, un pacchetto figlio deve in genere usare l'interfaccia utente del pacchetto padre e non inizializzare la propria interfaccia utente incorporata. Se la proprietà MSIDISABLEEEUI non è impostata all'interno del pacchetto padre, il pacchetto figlio usa l'interfaccia utente incorporata del pacchetto padre per impostazione predefinita e ignora la proprietà MSIDISABLEEEUI all'interno del pacchetto figlio.

La proprietà MSIDISABLEEEUI disabilita l'interfaccia utente incorporata per un singolo pacchetto. È possibile usare il [criterio MsiDisableEmbeddedUI](msidisableembeddedui.md) per disabilitare le interfacce utente incorporate per tutti i pacchetti nel computer.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Programma di installazione 5.0 Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Programma di installazione 4.5 in Windows Server 2008, Windows Vista, Windows Server 2003 e Windows XP. Vedere i [Windows di installazione Run-Time](windows-installer-portal.md) per informazioni sul Service Pack Windows minimo richiesto da una versione Windows Installer.<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà](properties.md)
</dt> </dl>

 

 





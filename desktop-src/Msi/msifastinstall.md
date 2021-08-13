---
description: La proprietà MSIFASTINSTALL può essere usata per ridurre il tempo necessario per installare un pacchetto di installazione di Windows di grandi dimensioni.
ms.assetid: 011668da-da04-4b80-989e-192b0daa3060
title: MSIFASTINSTALL - proprietà
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd28c731d34e769f0612acc12586349247231bce663036d3577f41df6a7256f9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118628504"
---
# <a name="msifastinstall-property"></a>MSIFASTINSTALL - proprietà

La **proprietà MSIFASTINSTALL** può essere usata per ridurre il tempo necessario per installare un pacchetto di installazione di Windows di grandi dimensioni. La proprietà può essere impostata nella riga di comando o nella tabella [Property](property-table.md) per configurare le operazioni che l'utente o lo sviluppatore determina come non essenziali per l'installazione.

Il valore della **proprietà MSIFASTINSTALL** può essere una combinazione dei valori seguenti.



| Valore | Significato                                                                      |
|-------|------------------------------------------------------------------------------|
| 0     | Valore predefinito                                                                |
| 1     | Per questa installazione non viene salvato alcun punto di ripristino del sistema.                      |
| 2     | Eseguire solo [la determinazione dei costi dei file](file-costing.md) e ignorare il controllo degli altri costi. |
| 4     | Ridurre la frequenza dei messaggi di stato.                                   |



 

**[Windows Installer 4.5 o versioni precedenti:](not-supported-in-windows-installer-4-5.md)** Non supportato. Questa proprietà è disponibile a partire da Windows Installer 5.0.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Programma di installazione 5.0 Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Vedere i [Windows di installazione Run-Time](windows-installer-portal.md) per informazioni sul Service Pack minimo Windows richiesto da una versione Windows Installer.<br/> |



 

 





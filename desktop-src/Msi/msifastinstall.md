---
description: È possibile utilizzare la proprietà MSIFASTINSTALL per ridurre il tempo necessario per l'installazione di un pacchetto di Windows Installer di grandi dimensioni.
ms.assetid: 011668da-da04-4b80-989e-192b0daa3060
title: Proprietà MSIFASTINSTALL
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9474e295269fa4a8347210653bed5db772878662
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329122"
---
# <a name="msifastinstall-property"></a>Proprietà MSIFASTINSTALL

È possibile utilizzare la proprietà **MSIFASTINSTALL** per ridurre il tempo necessario per l'installazione di un pacchetto di Windows Installer di grandi dimensioni. La proprietà può essere impostata nella riga di comando o nella tabella delle [Proprietà](property-table.md) per configurare le operazioni che l'utente o lo sviluppatore determina non sono essenziali per l'installazione.

Il valore della proprietà **MSIFASTINSTALL** può essere una combinazione dei valori seguenti.



| Valore | Significato                                                                      |
|-------|------------------------------------------------------------------------------|
| 0     | Valore predefinito                                                                |
| 1     | Nessun punto di ripristino di sistema salvato per questa installazione.                      |
| 2     | Eseguire solo il [costo del file](file-costing.md) e ignorare il controllo di altri costi. |
| 4     | Ridurre la frequenza dei messaggi di stato.                                   |



 

**[Windows Installer 4,5 o versioni precedenti](not-supported-in-windows-installer-4-5.md):** Non supportato. Questa proprietà è disponibile a partire da Windows Installer 5,0.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Vedere i [requisiti di Run-Time Windows Installer](windows-installer-portal.md) per informazioni sul Service Pack minimo di Windows richiesto da una versione Windows Installer.<br/> |



 

 





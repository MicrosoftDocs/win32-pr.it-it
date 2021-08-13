---
description: La proprietà ROOTDRIVE specifica l'unità predefinita per la directory di destinazione dell'installazione.
ms.assetid: 9f36dc2a-2fb5-4787-a630-c7cc93ef51ec
title: ROOTDRIVE - proprietà
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 47ca4a3230dde5086b1383f3016da30d99976cf6560d0be994ecb0aaccc0ba6d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118625738"
---
# <a name="rootdrive-property"></a>ROOTDRIVE - proprietà

La **proprietà ROOTDRIVE** specifica l'unità predefinita per la directory di destinazione dell'installazione. Se la colonna Directory della tabella [Directory](directory-table.md) indica la directory di destinazione radice con un nome di proprietà non definito, il programma di installazione usa il valore della proprietà **ROOTDRIVE** per risolvere il percorso della directory di destinazione.

Se **ROOTDRIVE non** è impostato in una riga di comando o creato nella tabella [Property](property-table.md), il programma di installazione imposta questa proprietà. Durante [un'installazione amministrativa,](administrative-installation.md) il programma di installazione imposta **ROOTDRIVE** sulla prima unità di rete connessa in cui è possibile scrivere. Se non si tratta di un'installazione amministrativa o se il programma di installazione non trova unità di rete, il programma di installazione imposta **ROOTDRIVE** sull'unità locale che può essere scritta per avere più spazio libero.

Il valore di questa proprietà deve terminare con ' \\ '.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Programma di installazione 5.0 Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4.0 o Windows Installer 4.5 in Windows Server 2008 o Windows Vista. Windows Programma di installazione Windows Server 2003 o Windows XP. Vedere i [Windows di installazione Run-Time](windows-installer-portal.md) per informazioni sul Service Pack minimo Windows richiesto da una versione Windows Installer.<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà](properties.md)
</dt> </dl>

 

 





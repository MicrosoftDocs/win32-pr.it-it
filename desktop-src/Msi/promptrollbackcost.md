---
description: La proprietà PROMPTROLLBACKCOST specifica l'azione eseguita dal programma di installazione se le funzionalità di installazione di rollback sono abilitate e lo spazio su disco non è sufficiente per completare l'installazione. I valori possibili di PROMPTROLLBACKCOST sono i seguenti. ValueActionPVisualizza una finestra di dialogo che chiede se continuare senza un rollback. Eseguire il rollback di DDisable e continuare senza chiedere all'utente. FFail con la richiesta di errore di spazio su disco insufficiente.
ms.assetid: 6ffd0b3f-79b8-4ce3-a262-4d27ffc5a175
title: PROMPTROLLBACKCOST - proprietà
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 71cca3134593039354735e2e306a924620db8100eb0fd0e0a51f392c58f61897
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120129041"
---
# <a name="promptrollbackcost-property"></a>PROMPTROLLBACKCOST - proprietà

La **proprietà PROMPTROLLBACKCOST** specifica l'azione eseguita dal programma di installazione se le funzionalità di installazione di [rollback](rollback-installation.md) sono abilitate e lo spazio su disco non è sufficiente per completare l'installazione.

I valori possibili di **PROMPTROLLBACKCOST** sono i seguenti.



| Valore | Azione                                                              |
|-------|---------------------------------------------------------------------|
| P     | Visualizzare una finestra di dialogo in cui viene chiesto se continuare senza un rollback. |
| D     | Disabilitare il rollback e continuare senza chiedere all'utente.                  |
| F     | Non riesce con la richiesta di errore di spazio su disco insufficiente.                       |



 

## <a name="remarks"></a>Commenti

Quando l'interfaccia utente viene eseguita a livello Di base o nessun livello di interfaccia utente, il programma di installazione gestisce automaticamente tutta la logica di spazio su disco insufficiente.

Quando l'interfaccia utente viene eseguita a livello completo, all'utente possono essere fornite opzioni aggiuntive, ad esempio la richiesta di conferma prima di procedere con un rollback, la disabilitazione del rollback o la procedura senza rollback quando il disco è pieno. Lo sviluppatore del pacchetto deve creare la sequenza della finestra di dialogo per fornire le scelte appropriate all'utente. Gli elementi disponibili a tale scopo sono la proprietà [EnableRollback ControlEvent,](enablerollback-controlevent.md) [**OutOfDiskSpace,**](outofdiskspace.md) [**OutOfNoRbDiskSpace**](outofnorbdiskspace.md) e **la proprietà PROMPTROLLBACKCOST.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Programma di installazione 5.0 Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Programma di installazione 4.0 o Windows Installer 4.5 in Windows Server 2008 o Windows Vista. Windows Programma di installazione Windows Server 2003 o Windows XP. Vedere i [Windows di installazione Run-Time](windows-installer-portal.md) per informazioni sul Service Pack Windows minimo richiesto da una versione Windows Installer.<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà](properties.md)
</dt> </dl>

 

 





---
description: La proprietà PROMPTROLLBACKCOST specifica l'azione eseguita dal programma di installazione se le funzionalità di installazione rollback sono abilitate e lo spazio su disco è insufficiente per completare l'installazione. I valori possibili di PROMPTROLLBACKCOST sono i seguenti. ValueActionPDisplay una finestra di dialogo in cui viene chiesto se continuare senza eseguire il rollback. DDisable rollback e continua senza richiedere l'intervento dell'utente. FFail con il messaggio di errore di spazio su disco insufficiente.
ms.assetid: 6ffd0b3f-79b8-4ce3-a262-4d27ffc5a175
title: Proprietà PROMPTROLLBACKCOST
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3801ee894a66ad6e458cbad37252e289f724b9ba
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332607"
---
# <a name="promptrollbackcost-property"></a>Proprietà PROMPTROLLBACKCOST

La proprietà **PROMPTROLLBACKCOST** specifica l'azione eseguita dal programma di installazione se le funzionalità di [installazione rollback](rollback-installation.md) sono abilitate e lo spazio su disco è insufficiente per completare l'installazione.

I valori possibili di **PROMPTROLLBACKCOST** sono i seguenti.



| Valore | Azione                                                              |
|-------|---------------------------------------------------------------------|
| P     | Consente di visualizzare una finestra di dialogo in cui viene chiesto se continuare senza rollback. |
| D     | Disabilitare il rollback e continuare senza richiedere l'intervento dell'utente.                  |
| F     | Ha esito negativo con il messaggio di errore di spazio su disco insufficiente.                       |



 

## <a name="remarks"></a>Commenti

Quando l'interfaccia utente viene eseguita a livello di base o senza interfaccia utente, il programma di installazione gestisce automaticamente tutta la logica di spazio su disco.

Quando l'interfaccia utente viene eseguita a livello completo, all'utente possono essere concesse opzioni aggiuntive, ad esempio la richiesta prima di procedere con un rollback, la disabilitazione del rollback o la continuazione senza rollback quando il disco è pieno. Lo sviluppatore del pacchetto deve creare la sequenza della finestra di dialogo per fornire le scelte appropriate all'utente. Gli elementi disponibili per eseguire questa operazione sono la proprietà [EnableRollback ControlEvent](enablerollback-controlevent.md), [**OutOfDiskSpace**](outofdiskspace.md) , [**OutOfNoRbDiskSpace**](outofnorbdiskspace.md) e la proprietà **PROMPTROLLBACKCOST** .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista. Windows Installer in Windows Server 2003 o Windows XP. Vedere i [requisiti di Run-Time Windows Installer](windows-installer-portal.md) per informazioni sul Service Pack minimo di Windows richiesto da una versione Windows Installer.<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà](properties.md)
</dt> </dl>

 

 





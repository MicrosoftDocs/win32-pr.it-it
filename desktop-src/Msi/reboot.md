---
description: La proprietà restart disattiva alcune richieste di riavvio del sistema.
ms.assetid: d88752cd-f59d-4214-b5b5-ce126500aa4e
title: Riavvia proprietà
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d94b08a04f3e95d873f6fc233185ce623cafc25
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329248"
---
# <a name="reboot-property"></a>Riavvia proprietà

La proprietà restart disattiva alcune richieste **di riavvio del** sistema. Un amministratore usa in genere questa proprietà con una serie di installazioni per installare più prodotti contemporaneamente con un solo riavvio alla fine. Per ulteriori informazioni, vedere [riavvii del sistema](system-reboots.md).

Le azioni [ForceReboot](forcereboot-action.md) e [ScheduleReboot](schedulereboot-action.md) indicano al programma di installazione di richiedere all'utente di riavviare il sistema. Il programma di installazione può inoltre determinare che è necessario un riavvio se nella sequenza sono presenti azioni ForceReboot o ScheduleReboot. Ad esempio, il programma di installazione richiede automaticamente un riavvio se è necessario sostituire i file in uso durante l'installazione.

È possibile disattivare determinate richieste per i riavvii impostando la proprietà **reboot** come indicato di seguito.



| Valore di riavvio   | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Force          | Richiedere sempre un riavvio al termine dell'installazione. L'interfaccia utente chiede sempre all'utente di scegliere di riavviare alla fine. Se non è presente alcuna interfaccia utente e non si tratta di un' [installazione a più pacchetti](multiple-package-installations.md), il sistema viene riavviato automaticamente al termine dell'installazione. Se si tratta di un'installazione con più pacchetti, non viene eseguito il riavvio automatico del sistema e il programma di installazione restituisce un errore di \_ \_ riavvio \_ necessario. |
| Elimina       | Non visualizzare più la richiesta di riavvio al termine dell'installazione. Il programma di installazione richiede all'utente l'opzione per il riavvio durante l'installazione ogni volta che viene rilevata l' [azione ForceReboot](forcereboot-action.md). Se non è presente alcuna interfaccia utente, il sistema viene riavviato automaticamente a ogni ForceReboot. Il riavvio al termine dell'installazione, ad esempio causato da un tentativo di installazione di un file in uso, viene eliminato.                                    |
| ReallySuppress | Elimina tutti i riavvii e riavvia i prompt avviati da ForceReboot durante l'installazione. Non visualizzare tutti i riavvii e riavviare i prompt alla fine dell'installazione. Sia la richiesta di riavvio che il riavvio vengono eliminati. Ad esempio, il riavvio alla fine dell'installazione, causato da un tentativo di installazione di un file in uso, viene eliminato.                                                                                                                    |



 

## <a name="remarks"></a>Commenti

Il programma di installazione valuta solo il primo carattere della proprietà **reboot** .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista. Windows Installer in Windows Server 2003 o Windows XP. Vedere i [requisiti di Run-Time Windows Installer](windows-installer-portal.md) per informazioni sul Service Pack minimo di Windows richiesto da una versione Windows Installer.<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà](properties.md)
</dt> <dt>

[**Proprietà REBOOTPROMPT**](rebootprompt.md)
</dt> <dt>

[Riavvio del sistema](system-reboots.md)
</dt> </dl>

 

 





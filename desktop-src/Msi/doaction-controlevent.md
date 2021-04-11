---
description: Il ControlEvent DoAction notifica al programma di installazione di eseguire un'azione personalizzata. Questo evento può essere pubblicato tramite un controllo pulsante, un controllo CheckBox o un controllo SelectionTree. Questo evento deve essere creato nella tabella ControlEvent.
ms.assetid: 9a855330-8241-4912-84da-4fca43f1d240
title: ControlEvent DoAction
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74cc16c918522408e4cdf046e95d3d822ba3ac5c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128387"
---
# <a name="doaction-controlevent"></a>ControlEvent DoAction

Il ControlEvent DoAction notifica al programma di installazione di eseguire un'azione personalizzata. Questo evento può essere pubblicato tramite un controllo [pulsante](pushbutton-control.md) , un controllo [CheckBox](checkbox-control.md) o un controllo [SelectionTree](selectiontree-control.md) . Questo evento deve essere creato nella tabella [ControlEvent](controlevent-table.md) .

Si noti che le azioni personalizzate avviate da un ControlEvent DoAction possono inviare un messaggio con il [**metodo del messaggio**](session-message.md), ma non possono inviare un messaggio con [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage). Nei sistemi precedenti a Windows Server 2003, le azioni personalizzate avviate da un DoAction ControlEvent non possono inviare messaggi con **MsiProcessMessage** o **Metodo Message**. Per altre informazioni, vedere [invio di messaggi a Windows Installer con MsiProcessMessage](sending-messages-to-windows-installer-using-msiprocessmessage.md).

Questo ControlEvent richiede l'esecuzione dell'interfaccia utente a livello di [*interfaccia utente completo*](f-gly.md) . Questo evento non funzionerà con un'interfaccia utente [*ridotta*](r-gly.md) o un' [*interfaccia utente di base*](b-gly.md). Per ulteriori informazioni, vedere [livelli di interfaccia utente](user-interface-levels.md).

## <a name="published-by"></a>Pubblicato da

Questo ControlEvent viene pubblicato dal programma di installazione.

## <a name="argument"></a>Argomento

Stringa, il nome dell'azione personalizzata da eseguire.

## <a name="action-on-subscribers"></a>Azione sui sottoscrittori

Questo ControlEvent non esegue un'azione sui sottoscrittori.

## <a name="typical-use"></a>Utilizzo tipico

Un controllo [pulsante](pushbutton-control.md) in una finestra di dialogo è associato a questo evento nella tabella [ControlEvent](controlevent-table.md) per richiamare un'azione personalizzata.

 

 




---
description: DoAction ControlEvent notifica al programma di installazione di eseguire un'azione personalizzata. Questo evento può essere pubblicato da un controllo PushButton, un controllo CheckBox o un controllo SelectionTree. Questo evento deve essere creato nella tabella ControlEvent.
ms.assetid: 9a855330-8241-4912-84da-4fca43f1d240
title: DoAction ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: acc4133c9b9fb0b312423952ee72d1e9e38defc2713345e1a7ed106fb141f0a1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119692621"
---
# <a name="doaction-controlevent"></a>DoAction ControlEvent

DoAction ControlEvent notifica al programma di installazione di eseguire un'azione personalizzata. Questo evento può essere pubblicato da un [controllo PushButton,](pushbutton-control.md) [un controllo CheckBox](checkbox-control.md) o [un controllo SelectionTree.](selectiontree-control.md) Questo evento deve essere creato nella [tabella ControlEvent.](controlevent-table.md)

Si noti che le azioni personalizzate avviate da un ControlEvent DoAction possono inviare un messaggio con il [**metodo Message**](session-message.md), ma non possono inviare un messaggio [**con MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage). Nei sistemi precedenti a Windows Server 2003, le azioni personalizzate avviate da un Oggetto ControlEvent DoAction non possono inviare messaggi con **MsiProcessMessage** o **il metodo Message**. Per altre informazioni, vedere [Sending Messages to Windows Installer Using MsiProcessMessage](sending-messages-to-windows-installer-using-msiprocessmessage.md).

Questo ControlEvent richiede che l'interfaccia utente sia eseguita a livello [*completo dell'interfaccia*](f-gly.md) utente. Questo evento non funzionerà con un'interfaccia utente [*ridotta o*](r-gly.md) un'interfaccia utente [*di base.*](b-gly.md) Per altre informazioni, vedere [Interfaccia utente Levels.](user-interface-levels.md)

## <a name="published-by"></a>Pubblicato da

Questo ControlEvent viene pubblicato dal programma di installazione.

## <a name="argument"></a>Argomento

Stringa, il nome dell'azione personalizzata da eseguire.

## <a name="action-on-subscribers"></a>Azione nei Sottoscrittori

Questo ControlEvent non esegue un'azione sui sottoscrittori.

## <a name="typical-use"></a>Utilizzo tipico

Un [controllo PushButton](pushbutton-control.md) in una finestra di dialogo è associato a questo evento nella [tabella ControlEvent](controlevent-table.md) per richiamare un'azione personalizzata.

 

 




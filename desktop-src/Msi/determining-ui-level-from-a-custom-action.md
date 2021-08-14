---
description: Un'azione personalizzata in una tabella di sequenze dell'interfaccia utente o in un file eseguibile esterno potrebbe richiedere il livello di interfaccia utente corrente dell'installazione.
ms.assetid: d1ddadd5-b4ec-4c7c-aee4-b2d688a57eb4
title: Determinazione del livello dell'interfaccia utente da un'azione personalizzata
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af88753b5ea44927ac58b13bcb4742e7992e50e1499aa04964b60b632d68ec53
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118947568"
---
# <a name="determining-ui-level-from-a-custom-action"></a>Determinazione del livello dell'interfaccia utente da un'azione personalizzata

Un'azione personalizzata in una tabella di sequenze dell'interfaccia utente o in un file eseguibile esterno potrebbe richiedere il livello di interfaccia utente corrente dell'installazione. Ad esempio, un'azione personalizzata con una finestra di dialogo deve visualizzare la finestra di dialogo solo quando il livello dell'interfaccia utente è Interfaccia utente completa o Interfaccia utente ridotta, non deve visualizzare la finestra di dialogo se il livello dell'interfaccia utente è Interfaccia utente di base o Nessuno. È consigliabile usare la [**proprietà UILevel**](uilevel.md) per determinare il livello dell'interfaccia utente corrente. Non è possibile chiamare [**MsiSetInternalUI**](/windows/desktop/api/Msi/nf-msi-msisetinternalui) da un'azione personalizzata e non è possibile modificare la proprietà a livello di interfaccia utente dall'interno di un'azione personalizzata.

È consigliabile che le azioni personalizzate non usino il livello di interfaccia utente come condizione per l'invio di messaggi di errore al programma di installazione, perché ciò può interferire con la registrazione e i messaggi esterni.

 

 




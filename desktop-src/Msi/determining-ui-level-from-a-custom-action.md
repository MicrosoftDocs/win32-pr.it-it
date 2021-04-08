---
description: Un'azione personalizzata in una tabella di sequenza dell'interfaccia utente o un file eseguibile esterno può richiedere il livello di interfaccia utente corrente dell'installazione.
ms.assetid: d1ddadd5-b4ec-4c7c-aee4-b2d688a57eb4
title: Determinazione del livello dell'interfaccia utente da un'azione personalizzata
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2586cd03bfda2b22e721c0ae9c3393d4bbc525a6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103967812"
---
# <a name="determining-ui-level-from-a-custom-action"></a>Determinazione del livello dell'interfaccia utente da un'azione personalizzata

Un'azione personalizzata in una tabella di sequenza dell'interfaccia utente o un file eseguibile esterno può richiedere il livello di interfaccia utente corrente dell'installazione. Ad esempio, un'azione personalizzata che dispone di una finestra di dialogo dovrebbe visualizzare la finestra di dialogo solo quando il livello dell'interfaccia utente è un'interfaccia utente completa o un'interfaccia utente ridotta, non dovrebbe visualizzare la finestra di dialogo se il livello dell'interfaccia utente è interfaccia utente di base o nessuno. È necessario utilizzare la proprietà [**UILevel**](uilevel.md) per determinare il livello di interfaccia utente corrente. Non è possibile chiamare [**MsiSetInternalUI**](/windows/desktop/api/Msi/nf-msi-msisetinternalui) da un'azione personalizzata e non è possibile modificare la proprietà a livello di interfaccia utente dall'interno di un'azione personalizzata.

È consigliabile che le azioni personalizzate non utilizzino il livello di interfaccia utente come condizione per l'invio di messaggi di errore al programma di installazione, in quanto ciò può interferire con la registrazione e i messaggi esterni.

 

 




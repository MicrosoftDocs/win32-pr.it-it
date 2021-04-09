---
title: Guida alla programmazione di plug-in dell'interfaccia utente
description: Guida alla programmazione di plug-in dell'interfaccia utente
ms.assetid: 7bc0805a-306d-4b48-bc24-41077c8c7b3d
keywords:
- Windows Media Player, plug-in
- Windows Media Player, plug-in dell'interfaccia utente
- Plug-in di Windows Media Player, interfaccia utente
- plug-in, interfaccia utente
- plug-in dell'interfaccia utente, guida per programmatori
- Plug-in dell'interfaccia utente, guida per programmatori
- Guida per programmatori, plug-in dell'interfaccia utente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d417d246e92a642711e8cb02f77ff3795d47c995
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856485"
---
# <a name="user-interface-plug-ins-programming-guide"></a>Guida alla programmazione di plug-in dell'interfaccia utente

I due esempi di codice descritti in questa sezione illustrano il processo di implementazione di un plug-in dell'interfaccia utente personalizzata che inizia con il codice generato dalla procedura guidata per il plug-in di Windows Media Player.

Il plug-in dell'interfaccia utente di ricerca è un plug-in dell'area dei metadati che fornisce un pulsante di **ricerca** . Quando si fa clic su questo pulsante, nel Web browser predefinito viene avviata una pagina di ricerca che contiene informazioni sull'autore dell'elemento multimediale corrente.

Il primo passaggio per la creazione di questo plug-in consiste nell'avviare un nuovo progetto in Microsoft Visual C++ selezionando la **procedura guidata plug-in di Windows Media Player** dalla scheda **progetti** . Assegnare al progetto il nome "Search" e fare clic su **OK**. Scegliere il **plug-in dell'interfaccia utente** e fare clic su **Avanti**. Scegliere quindi il tipo di metadati dall'elenco delle opzioni e fare clic su **Avanti**. Infine, fare clic sulla casella di controllo per il supporto dell'esecuzione automatica in modo che il plug-in venga caricato automaticamente, quindi fare clic su **fine**. La procedura guidata genera i file di progetto necessari, incluse le implementazioni di base della classe CSearch e l'interfaccia **IWMPPluginUI** che supporta, e la classe CPluginWindow che fornisce l'interfaccia utente. Questo è il codice che verrà modificato per fornire la funzionalità di plug-in descritta in questa sezione.

L'ultimo argomento di questa sezione descrive come creare un plug-in di interfaccia utente in background per Windows Media Player 10 Mobile. Questo plug-in USA codice modificato generato dalla procedura guidata plug-in di Windows Media Player per creare un plug-in per Windows Media Player 10 Mobile.

In questa sezione vengono trattati gli argomenti seguenti.



| Argomento                                                                                                                                            | Descrizione                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| [Implementazione di CSearch](implementing-csearch.md)                                                                                                 | Descrive le modifiche necessarie alla classe CSearch.                                |
| [Implementazione di CPluginWindow](implementing-cpluginwindow.md)                                                                                     | Descrive le modifiche necessarie alla classe CPluginWindow.                          |
| [Creazione di un plug-in dell'interfaccia utente per Windows Media Player 10 Mobile](creating-a-user-interface-plug-in-for-windows-media-player-10-mobile.md) | Viene descritto come creare un plug-in di interfaccia utente in background per Windows Media Player 10 Mobile. |



 

 

 





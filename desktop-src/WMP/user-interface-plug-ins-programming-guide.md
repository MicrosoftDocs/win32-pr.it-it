---
title: Interfaccia utente di programmazione dei plug-in
description: Interfaccia utente di programmazione dei plug-in
ms.assetid: 7bc0805a-306d-4b48-bc24-41077c8c7b3d
keywords:
- Windows Media Player, plug-in
- Windows Media Player,plug-in dell'interfaccia utente
- Windows Media Player plug-in, interfaccia utente
- plug-in, interfaccia utente
- plug-in dell'interfaccia utente, guida per programmatori
- plug-in dell'interfaccia utente, guida alla programmazione
- guida per programmatori, plug-in dell'interfaccia utente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fcba6c3c7218e504a2e8752a4d1680e4887ec5aa7bfa69744fab00b27cbee797
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118831481"
---
# <a name="user-interface-plug-ins-programming-guide"></a>Interfaccia utente di programmazione dei plug-in

I due esempi di codice descritti in questa sezione illustrano il processo di implementazione di un plug-in dell'interfaccia utente personalizzato a partire dal codice generato dalla creazione guidata plug-in Windows Media Player.

Il plug-in dell'interfaccia utente di ricerca è un plug-in dell'area dei metadati che fornisce un **pulsante** Cerca. Quando si fa clic su questo pulsante, viene avviata una pagina di ricerca nel Web browser predefinito che contiene informazioni sull'artista dell'elemento multimediale corrente.

Il primo passaggio per la creazione di questo plug-in consiste nell'avviare un nuovo progetto in Microsoft Visual C++ selezionando Windows Media Player **creazione guidata plug-in** nella **scheda** Progetti. Assegnare al progetto il nome "Search" e fare clic su **OK.** Scegliere **Plug-in dell'interfaccia utente** e fare clic **su Avanti.** Scegliere quindi Il tipo di metadati dall'elenco di opzioni e fare clic su **Avanti.** Infine, fare clic sulla casella di controllo per il supporto dell'esecuzione automatica in modo che il plug-in verrà caricato automaticamente e quindi fare clic su **Fine**. La procedura guidata genera i file di progetto necessari, incluse le implementazioni di base della classe CSearch e **dell'interfaccia IWMPPluginUI** che supporta e la classe CPluginWindow che fornisce l'interfaccia utente. Si tratta del codice che verrà modificato per fornire la funzionalità del plug-in descritta in questa sezione.

L'ultimo argomento di questa sezione descrive come creare un plug-in dell'interfaccia utente in background per Windows Media Player 10 Mobile. Questo plug-in usa il codice modificato generato dalla Creazione guidata plug-in Windows Media Player per creare un plug-in per Windows Media Player 10 Mobile.

In questa sezione vengono trattati gli argomenti seguenti.



| Argomento                                                                                                                                            | Descrizione                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| [Implementazione di CSearch](implementing-csearch.md)                                                                                                 | Descrive le modifiche necessarie per la classe CSearch.                                |
| [Implementazione di CPluginWindow](implementing-cpluginwindow.md)                                                                                     | Descrive le modifiche necessarie per la classe CPluginWindow.                          |
| [Creazione di Interfaccia utente plug-in per Windows Media Player 10 Mobile](creating-a-user-interface-plug-in-for-windows-media-player-10-mobile.md) | Descrive come creare un plug-in dell'interfaccia utente in background per Windows Media Player 10 Mobile. |



 

 

 





---
title: Effetti grafici
description: Elenco di funzionalità che devono essere disabilitate durante l'esecuzione come sessione remota in un ambiente Servizi Desktop remoto.
ms.assetid: 229a1058-acba-4d4b-ba52-824dda4f91a5
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 711f850b8bac5d084419b1f15c2e0efe619da5b0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955513"
---
# <a name="graphic-effects"></a>Effetti grafici

Un server Servizi Desktop remoto si basa sulla rete per trasmettere tutti i dati di input e output ai terminali client. Di conseguenza, le applicazioni che utilizzano un utilizzo eccessivo degli effetti grafici possono influire sulle prestazioni di tutti i client di Servizi Desktop remoto rallentando la rete. Inoltre, la velocità di trasmissione più lenta in una rete può causare la visualizzazione di questi effetti speciali meno gradevoli rispetto a un ambiente video locale.

In particolare, le applicazioni devono disabilitare o ridurre al minimo l'uso delle funzionalità seguenti quando vengono eseguite in un ambiente di Servizi Desktop remoto come sessione remota:

-   Schermate iniziali: informazioni sul prodotto grafico o sull'azienda visualizzate durante l'avvio di un'applicazione. La trasmissione di una schermata iniziale a un client di Connessione Desktop remoto (RDC) utilizza una larghezza di banda di rete aggiuntiva e impone all'utente di attendere prima di accedere all'applicazione.
-   Animazioni, che utilizzano sia il tempo della CPU che la larghezza di banda di rete.
-   Input diretto o output sullo schermo. Se è necessario leggere i bit dalla schermata, mantenere una copia separata e fuori schermo del buffer video. Analogamente, se è necessario eseguire un output dello schermo elaborato, ad esempio sovrapponendo diverse immagini per giungere a uno schermo composito finale, eseguire tale operazione in un buffer fuori schermo, quindi inviare i risultati al buffer video effettivo.

Per ulteriori informazioni sul rilevamento di sessioni remote, vedere [rilevamento dell'ambiente Servizi Desktop remoto](detecting-the-terminal-services-environment.md).

Utilizzare la libreria Microsoft Foundation Class, o MFC, quando possibile. MFC dispone di un lungo elenco di classi tentate e vere per l'esecuzione di un'ampia gamma di attività. La maggior parte di queste classi funziona bene in un ambiente di Servizi Desktop remoto, in genere molto migliore rispetto alle soluzioni riprogettate. Un esempio valido è la classe che fornisce il testo della Guida sensibile al contesto, ovvero il testo della Guida visualizzato sullo schermo quando il puntatore del mouse viene posizionato su un pulsante o una voce di menu. Se un'applicazione utilizza l'implementazione MFC per fornire questa funzionalità, funzionerà ragionevolmente correttamente sul sistema desktop. Tuttavia, se l'applicazione implementa questa funzionalità utilizzando le finestre di dialogo o un approccio alternativo, il risultato finale potrebbe non funzionare correttamente in un ambiente Servizi Desktop remoto.

 

 





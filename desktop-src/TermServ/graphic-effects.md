---
title: Effetti grafici
description: Elenco di funzionalità che devono essere disabilitate durante l'esecuzione come sessione remota in un Servizi Desktop remoto locale.
ms.assetid: 229a1058-acba-4d4b-ba52-824dda4f91a5
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2cad01bb7b61c471ba81f382d1fc4031b8c44dcef63a78c5a0cc17641b5e457e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119059439"
---
# <a name="graphic-effects"></a>Effetti grafici

Un Servizi Desktop remoto server si basa sulla rete per trasmettere tutti gli input e l'output ai terminali client. Di conseguenza, le applicazioni che usano in modo eccessivo gli effetti grafici possono influire sulle prestazioni di Servizi Desktop remoto client rallentando la rete. Inoltre, la velocità di trasmissione più lenta su una rete potrebbe causare questi effetti speciali meno gradevoli rispetto a quelli di un ambiente video locale.

In particolare, le applicazioni devono disabilitare o ridurre al minimo l'uso delle funzionalità seguenti quando vengono eseguite in un ambiente Servizi Desktop remoto come sessione remota:

-   Schermate iniziali: informazioni grafiche sul prodotto o sull'azienda visualizzate durante l'avvio di un'applicazione. La trasmissione di una schermata iniziale a un client rdc (Connessione Desktop remoto) utilizza una larghezza di banda di rete aggiuntiva e forza l'utente ad attendere prima di accedere all'applicazione.
-   Animazioni, che utilizzano sia il tempo cpu che la larghezza di banda di rete.
-   Indirizzare l'input o l'output alla schermata. Se è necessario leggere i bit dallo schermo, mantenere una copia separata fuori schermo del buffer video. Analogamente, se è necessario eseguire un output dello schermo elaborato, ad esempio sovrapporre diverse immagini per arrivare a uno schermo composito finale, eseguire questa operazione in un buffer fuori schermo e quindi inviare i risultati al buffer video effettivo.

Per altre informazioni sul rilevamento di sessioni remote, vedere [Detecting the Servizi Desktop remoto Environment](detecting-the-terminal-services-environment.md).

Usare la libreria Microsoft Foundation Class, o MFC, quando possibile. MFC include un lungo elenco di classi tentate e vere per l'esecuzione di un'ampia gamma di attività. La maggior parte di queste classi funziona bene in un ambiente Servizi Desktop remoto, in genere molto meglio delle soluzioni ri-progettate. Un buon esempio è la classe che fornisce testo della Guida sensibile al contesto, ovvero il testo della Guida visualizzato sullo schermo quando il puntatore del mouse viene posizionato su un pulsante o una voce di menu. Se un'applicazione usa l'implementazione MFC per fornire questa funzionalità, funzionerà ragionevolmente bene nel sistema desktop. Tuttavia, se l'applicazione implementa questa funzionalità usando finestre di dialogo o un approccio alternativo, il risultato finale potrebbe non funzionare anche in un Servizi Desktop remoto ambiente.

 

 





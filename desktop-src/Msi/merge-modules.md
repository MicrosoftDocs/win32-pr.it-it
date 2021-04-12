---
description: I moduli merge forniscono un metodo standard mediante il quale gli sviluppatori distribuiscono i componenti Windows Installer condivisi e la logica di configurazione alle applicazioni.
ms.assetid: 673de3ff-e58c-4153-9c8d-c3baebba5eb1
title: Unisci moduli
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3499368b309909bcb06da45476d43d8cac28e205
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233848"
---
# <a name="merge-modules"></a>Unisci moduli

I moduli merge forniscono un metodo standard mediante il quale gli sviluppatori distribuiscono i [*componenti*](c-gly.md) Windows Installer condivisi e la logica di configurazione alle applicazioni. I moduli merge vengono utilizzati per fornire codice condiviso, file, risorse, voci del registro di sistema e la logica di installazione alle applicazioni come un unico file composto. Gli sviluppatori che creano nuovi modelli merge o utilizzano i moduli merge esistenti devono seguire lo standard descritto in questa sezione.

Un modulo merge è simile alla struttura di un file Windows Installer [*. msi*](m-gly.md)semplificato. Un modulo merge, tuttavia, non può essere installato da solo, ma deve essere unito in un pacchetto di installazione utilizzando uno strumento di merge. Gli sviluppatori che desiderano utilizzare i moduli unione devono ottenere uno degli strumenti di merge distribuiti liberamente, ad esempio Mergemod.dll, oppure acquistare uno strumento di merge da un fornitore di software indipendente. Gli sviluppatori possono creare nuovi moduli unione usando molti degli stessi strumenti software usati per creare un pacchetto di installazione di Windows Installer, ad esempio l'editor di tabelle di database Orca fornito con Windows Installer SDK.

Quando un modulo merge viene unito nel file con estensione msi di un'applicazione, tutte le informazioni e le risorse necessarie per installare i componenti forniti dal modulo merge vengono incorporate nel file con estensione msi dell'applicazione. Il modulo merge non è più necessario per installare questi componenti e non è necessario che il modulo merge sia accessibile a un utente. Poiché tutte le informazioni necessarie per installare i componenti vengono recapitate come un singolo file, l'utilizzo di modelli Unione può eliminare molte istanze di conflitti di versione, voci del registro di sistema mancanti e file installati in modo errato.

Per ulteriori informazioni sui moduli merge, vedere:

-   [Informazioni sui moduli merge](about-merge-modules.md)
-   [Uso di moduli merge](using-merge-modules.md)
-   [Riferimento al modulo merge](merge-module-reference.md)

 

 




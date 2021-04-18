---
description: Il Windows Installer riduce il costo totale di proprietà (TCO) delle applicazioni, aumentando la capacità dei clienti di gestire e gestire i componenti dell'applicazione durante la fase di installazione e di esecuzione.
ms.assetid: fbb139e3-c81b-44fc-9e92-bada0be02862
title: Gestione dei componenti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aeff6c25556879429330170ec8190b1296576517
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314302"
---
# <a name="component-management"></a>Gestione dei componenti

Il Windows Installer riduce il costo totale di proprietà (TCO) delle applicazioni, aumentando la capacità dei clienti di gestire e gestire i componenti dell'applicazione durante la fase di installazione e di esecuzione. Il database di installazione tiene traccia delle applicazioni che richiedono un particolare componente, ovvero i file che comprendono ogni componente, in cui ogni file è installato nel sistema e in cui si trovano le origini dei componenti. Ciò consente agli sviluppatori di creare pacchetti che offrono i vantaggi seguenti:

-   Maggiore resilienza delle applicazioni. Utilizzare il programma di installazione per rilevare e reinstallare i componenti danneggiati senza dover eseguire di nuovo l'installazione. Il programma di installazione controlla il percorso di un componente in fase di esecuzione. Questo consente di liberare le applicazioni dalla dipendenza da percorsi di file statici che generalmente differiscono tra i computer e possono puntare a componenti mancanti. Per altre informazioni, vedere [resilienza](resiliency.md).
-   Installazione su richiesta. Questo set di funzionalità non viene installato durante l'installazione, ma viene specificato nel database per l'installazione JIT (just-in-Time) per l'utilizzo, se richiesto dall'applicazione in futuro. Gli utenti non devono eseguire di nuovo l'installazione. Per altre informazioni, vedere [installazione su richiesta](installation-on-demand.md).
-   Annuncio di collegamenti a funzionalità, applicazioni o interi prodotti nell'interfaccia utente. Gli utenti possono installarli su richiesta usando i tasti di scelta rapida. Gli utenti possono anche rimuovere le funzionalità, le applicazioni o tutti i prodotti su richiesta. Per ulteriori informazioni, vedere l' [annuncio](advertisement.md).
-   Personalizzazione dell'installazione. Un amministratore può applicare le trasformazioni al database che adattano l'installazione per un determinato gruppo di utenti. Per altre informazioni, vedere [Personalizzazione](customization.md).
-   Distribuzione più semplice degli aggiornamenti delle applicazioni. Utilizzare il programma di installazione per aggiornare i prodotti. Per ulteriori informazioni, vedere applicazione di [patch e aggiornamenti](patching-and-upgrades.md).
-   Visualizzazione del collegamento alla funzionalità. Il programma di installazione Visualizza i collegamenti alle funzionalità eseguite localmente con i collegamenti alle funzionalità eseguite in modalità remota. Poiché il database di installazione specifica il contesto di esecuzione di ogni funzionalità, i punti di ingresso visibili in modo visibile possono essere presentati agli utenti in base alle esigenze.
-   Mantieni le metriche di utilizzo per le funzionalità. Gli sviluppatori possono fornire un pacchetto di installazione che mantiene il conteggio dell'utilizzo di una funzionalità da parte di tutte le applicazioni client e rimuove i componenti che non vengono utilizzati.
-   Incorporare le installazioni. Gli sviluppatori possono incorporare le funzionalità di gestione dei componenti del programma di installazione nelle proprie applicazioni mediante la creazione di un pacchetto di installazione e l'utilizzo delle [funzioni del programma di installazione](installer-functions.md) nel codice dell'applicazione. Nella figura seguente viene illustrata un'applicazione che richiede l'installazione di una funzionalità.

    ![installazione della funzionalità richiesta dall'applicazione. ](images/over1.png)

 

 




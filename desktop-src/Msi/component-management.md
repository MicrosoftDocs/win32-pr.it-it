---
description: Il Windows installer riduce il costo totale di proprietà (TCO) delle applicazioni aumentando la capacità dei clienti di gestire e gestire i componenti dell'applicazione durante l'installazione e la fase di esecuzione.
ms.assetid: fbb139e3-c81b-44fc-9e92-bada0be02862
title: Gestione dei componenti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a818e6ceab0ed793ded2bdd0034d9fe8355d16fbbea1d5c78d521f4682b7c373
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118144816"
---
# <a name="component-management"></a>Gestione dei componenti

Il Windows installer riduce il costo totale di proprietà (TCO) delle applicazioni aumentando la capacità dei clienti di gestire e gestire i componenti dell'applicazione durante l'installazione e la fase di esecuzione. Il database di installazione tiene traccia delle applicazioni che richiedono un particolare componente, quali file costituiscono ogni componente, in cui ogni file è installato nel sistema e dove si trovano le origini dei componenti. Ciò consente agli sviluppatori di creare pacchetti che offrono i vantaggi seguenti:

-   Maggiore resilienza delle applicazioni. Usare il programma di installazione per rilevare e reinstallare i componenti danneggiati senza dover eseguire nuovamente il programma di installazione. Il programma di installazione controlla il percorso di un componente in fase di esecuzione. In questo modo le applicazioni non possono dipendere da percorsi di file statici che in genere differiscono tra i computer e possono puntare a componenti mancanti. Per altre informazioni, vedere [Resilienza.](resiliency.md)
-   Installazione su richiesta. Questo set di funzionalità non viene installato durante l'installazione, ma viene specificato nel database da installare just-in-time per l'uso, se richiesto dall'applicazione in futuro. Gli utenti non devono eseguire nuovamente l'installazione. Per altre informazioni, vedere [Installation-On-Demand](installation-on-demand.md).
-   Annuncio di collegamenti a funzionalità, applicazioni o interi prodotti nell'interfaccia utente. Gli utenti possono installarlo su richiesta usando i collegamenti. Gli utenti possono anche rimuovere funzionalità, applicazioni o interi prodotti su richiesta. Per altre informazioni, vedere [Advertisement](advertisement.md).
-   Personalizzazione dell'installazione. Un amministratore può applicare trasformazioni al database che adattano l'installazione per un determinato gruppo di utenti. Per altre informazioni, vedere [Personalizzazione](customization.md).
-   Distribuzione più semplice degli aggiornamenti delle applicazioni. Usare il programma di installazione per aggiornare i prodotti. Per altre informazioni, vedere [Applicazione di patch e aggiornamenti.](patching-and-upgrades.md)
-   Visualizzazione dei tasti di scelta rapida delle funzionalità. Il programma di installazione visualizza i collegamenti alle funzionalità eseguite in locale con collegamenti alle funzionalità eseguite in modalità remota. Poiché il database di installazione specifica il contesto di esecuzione di ogni funzionalità, è possibile presentare agli utenti punti di ingresso visibilmente equivalenti in base alle esigenze.
-   Mantenere le metriche di utilizzo per le funzionalità. Gli sviluppatori possono fornire un pacchetto di installazione che mantiene il numero di utilizzo di una funzionalità da tutte le applicazioni client e rimuove i componenti che non vengono usati.
-   Incorporare le installazioni. Gli sviluppatori possono incorporare le funzionalità di gestione dei componenti del programma di installazione nelle applicazioni mediante la creazione di un pacchetto di installazione e l'uso delle funzioni del programma di installazione [nel](installer-functions.md) codice dell'applicazione. La figura seguente illustra un'applicazione che richiede l'installazione di una funzionalità.

    ![applicazione che richiede l'installazione della funzionalità. ](images/over1.png)

 

 




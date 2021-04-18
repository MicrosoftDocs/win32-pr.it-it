---
description: "Qualsiasi operazione di backup che tenti di copiare un'immagine completa e stabile di un sistema deve affrontare i problemi seguenti:"
ms.assetid: 8ccdba6d-1097-4c1c-982c-f3d9cbdf06cd
title: Problemi comuni di backup del volume
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f10433e0a695c11f7e61a258c3256baa651dc27
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318905"
---
# <a name="common-volume-backup-issues"></a>Problemi comuni di backup del volume

Qualsiasi operazione di backup che tenti di copiare un'immagine completa e stabile di un sistema deve affrontare i problemi seguenti:

-   File inaccessibili durante un backup. Per le applicazioni in esecuzione è spesso necessario che i file vengano aperti in modalità esclusiva durante un backup, impedendo la copia dei programmi di backup.
-   Stato del file incoerente. Anche se i file di un'applicazione non sono aperti in modalità esclusiva, è possibile che, a causa del tempo limitato necessario per l'apertura, il backup e la chiusura di un file, che i file copiati nei supporti di archiviazione non riflettano tutti lo stesso stato dell'applicazione.
-   Necessità di ridurre al minimo le interruzioni del servizio. Per garantire che l'accessibilità dei file e l'integrità dei dati di cui viene eseguito il backup possano richiedere la sospensione e/o la chiusura di tutti i programmi in esecuzione durante un backup del volume. Per i sistemi con dischi di grandi dimensioni, la durata può essere di ore.

    Alcuni fornitori di archiviazione hanno tentato di risolvere questi problemi offrendo un meccanismo di acquisizione del volume, ovvero un mezzo per acquisire un'immagine dei file su disco in un determinato istante di tempo, usando un meccanismo copy-on-Write o "split mirror". Tuttavia, queste soluzioni comportano difficoltà proprie:

    -   Implementazioni del fornitore incompatibili dell'acquisizione del volume. Molti provider di dispositivi RAID forniscono meccanismi di acquisizione del volume. Ogni fornitore dispone tuttavia di una propria interfaccia e ognuno deve ottenere supporto dai fornitori di backup per le interfacce di acquisizione del volume. Ciò significa che i fornitori di applicazioni di backup devono supportare più implementazioni di acquisizione di volumi, che non sono desiderabili.
    -   Mancanza di coordinamento dell'applicazione. Molti dispositivi che supportano un'acquisizione di volume non supportano il coordinamento delle applicazioni in esecuzione con il blocco dei dati su disco. Per i dispositivi che eseguono, come per le applicazioni di backup, ogni fornitore ha un'interfaccia diversa.
    -   Supporto limitato per i dispositivi non RAID. Pochi se i fornitori di dischi convenzionali forniscono il supporto per qualsiasi tipo di acquisizione dei volumi nei driver di dispositivo. Ciò significa che i meccanismi di acquisizione sono limitati a determinati sistemi disco e in genere non supportano il backup delle aree di sistema.
    -   È necessario gestire gli aggiornamenti al disco durante l'acquisizione del volume. Sebbene i meccanismi di acquisizione del volume forniti dal fornitore di archiviazione possano bloccare lo stato dei dati su disco, non sempre interagiscono con le applicazioni in esecuzione. Questo significa spesso che i dati inviati al volume mentre è in corso l'acquisizione del volume in un dispositivo di archiviazione potrebbero andare persi.
    -   Backup multivolume coerente. Il dispositivo di archiviazione esegue queste acquisizioni di volumi, pertanto non è in genere disponibile alcun meccanismo per il coordinamento del tempo di blocco dei dati. Ciò è particolarmente vero se i dispositivi provengono da fornitori distinti. Se pertanto sono presenti più volumi di archiviazione in un backup con acquisizione volume, è possibile che l'immagine temporale mantenuta per ogni volume non sia coerente.

 

 




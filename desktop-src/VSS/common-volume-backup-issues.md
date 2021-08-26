---
description: "Qualsiasi operazione di backup che tenta di copiare un'immagine completa e stabile di un sistema deve gestire i problemi seguenti:"
ms.assetid: 8ccdba6d-1097-4c1c-982c-f3d9cbdf06cd
title: Problemi comuni di backup dei volumi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16275c0d8e9128110736dd5feb51c75d2977b77c746b56cda487eed3aec86c34
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120032891"
---
# <a name="common-volume-backup-issues"></a>Problemi comuni di backup dei volumi

Qualsiasi operazione di backup che tenta di copiare un'immagine completa e stabile di un sistema deve gestire i problemi seguenti:

-   File inaccessibili durante un backup. Le applicazioni in esecuzione spesso devono mantenere i file aperti in modalità esclusiva durante un backup, impedendo ai programmi di backup di copiarli.
-   Stato del file incoerente. Anche se i file di un'applicazione non sono aperti in modalità esclusiva, è possibile, a causa del tempo finito necessario per aprire, eseguire il backup e chiudere un file, che i file copiati nei supporti di archiviazione non riflettano tutti lo stesso stato dell'applicazione.
-   È necessario ridurre al minimo le interruzioni del servizio. Per garantire l'accessibilità dei file e l'integrità dei dati sottoposti a backup, può essere necessaria la sospensione e/o la chiusura di tutti i programmi in esecuzione durante un backup del volume. Per i sistemi con dischi di grandi dimensioni, la durata potrebbe essere di ore.

    Di recente, alcuni fornitori di risorse di archiviazione hanno tentato di risolvere questi problemi fornendo un meccanismo di acquisizione del volume, ovvero un mezzo per acquisire un'immagine dei file su disco in un determinato momento, usando un meccanismo di copia su scrittura o "split mirror". Tuttavia, queste soluzioni comportano difficoltà proprie:

    -   Implementazioni del fornitore incompatibili di Volume Capture. Molti provider di dispositivi RAID forniscono meccanismi di acquisizione del volume. Tuttavia, ogni fornitore ha una propria interfaccia e deve ottenere supporto dai fornitori di backup per le interfacce di acquisizione dei volumi. Ciò significa che i fornitori di applicazioni di backup devono supportare più implementazioni di Volume Capture, il che è indesiderato.
    -   Mancanza di coordinamento delle applicazioni. Molti dispositivi che supportano l'acquisizione di volumi non supportano il coordinamento delle applicazioni in esecuzione con il blocco dei dati su disco. Per i dispositivi che fanno, come con le applicazioni di backup, ogni fornitore ha un'interfaccia diversa.
    -   Supporto limitato per i dispositivi non RAID. Pochi fornitori di dischi convenzionali forniscono supporto per qualsiasi tipo di acquisizione di volumi nei driver di dispositivo. Ciò significa che i meccanismi di acquisizione sono limitati a determinati sistemi disco e in genere non supportano il backup delle aree di sistema.
    -   È necessario gestire gli aggiornamenti del disco durante l'acquisizione del volume. Anche se i meccanismi di acquisizione dei volumi forniti dal fornitore dell'archiviazione possono bloccare lo stato dei dati su disco, non sempre interagiscono con le applicazioni in esecuzione. Ciò significa spesso che i dati inviati al volume mentre un dispositivo di archiviazione è in fase di acquisizione del volume potrebbero andare persi.
    -   Backup multivolume coerente. Il dispositivo di archiviazione esegue queste acquisizioni di volume, quindi in genere non esiste alcun meccanismo per coordinare l'intervallo di blocco dei dati. Questo vale in particolare se i dispositivi provengono da fornitori separati. Pertanto, se più volumi di archiviazione sono coinvolti in un backup con un'acquisizione di volume, l'immagine dell'ora mantenuta per ogni volume potrebbe non essere coerente.

 

 




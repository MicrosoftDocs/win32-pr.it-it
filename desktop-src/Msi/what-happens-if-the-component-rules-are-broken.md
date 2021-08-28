---
description: In alcuni casi, gli autori possono decidere di dover interrompere le regole per la creazione di componenti, come descritto in Organizzazione delle applicazioni in componenti e Modifica del codice del componente.
ms.assetid: 487b6a00-77eb-4c51-8e32-46bcd4493df8
title: Cosa accade se le regole del componente vengono interrotte?
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e3f830fa402da44be992d74adc957d88a19442dcbb51173a87e79fa2266552a1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119498767"
---
# <a name="what-happens-if-the-component-rules-are-broken"></a>Cosa accade se le regole del componente vengono interrotte?

In alcuni casi, gli autori possono decidere di dover interrompere le regole per la creazione di componenti, come descritto [in](organizing-applications-into-components.md) Organizzazione di applicazioni in componenti e Modifica del codice [del componente](changing-the-component-code.md). Gli autori devono essere consapevoli delle possibili conseguenze di questa operazione e devono in caso contrario garantire che i componenti non siano mai installati dove possono danneggiare altre applicazioni o componenti nel sistema dell'utente.

L'elenco seguente descrive i modi in cui gli autori talvolta infrandono le regole dei componenti consigliati e le possibili conseguenze.

Un autore aggiunge risorse a un componente senza modificare il codice del componente.

-   I prodotti installati con il componente precedente non hanno informazioni sulle risorse aggiunte nel database di installazione.
-   Se nello stesso computer sono installati sia un nuovo prodotto con le risorse aggiunte che un prodotto precedente, le risorse possono essere abbandonate se il nuovo prodotto viene disinstallato per primo.
-   Un prodotto precedente senza le risorse aggiunte non può ripristinare la versione più recente del componente. La reinstallazione del prodotto precedente non ripristina le risorse aggiunte.

Un autore rimuove le risorse da un componente senza modificare il codice del componente.

-   I prodotti installati con il nuovo componente non hanno informazioni sulle risorse rimosse nel database di installazione.
-   Se nello stesso computer sono installati sia un prodotto precedente, con le informazioni sulle risorse, sia un nuovo prodotto, le risorse possono essere abbandonate se il prodotto precedente viene disinstallato per primo.
-   Un nuovo prodotto con le risorse rimosse non può ripristinare la versione precedente del prodotto. La reinstallazione del nuovo prodotto non ripristina le risorse rimosse.

Un autore include un file incompatibile con le versioni precedenti senza modificare il codice del componente.

Se un file incompatibile viene incluso in un componente senza modificare il codice del componente, il controllo delle versioni dei [file](default-file-versioning.md) predefinito fa sì che il programma di installazione sovrascriva il file originale con il file incompatibile più recente. Ciò può danneggiare i prodotti vecchi che necessitano del file originale. Può anche impedire al programma di installazione di ripristinare il prodotto precedente perché la versione del file del percorso della chiave di un componente determina la versione del componente. Se è già installata una versione più recente del file del percorso della chiave, il programma di installazione non installa una versione precedente del componente. Per altre informazioni, vedere [Regole di controllo delle versioni dei file.](file-versioning-rules.md) In questo caso, il nuovo prodotto deve essere rimosso prima di poter reinstallare il prodotto precedente.

-   [Il controllo delle versioni dei file](default-file-versioning.md) predefinito fa sì che il programma di installazione sovrascriva il file originale con il file incompatibile più recente.
-   I prodotti vecchi che necessitano del file originale sono danneggiati.
-   Può anche impedire al programma di installazione di ripristinare il prodotto precedente perché la versione del file del percorso della chiave di un componente determina la versione del componente. Se è già installata una versione più recente del file del percorso della chiave, il programma di installazione non installa la versione precedente del componente. Per altre informazioni, vedere [Regole di controllo delle versioni dei file.](file-versioning-rules.md) In questo caso, il nuovo prodotto deve essere rimosso prima di poter reinstallare il prodotto precedente.

Un autore include la stessa risorsa in due componenti diversi.

Se due componenti hanno una risorsa con lo stesso nome e lo stesso percorso ed entrambi i componenti vengono installati nella stessa cartella, la rimozione di uno dei due componenti rimuove la risorsa comune, danneggiando il componente rimanente.

-   La disinstallazione di uno dei due componenti rimuove la risorsa e interrompe l'altro componente.
-   Il meccanismo di conteggio dei riferimenti ai componenti è danneggiato.

 

 




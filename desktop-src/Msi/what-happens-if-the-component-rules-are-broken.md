---
description: In alcuni casi, gli autori possono decidere di suddividere le regole per la creazione di componenti come descritto in organizzazione di applicazioni in componenti e modifica del codice componente.
ms.assetid: 487b6a00-77eb-4c51-8e32-46bcd4493df8
title: Cosa accade se le regole dei componenti sono interrotte?
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78f61a0a819856c5014aa70acfaeb46be5043e58
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314194"
---
# <a name="what-happens-if-the-component-rules-are-broken"></a>Cosa accade se le regole dei componenti sono interrotte?

In alcuni casi, gli autori possono decidere di suddividere le regole per la creazione di componenti come descritto in [organizzazione di applicazioni in componenti](organizing-applications-into-components.md) e [modifica del codice componente](changing-the-component-code.md). È necessario che gli autori siano consapevoli delle possibili conseguenze di questa operazione e che, in caso contrario, garantiscano che i loro componenti non vengano mai installati dove possono danneggiare altre applicazioni o componenti nel sistema dell'utente.

Nell'elenco seguente vengono descritte le modalità con cui gli autori interrompono talvolta le regole dei componenti consigliate e le possibili conseguenze.

Un autore aggiunge risorse a un componente senza modificare il codice componente.

-   I prodotti installati con il componente precedente non contengono informazioni sulle risorse aggiunte nel database di installazione.
-   Se un nuovo prodotto con le risorse aggiunte e un prodotto precedente sono installati nello stesso computer, è possibile che le risorse rimangano invariate se il nuovo prodotto viene disinstallato per primo.
-   Un prodotto precedente senza le risorse aggiunte non è in grado di ripristinare la versione più recente del componente. Se si reinstalla il prodotto precedente, le risorse aggiunte non vengono ripristinate.

Un autore rimuove le risorse da un componente senza modificare il codice componente.

-   I prodotti installati con il nuovo componente non contengono informazioni sulle risorse rimosse nel database di installazione.
-   Se un prodotto precedente, con le informazioni sulle risorse e un nuovo prodotto sono installati nello stesso computer, è possibile che le risorse rimangano invariate se il prodotto precedente viene disinstallato per primo.
-   Un nuovo prodotto con le risorse rimosse non è in grado di ripristinare la versione precedente del prodotto. La reinstallazione del nuovo prodotto non comporta il ripristino delle risorse rimosse.

Un autore include un file incompatibile con le versioni precedenti senza modificare il codice componente.

Se un file non compatibile è incluso in un componente senza modificare il codice del componente, il [controllo delle versioni dei file predefinito](default-file-versioning.md) fa in modo che il programma di installazione sovrascriva il file originale con il file non compatibile più recente. Questo può danneggiare i prodotti obsoleti che necessitano del file originale. Potrebbe anche impedire al programma di installazione di ripristinare il vecchio prodotto perché la versione del file di percorso della chiave di un componente determina la versione del componente. Se è già installata una versione più recente del file del percorso della chiave, il programma di installazione non installa una versione precedente del componente. Per altre informazioni, vedere [regole di controllo delle versioni dei file](file-versioning-rules.md). In questo caso, è necessario rimuovere il nuovo prodotto prima di poter reinstallare il vecchio prodotto.

-   Il [controllo delle versioni dei file predefinito](default-file-versioning.md) consente al programma di installazione di sovrascrivere il file originale con il file non compatibile più recente.
-   I prodotti obsoleti che necessitano del file originale sono danneggiati.
-   Potrebbe anche impedire al programma di installazione di ripristinare il vecchio prodotto perché la versione del file di percorso della chiave di un componente determina la versione del componente. Se è già installata una versione più recente del file del percorso della chiave, il programma di installazione non installa la versione precedente del componente. Per altre informazioni, vedere [regole di controllo delle versioni dei file](file-versioning-rules.md). In questo caso, è necessario rimuovere il nuovo prodotto prima di poter reinstallare il vecchio prodotto.

Un autore include la stessa risorsa in due componenti diversi.

Se due componenti hanno una risorsa con lo stesso nome e la stessa posizione ed entrambi i componenti sono installati nella stessa cartella, la rimozione di uno dei componenti rimuove la risorsa comune, che danneggia il componente rimanente.

-   La disinstallazione di entrambi i componenti comporta la rimozione della risorsa e l'interruzione dell'altro componente.
-   Il meccanismo di conteggio dei riferimenti del componente è danneggiato.

 

 




---
title: Uso dei profili di dispositivo con WCS
description: I profili di dispositivo sono uno strumento di base per la gestione dei colori.
ms.assetid: 9ea420ad-dcf1-4ba9-b739-308be7a56a6c
keywords:
- Windows Color System (WCS), profili di dispositivo
- WCS (sistema di colori Windows), profili di dispositivo
- Gestione colori immagine, profili dispositivo
- gestione dei colori, profili di dispositivo
- colori, profili di dispositivo
- Windows Color System (WCS), profili
- WCS (Windows Color System), profili
- Gestione colori immagine, profili
- gestione dei colori, profili
- colori, profili
- profili di dispositivo
- Conversione colori
- profili di collegamento del dispositivo
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2cf58b46cbee67d437e7d6fe343c7f3a0fab451b
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "106321005"
---
# <a name="using-device-profiles-with-wcs"></a>Uso dei profili di dispositivo con WCS

I profili di dispositivo sono uno strumento di base per la gestione dei colori. Un [profilo di dispositivo](d.md) è un file che contiene informazioni su come convertire i colori nello spazio di colore e la [gamma](./g.md) di colori di un dispositivo specifico in uno spazio di colore indipendente dal dispositivo. Lo spazio di colore indipendente dal dispositivo usato da ICM2 viene definito spazio di connessione del profilo (PC). Un profilo di dispositivo contiene anche informazioni su come convertire i colori dai PC nello spazio dei colori e nel gamut dei colori di un dispositivo specifico.

Questi due set di informazioni di conversione vengono usati per la [conversione dei colori](c.md) e la gestione dei colori. Ad esempio, è possibile creare un'immagine nello spazio colore e nella gamma di colori di una visualizzazione video. Le informazioni nei file del profilo del dispositivo possono essere utilizzate per visualizzare una rappresentazione di un'immagine stampata. Spesso gli utenti desiderano visualizzare sullo schermo il modo in cui i colori cambiano quando viene stampata un'immagine. Questa operazione è detta correzione. Un'immagine può essere provata convertendo i colori dal gamut dei colori di origine (lo schermo) ai colori dei [PC](p.md) e quindi convertendo i computer nel gamut dei colori di destinazione (la stampante). L'immagine risultante può essere visualizzata sullo schermo, in modo da consentire all'utente di visualizzare l'immagine finale quando viene stampata.

I profili di dispositivo consentono anche usi più complessi. Ad esempio, possono essere usati per avere un'idea dell'aspetto di un'immagine creata in uno schermo video quando viene stampato in una stampante laser ad alta risoluzione. L'esempio è più complesso se è presente solo una stampante inkjet standard in cui riprovare. ICM2 convertirà l'immagine dalla [gamma](./g.md) dello schermo alla gamma della stampante inkjet. Da qui viene convertito nella gamma della stampante laser. L'immagine risultante può essere stampata sulla stampante a getto d'inchiostro. Naturalmente, l'immagine potrebbe essere a una risoluzione superiore quando viene stampata sulla stampante laser con colori. Tuttavia, i colori dell'immagine di correzione stampata sulla stampante inkjet sarebbero una corrispondenza vicina ai colori che la stampante laser avrebbe stampato.

Le conversioni da un profilo di dispositivo possono essere concatenate in un singolo file, denominato *profilo di collegamento del dispositivo*. Se una serie di conversioni viene usata ripetutamente, la creazione di un profilo di collegamento del dispositivo consente di ridurre il tempo di conversione.

È possibile gestire i profili dei dispositivi stessi. Gestione del profilo è il processo di associazione dei profili colori alle istanze del dispositivo. A qualsiasi dispositivo di output a colori può essere associato un set di uno o più profili colori. I produttori di hardware e le terze parti che forniscono profili colori devono eseguire la gestione dei profili.

È possibile condividere i set di profili tra i dispositivi oppure dedicarli a dispositivi specifici. Si supponga, ad esempio, di disporre di due stampanti a colori dello stesso modello. Ogni stampante richiederebbe l'associazione di un set di profili colori. Il set di profili colori per una stampante corrisponde alle diverse configurazioni possibili in tale modello. Essendo dello stesso modello, entrambe le stampanti possono condividere un set di profili. In alternativa, è possibile assegnare a ogni stampante un proprio set di profili distinti. In quest'ultimo caso, i profili colori nel set possono essere calibrati con precisione per il singolo output della stampante, non solo per le caratteristiche generali di output del modello.

Sono disponibili tre classi diverse di profili ICC: profili di input, profili di visualizzazione e profili di output. I profili di input sono in genere associati a un dispositivo, ad esempio uno scanner. I profili di visualizzazione sono in genere associati a un monitor del computer. I profili di output sono comunemente associati alle stampanti.

La specifica consente anche profili di dispositivo, profili astratti, profili di collegamento a dispositivi, profili colori denominati e profili dello spazio dei colori.

Un profilo di dispositivo descrive lo spazio dei colori di un dispositivo specifico.

Un profilo astratto fornisce un metodo generico per consentire agli utenti di apportare modifiche dei colori soggettive a immagini o oggetti grafici tramite la trasformazione dei dati di colore nei PC.

Come indicato in precedenza, un profilo di collegamento del dispositivo Concatena una serie di profili in un'unica trasformazione.

I profili colori denominati possono essere considerati come profili di pari livello ai profili di dispositivo. Per un determinato dispositivo sono disponibili uno o più profili di dispositivo per gestire le conversioni dei colori del processo e uno o più profili colori denominati per gestire i colori denominati. Potrebbero essere presenti più profili colori denominati per tenere conto di diversi materiali di consumo o più fornitori di colori denominati.

Un profilo dello spazio dei colori descrive uno spazio di colore indipendente dal dispositivo.

Nella tabella seguente sono riepilogati i vari tipi di profili.



| Tipo di profilo        | Descrizione                                                                                                                   |
|---------------------|-------------------------------------------------------------------------------------------------------------------------------|
| Profilo astratto    | Profilo che è stato regolato in base alle preferenze specifiche di un utente.                                                     |
| Profilo dello spazio colore | Profilo che descrive uno spazio di colore indipendente dal dispositivo.                                                                    |
| Profilo collegamento dispositivo | Serie di profili concatenati in un unico profilo.                                                    |
| Profilo del dispositivo      | Profilo che descrive lo spazio dei colori di un dispositivo specifico.                                                              |
| Profilo di visualizzazione     | Classe o categoria di profili che include qualsiasi tipo di profilo associato a una visualizzazione.                                  |
| Profilo di input       | Classe o categoria di profili che include qualsiasi tipo di profilo associato a un dispositivo di input, ad esempio uno scanner.          |
| Profilo colori denominato | Profilo per uno spazio colore costituito da colori denominati.                                                                    |
| Profili di output     | Classe o categoria di profili che include qualsiasi tipo di profilo associato a un dispositivo di output hardcopy, ad esempio una stampante. |



 

È possibile creare trasformazioni colore con uno o più profili. Se una trasformazione viene creata con un solo profilo, il profilo deve essere un profilo di collegamento del dispositivo. Una trasformazione può inoltre includere due o più profili in una catena. In caso contrario, non può contenere profili di collegamento del dispositivo. I profili astratti possono trovarsi solo al centro della catena. Il primo e l'ultimo profilo devono essere profili di dispositivo o profili dello spazio dei colori.

 

 
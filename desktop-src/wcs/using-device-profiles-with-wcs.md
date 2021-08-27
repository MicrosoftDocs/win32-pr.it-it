---
title: Uso di profili di dispositivo con WCS
description: I profili di dispositivo sono uno strumento di base per la gestione dei colori.
ms.assetid: 9ea420ad-dcf1-4ba9-b739-308be7a56a6c
keywords:
- Windows Sistema colori (WCS), profili dispositivo
- WCS (Windows Color System), profili dispositivo
- gestione dei colori delle immagini, profili di dispositivo
- gestione dei colori, profili di dispositivo
- colori, profili di dispositivo
- Windows Sistema colori (WCS), profili
- WCS (Windows Color System), profili
- gestione dei colori delle immagini, profili
- gestione dei colori, profili
- colori, profili
- profili di dispositivo
- conversione dei colori
- profili di collegamento del dispositivo
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c8211ff883f8e30e7b67b0168e6da980744b252cbb1b89412fc834ac6370cca
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120090071"
---
# <a name="using-device-profiles-with-wcs"></a>Uso di profili di dispositivo con WCS

I profili di dispositivo sono uno strumento di base per la gestione dei colori. Un [profilo di](d.md) dispositivo è un file che contiene informazioni su come convertire i colori nello spazio colori e la gamma di [colori](./g.md) di un dispositivo specifico in uno spazio colori indipendente dal dispositivo. Lo spazio colori indipendente dal dispositivo utilizzato da ICM2 è denominato spazio di connessione del profilo (PCS). Un profilo di dispositivo contiene anche informazioni su come convertire i colori dal PCS nello spazio colori e nella gamma di colori di un dispositivo specifico.

Questi due set di informazioni sulla conversione vengono usati per la [conversione dei colori e](c.md) la gestione dei colori. Ad esempio, un'immagine può essere creata nello spazio colori e nella gamma di colori di una visualizzazione video. Le informazioni nei file del profilo del dispositivo possono essere usate per visualizzare una rappresentazione di un'immagine stampata. Gli utenti spesso vogliono vedere sullo schermo come cambieranno i colori quando viene stampata un'immagine. Questa operazione è denominata strumenti di correzione. Un'immagine può essere verificata convertendo i colori dalla gamma di colori di origine (lo schermo) in colori [PCS](p.md) e quindi convertendoli dal PCS alla gamma di colori di destinazione (la stampante). L'immagine risultante può essere visualizzata sullo schermo, consentendo all'utente di visualizzare l'aspetto dell'immagine finale quando viene stampata.

Anche i profili di dispositivo consentono usi più complessi. Ad esempio, possono essere usati per avere un'idea dell'aspetto di un'immagine creata su un display video quando viene stampata su una stampante laser ad alta risoluzione. L'esempio diventa più complesso se è presente solo una stampante a getto d'input penna standard su cui eseguire la verifica. ICM2 converte l'immagine dalla [gamma](./g.md) dello schermo nella gamma della stampante inkjet. Da qui viene convertito nella gamma della stampante laser. L'immagine risultante può essere stampata sulla stampante inkjet. Naturalmente l'immagine avrebbe una risoluzione più elevata quando viene stampata sulla stampante a colori. Tuttavia, i colori dell'immagine di prova stampata sulla stampante inkjet corrisponderebbero molto ai colori stampati dalla stampante laser.

Le conversioni da un profilo di dispositivo possono essere concatenate in un singolo file, denominato *profilo di collegamento del dispositivo.* Se si usa più volte una serie di conversioni, la creazione di un profilo di collegamento del dispositivo ridurrà il tempo di conversione.

I profili di dispositivo possono essere gestiti. La gestione dei profili è il processo di associazione dei profili colori alle istanze del dispositivo. A qualsiasi dispositivo di output a colori può essere associato un set di uno o più profili colori. I produttori di hardware e terze parti che forniscono profili colore devono eseguire la gestione dei profili.

I set di profili possono essere condivisi tra dispositivi o dedicati a dispositivi specifici. Si supponga, ad esempio, di avere due stampanti a colori dello stesso modello. Per ogni stampante è necessario associare un set di profili colori. Il set di profili colori per una stampante corrisponde alle varie configurazioni possibili in tale modello. Essendo dello stesso modello, entrambe le stampanti possono condividere un set di profili. L'alternativa consiste nel assegnare a ogni stampante un proprio set di profili distinto. In quest'ultimo caso, i profili colori nel set possono essere calibrati esattamente in base all'output singolo della stampante, non solo alle caratteristiche generali di output del modello.

Esistono tre diverse classi di profili ICC: profili di input, profili di visualizzazione e profili di output. I profili di input sono in genere associati a un dispositivo, ad esempio uno scanner. I profili di visualizzazione sono in genere associati a un monitoraggio del computer. I profili di output sono comunemente associati alle stampanti.

La specifica consente anche profili di dispositivo, profili astratti, profili di collegamento del dispositivo, profili colori denominati e profili dello spazio colori.

Un profilo di dispositivo descrive lo spazio colore di un dispositivo specifico.

Un profilo astratto fornisce un metodo generico per consentire agli utenti di apportare modifiche di colore soggettive alle immagini o agli oggetti grafici trasformando i dati sui colori all'interno del PCS.

Come accennato in precedenza, un profilo di collegamento del dispositivo concatena una serie di profili in un'unica trasformazione.

I profili colori denominati possono essere ritenuti profili di pari livello per i profili di dispositivo. Per un determinato dispositivo sono disponibili uno o più profili di dispositivo per gestire le conversioni dei colori di processo e uno o più profili colori denominati per gestire i colori denominati. Potrebbero essere presenti più profili colori denominati per l'utilizzo di materiali di consumo diversi o più fornitori di colori denominati.

Un profilo dello spazio colori descrive uno spazio colori indipendente dal dispositivo.

La tabella seguente riepiloga i vari tipi di profili.



| Tipo di profilo        | Descrizione                                                                                                                   |
|---------------------|-------------------------------------------------------------------------------------------------------------------------------|
| Profilo astratto    | Profilo che è stato modificato in base alle preferenze specifiche di un utente.                                                     |
| Profilo dello spazio colori | Profilo che descrive uno spazio colori indipendente dal dispositivo.                                                                    |
| Profilo collegamento dispositivo | Serie di profili concatenati in un unico profilo.                                                    |
| Profilo del dispositivo      | Profilo che descrive lo spazio colore di un dispositivo specifico.                                                              |
| Visualizzare il profilo     | Classe o categoria di profili che include qualsiasi tipo di profilo associato a una visualizzazione.                                  |
| Profilo di input       | Classe o categoria di profili che include qualsiasi tipo di profilo associato a un dispositivo di input, ad esempio uno scanner.          |
| Profilo colori denominato | Profilo per uno spazio colori costituito da colori denominati.                                                                    |
| Profili di output     | Classe o categoria di profili che include qualsiasi tipo di profilo associato a un dispositivo di output hardcopy, ad esempio una stampante. |



 

Le trasformazioni di colore possono essere create con uno o più profili. Se viene creata una trasformazione con un solo profilo, il profilo deve essere un profilo di collegamento del dispositivo. Una trasformazione può avere anche due o più profili in una catena. In caso contrario, non può contenere profili di collegamento del dispositivo. I profili astratti possono essere solo al centro della catena. Il primo e l'ultimo profilo devono essere profili di dispositivo o profili di spazio colore.

 

 
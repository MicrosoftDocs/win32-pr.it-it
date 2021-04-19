---
description: Proprietà di esempio MPEG
ms.assetid: 339aab84-e5ad-4071-8b67-2b04cb17e450
title: Proprietà di esempio MPEG
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c20df4b9285a77d00bd98bc6f21558f0d6b3c60
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106304155"
---
# <a name="mpeg-sample-properties"></a>Proprietà di esempio MPEG

Gli esempi MPEG presentano le seguenti caratteristiche.

**Timestamp**

Non tutti gli esempi hanno ora di inizio e di fine. L'ora di arresto dell'esempio per i dati del pacchetto e del payload non è utile. viene in genere impostato sull'ora di inizio più uno. Per gli esempi di dati del pacchetto o del payload MPEG verrà impostata un'ora di avvio e di arresto se il pacchetto a livello di sistema da cui sono stati generati ha un PTS valido.

Per ulteriori informazioni sui timestamp, vedere la sezione 2.4.1 di ISO1-11172: "l'intestazione del pacchetto può contenere i timestamp di decodifica e/o di presentazione (DTS e PTS) che fanno riferimento alla prima unità di accesso nel pacchetto".

Per i \_ tipi principali del flusso MPEG, l'ora di inizio è la posizione in byte del primo byte, valutato a 1 byte al secondo. L'ora di arresto è la posizione in byte dell'ultimo byte. Pertanto, i campioni consecutivi dovrebbero avere l'ora di arresto del primo pacchetto uguale all'ora di inizio del pacchetto successivo. Per i dati del CD video, l'origine del supporto deve corrispondere al formato di un file video CD esposto da CDFS con il blocco RIFF standard all'inizio.

Per i tipi di payload e pacchetti video MPEG, il timestamp è l'ora di presentazione per il primo fotogramma video il cui codice di avvio dell'immagine inizia nell'esempio.

Per i tipi di payload e pacchetti audio MPEG, il timestamp è l'ora di presentazione del primo frame audio il cui codice di sincronizzazione inizia nell'esempio.

Si presuppone che i dati del pacchetto e del payload senza timestamp possano essere registrati correttamente dai filtri di gestione.

**Discontinuità**

Se si verifica un'interruzione nel flusso (ad esempio, un gap nei dati in tempo reale o un errore nei dati o dopo una ricerca), la proprietà discontinuità viene impostata sul campione multimediale successivo. Ciò consente anche una discontinuità dei timestamp.

**Notifiche di fine flusso**

Quando il decodificatore riceve la notifica, deve elaborare i dati memorizzati nel buffer. Tutti i nuovi dati devono quindi iniziare con la proprietà discontinuità.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Supporto MPEG-2 in DirectShow](mpeg-2-support-in-directshow.md)
</dt> </dl>

 

 




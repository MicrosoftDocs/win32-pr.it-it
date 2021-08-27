---
description: Proprietà di esempio MPEG
ms.assetid: 339aab84-e5ad-4071-8b67-2b04cb17e450
title: Proprietà di esempio MPEG
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c78872b41c579f6af594280b064bfbefc65ef13e8b9d4abf8c21ba9b19613bcf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120075791"
---
# <a name="mpeg-sample-properties"></a>Proprietà di esempio MPEG

Gli esempi MPEG hanno le caratteristiche seguenti.

**Timestamp**

Non tutti gli esempi hanno orari di avvio e arresto. Il tempo di arresto dell'esempio per i dati di pacchetto e payload non è utile. è in genere impostato sull'ora di inizio più uno. Gli esempi di dati del pacchetto MPEG o del payload avranno un tempo di avvio e arresto impostato se il pacchetto del livello di sistema da cui vengono generati ha un PTS valido.

Per altre informazioni sui timestamp, vedere la sezione 2.4.1 di ISO1-11172: "L'intestazione del pacchetto può contenere timestamp di decodifica e/o presentazione (DTS e PTS) che fanno riferimento alla prima unità di accesso nel pacchetto".

Per i tipi principali del flusso MPEG, l'ora di inizio è la posizione in byte del primo byte, con una velocità di \_ 1 byte al secondo. L'ora di arresto è la posizione in byte dell'ultimo byte. Pertanto, gli esempi consecutivi devono avere l'ora di arresto del primo pacchetto uguale all'ora di inizio del pacchetto successivo. Per Video CD dati, l'origine del supporto deve corrispondere al formato di un file video-CD esposto da CDFS con il blocco RIFF standard all'inizio.

Per i pacchetti video MPEG e i tipi di payload, il timestamp è l'ora di presentazione per il primo fotogramma video il cui codice di avvio dell'immagine inizia nell'esempio.

Per i tipi di pacchetto e payload audio MPEG, il timestamp è l'ora di presentazione per il primo fotogramma audio il cui codice di sincronizzazione inizia nell'esempio.

Si presuppone che i dati del pacchetto e del payload senza timestamp possano essere prerollati correttamente dai filtri di gestione.

**Discontinuità**

Se si verifica un'interruzione nel flusso (ad esempio, un gap nei dati in tempo reale o un errore nei dati o dopo una ricerca), la proprietà discontinuità viene impostata sull'esempio multimediale successivo. Ciò consente anche una discontinuità del timestamp.

**Notifiche di fine flusso**

Quando il decodificatore riceve questa notifica, deve elaborare tutti i dati memorizzati nel buffer. I nuovi dati devono quindi iniziare con la proprietà discontinuity.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Supporto mpeg-2 in DirectShow](mpeg-2-support-in-directshow.md)
</dt> </dl>

 

 




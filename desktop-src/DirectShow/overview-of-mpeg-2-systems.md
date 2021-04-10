---
description: Panoramica dei sistemi MPEG-2
ms.assetid: 1ebfb194-002f-40ac-9be5-267861b6687b
title: Panoramica dei sistemi MPEG-2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4206b36db7b3172c6e161745922e83490855c73c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104125025"
---
# <a name="overview-of-mpeg-2-systems"></a>Panoramica dei sistemi MPEG-2

Questa sezione fornisce una panoramica generale e non tecnica del livello di sistemi MPEG-2. I sistemi MPEG-2 sono lo standard che definisce la modalità di multiplexing di flussi audio e video in MPEG-2.

**Flussi elementari**

Il multiplexing MPEG-2 inizia con uno o più flussi di byte, detti flussi elementari, che contengono video, audio o altri dati. Ad esempio, un video ES contiene fotogrammi video compressi, più intestazioni di sequenza, intestazioni del gruppo di immagini (GOP) e qualsiasi altro elemento necessario dal decodificatore per decodificare il flusso. Il livello Systems non definisce il contenuto del flusso di byte ES.

Un flusso elementare viene suddiviso in pacchetti, formando un *flusso elementare in pacchetto* (PES). I pacchetti PES hanno una lunghezza variabile. Il contenuto del pacchetto è denominato *payload*. Ogni pacchetto PES include anche un'intestazione. Il multiplexer assegna un ID flusso di 1 byte a ogni PES; i singoli pacchetti PES sono identificati dall'ID del flusso nell'intestazione del pacchetto. Per i flussi audio, l'ID del flusso ha il formato 110 *xxxxx*. Per il video, il formato dell'ID del flusso è 1110 *aaaa*.

Lo standard MPEG-2 definisce due modi per distribuire flussi elementari in pacchetto: *flussi di programma* e flussi di *trasporto*.

**Flussi di programma**

I flussi di programma sono progettati per ambienti che sono relativamente privi di errori, ad esempio l'archiviazione di file locali. In un flusso di programma, i pacchetti PES sono in multiplex e organizzati in unità denominate *Pack*. Tutti i flussi PES in un flusso di programma sono sincronizzati con lo stesso clock.

**Flussi di trasporto**

I flussi di trasporto (TS) sono progettati per ambienti non affidabili o soggetti a errori, ad esempio trasmissioni di rete. Possono inoltre contenere più programmi sincronizzati con orologi diversi. Un flusso di trasporto aggiunge un secondo livello di packetizing: i flussi PES sono inclusi nel pacchetto dei pacchetti di flusso di trasporto, che hanno una dimensione fissa di 188 byte per pacchetto. I pacchetti TS possono contenere anche flussi di informazioni sul programma, descritti nella sezione seguente.

Ogni pacchetto TS dispone di un'intestazione di 4 byte, più un campo di adattamento facoltativo che contiene informazioni aggiuntive sull'intestazione. Il multiplexer assegna un ID programma (PID) a ogni flusso di PES o flusso di informazioni sul programma. I PID vengono usati per identificare i pacchetti di Servizi terminal, in modo analogo al modo in cui gli ID flusso identificano i pacchetti PES. Se un flusso di trasporto contiene più programmi, gli ID del *flusso* potrebbero non essere univoci, ma le assegnazioni PID sono univoche all'interno del flusso di trasporto.

**Informazioni specifiche del programma**

Poiché un flusso di trasporto può includere più programmi, è necessario un modo per associare i diversi pacchetti PES ai programmi a cui appartengono. Questa operazione viene eseguita utilizzando le tabelle che identificano i flussi del programma. Insieme, questi dati sono detti informazioni specifiche del programma. I dati PSI vengono trasportati nei pacchetti TS, esattamente come i dati PES. Sono disponibili vari tipi di dati PSI, tra cui:

-   Tabella Association Program (PAT). PAT viene sempre assegnato a PID 0x000. Ogni voce del PAT è un PID che identifica i pacchetti PMT per il programma (vedere elemento successivo).
-   Tabella della mappa programmi (PMT). Ogni PMT definisce un programma. Il PMT contiene un elenco di flussi; ogni voce della tabella fornisce il PID per quel flusso, oltre a un codice che identifica il tipo di flusso. ISO/IEC 13818-1 definisce alcuni tipi di flusso standard; nella tabella seguente viene illustrato un elenco abbreviato.

    | tipo di flusso \_ | Descrizione  |
    |--------------|--------------|
    | 0x01         | Video MPEG-1 |
    | 0x02         | Video MPEG-2 |
    | 0x03         | Audio MPEG-1 |
    | 0x04         | Audio MPEG-2 |
    | 0x80-0xFF  | Utente privato |

    

     

    Altri standard basati su MPEG-2, ad esempio ATSC, possono definire altri tipi di flusso nell'intervallo "utente privato". Ad esempio, ATSC definisce 0x81 come audio Dolby AC-3.

-   Tabelle di accesso condizionale (CAT)
-   Tabelle di identificazione della rete (NIT)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Supporto MPEG-2 in DirectShow](mpeg-2-support-in-directshow.md)
</dt> </dl>

 

 




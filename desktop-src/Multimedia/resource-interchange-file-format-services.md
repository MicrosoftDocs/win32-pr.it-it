---
title: Servizi di formato file di interscambio di risorse
description: Servizi di formato file di interscambio di risorse
ms.assetid: 8526794b-7b40-470f-94f7-935d7dbf9151
keywords:
- I/O di file multimediali, formato di file di interscambio di risorse (RIFF)
- I/O di file, formato di file di interscambio di risorse (RIFF)
- input e output (I/O), formato di file di interscambio di risorse (RIFF)
- I/O (input e output),formato di file di interscambio di risorse (RIFF)
- Funzione mmioOpen
- resource interchange file format (RIFF)
- RIFF (formato di file di interscambio di risorse)
- RIFF I/O
- Blocco RIFF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5967165996b2a7fb9ed9b40c9a1f3c5608cd3bb4eb1e6cf05ae351f6ce6f2a7d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117801930"
---
# <a name="resource-interchange-file-format-services"></a>Servizi di formato file di interscambio di risorse

Il formato preferito per i file multimediali è riFF (Resource Interchange File Format). Le funzioni di I/O di file RIFF funzionano con i servizi di I/O di file di base memorizzati nel buffer e senza buffer. È possibile aprire, leggere e scrivere file RIFF nello stesso modo di altri tipi di file. Per informazioni dettagliate su RIFF, vedere [Funzioni e macro AVIFile](avifile-functions-and-macros.md).

I file RIFF usano codici di quattro caratteri per identificare gli elementi del file. Questi codici sono quantità a 32 bit che rappresentano una sequenza da uno a quattro caratteri alfanumerici ASCII, riempiti a destra con spazi. Il tipo di dati per i codici a quattro caratteri è **FOURCC.** Usare la macro [**mmioFOURCC**](/windows/win32/api/vfw/nf-vfw-mmiofourcc) per convertire quattro caratteri in un codice a quattro caratteri. Per convertire una stringa con terminazione Null in un codice a quattro caratteri, usare la funzione [**mmioStringToFOURCC.**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiostringtofourcc)

Il blocco predefinito di base di un file RIFF è un *blocco*. Un blocco è un'unità logica di dati multimediali, ad esempio un singolo fotogramma in un clip video. Ogni blocco contiene i campi seguenti:

-   Codice di quattro caratteri che specifica l'identificatore di blocco
-   Valore doubleword che specifica le dimensioni del membro dati nel blocco
-   Un campo dati

La figura seguente mostra un blocco "RIFF" che contiene due sottochunk.

![blocco riff che contiene due immagini subchunk](images/mmio1.gif)

Un blocco contenuto in un altro blocco è *un sottochunk*. Gli unici blocchi consentiti per contenere subchunk sono quelli con un identificatore di blocco "RIFF" o "LIST". Un blocco che contiene un altro blocco è detto *blocco padre.* Il primo blocco in un file RIFF deve essere un blocco "RIFF". Tutti gli altri blocchi nel file sono sottofase del blocco "RIFF".

I blocchi "RIFF" includono un campo aggiuntivo nei primi quattro byte del campo dati. Questo campo aggiuntivo fornisce *il tipo di* modulo del campo. Il tipo di modulo è un codice di quattro caratteri che identifica il formato dei dati archiviati nel file. Ad esempio, i file waveform-audio Microsoft hanno un tipo di formato "WAVE".

I blocchi "LIST" includono anche un campo aggiuntivo nei primi quattro byte del campo dati. Questo campo aggiuntivo contiene il *tipo di* elenco del campo. Il tipo di elenco è un codice di quattro caratteri che identifica il contenuto dell'elenco. Ad esempio, un blocco "LIST" con tipo di elenco "INFO" può contenere blocchi "ICOP" e "ICRD" che forniscono informazioni sul copyright e sulla data di creazione. La figura seguente mostra un blocco "RIFF" che contiene un blocco "LIST" e un altro sottochunk (il blocco "LIST" contiene due sottofase).

![blocco riff che contiene un'immagine del blocco elenco](images/mmio2.gif)

I servizi di I/O di file multimediali includono due funzioni che è possibile usare per spostarsi tra blocchi in un file RIFF: [**mmioAscend**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioascend) e [**mmioDescend.**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiodescend) È possibile usare queste funzioni come funzioni di ricerca di alto livello. Quando si scende in un blocco, la posizione del file viene impostata sul campo dati del blocco (8 byte dall'inizio del blocco). Per i blocchi "RIFF" e "LIST", la posizione del file viene impostata sul percorso che segue il tipo di modulo o di elenco (12 byte dall'inizio del blocco). Quando si esce da un blocco, la posizione del file viene impostata sul percorso dopo la fine del blocco.

Per creare un nuovo blocco, usare la funzione [**mmioCreateChunk**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiocreatechunk) per scrivere un'intestazione di blocco nella posizione corrente in un file aperto. Le funzioni **mmioAscend**, **mmioDescend** e **mmioCreateChunk** usano la [**struttura MMCKINFO**](/windows/win32/api/mmiscapi/ns-mmiscapi-mmckinfo) per specificare e recuperare informazioni sui blocchi "RIFF".

 

 
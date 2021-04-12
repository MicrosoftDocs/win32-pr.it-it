---
title: Servizi formato file di interscambio risorse
description: Servizi formato file di interscambio risorse
ms.assetid: 8526794b-7b40-470f-94f7-935d7dbf9151
keywords:
- I/O file multimediale, formato file di interscambio risorse (RIFF)
- I/O file, formato file di interscambio risorse (RIFF)
- input e output (I/O), formato del file di interscambio delle risorse (RIFF)
- I/O (input e output), formato del file di interscambio delle risorse (RIFF)
- mmioOpen (funzione)
- formato file di interscambio risorse (RIFF)
- RIFF (formato file di interscambio risorse)
- I/O RIFF
- Blocco RIFF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50cca3792ccded248951065c7b69f2e50d27e0ba
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104336870"
---
# <a name="resource-interchange-file-format-services"></a>Servizi formato file di interscambio risorse

Il formato preferito per i file multimediali è il formato di file di interscambio risorse (RIFF). Le funzioni di I/O dei file RIFF funzionano con i servizi di i/O dei file di base memorizzati nel buffer e non memorizzati nel buffer. È possibile aprire, leggere e scrivere file RIFF nello stesso modo degli altri tipi di file. Per informazioni dettagliate su RIFF, vedere [avifile Functions and Macros](avifile-functions-and-macros.md).

I file RIFF usano codici di quattro caratteri per identificare gli elementi del file. Questi codici sono quantità a 32 bit che rappresentano una sequenza da uno a quattro caratteri alfanumerici ASCII, con riempimento a destra con caratteri di spazio. Il tipo di dati per i codici a quattro caratteri è **fourcc**. Usare la macro [**mmioFOURCC**](/windows/win32/api/vfw/nf-vfw-mmiofourcc) per convertire quattro caratteri in un codice di quattro caratteri. Per convertire una stringa con terminazione null in un codice di quattro caratteri, usare la funzione [**mmioStringToFOURCC**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiostringtofourcc) .

Il blocco predefinito di base *di un file* riff è un blocco. Un blocco è un'unità logica di dati multimediali, ad esempio un singolo frame in un clip video. Ogni blocco contiene i campi seguenti:

-   Codice di quattro caratteri che specifica l'identificatore del blocco
-   Valore parola doppia che specifica la dimensione del membro dati nel blocco
-   Un campo dati

La figura seguente mostra un blocco "RIFF" che contiene due sottoblocchi.

![blocco riff che contiene l'immagine di due sottoblocchi](images/mmio1.gif)

Un blocco contenuto in un altro blocco è un *sottoblocco*. Gli unici blocchi consentiti per contenere sottoblocchi sono quelli con un identificatore di blocco "RIFF" o "LIST". Un blocco contenente un altro blocco viene chiamato *blocco padre*. Il primo blocco in un file RIFF deve essere un blocco "RIFF". Tutti gli altri blocchi del file sono sottoblocchi del blocco "RIFF".

I blocchi "RIFF" includono un campo aggiuntivo nei primi quattro byte del campo dati. Questo campo aggiuntivo fornisce il *tipo di form* del campo. Il tipo di modulo è un codice di quattro caratteri che identifica il formato dei dati archiviati nel file. Ad esempio, Microsoft waveform-file audio hanno un tipo di modulo "WAVE".

I blocchi "LIST" includono anche un campo aggiuntivo nei primi quattro byte del campo dati. Questo campo aggiuntivo contiene il *tipo di elenco* del campo. Il tipo di elenco è costituito da un codice di quattro caratteri che identifica il contenuto dell'elenco. Ad esempio, un blocco "LIST" con un tipo di elenco "INFO" può contenere blocchi "ICOP" e "ICRD" che forniscono informazioni sul copyright e sulla data di creazione. La figura seguente mostra un blocco "RIFF" che contiene un blocco "LIST" e un altro sottoblocco (il blocco "LIST" contiene due sottoblocchi).

![blocco riff che contiene un'immagine del blocco di elenco](images/mmio2.gif)

I servizi di I/O dei file multimediali includono due funzioni che è possibile usare per spostarsi tra I blocchi in un file RIFF: [**mmioAscend**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioascend) e [**mmioDescend**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiodescend). È possibile utilizzare queste funzioni come funzioni di ricerca di alto livello. Quando si scende in un blocco, la posizione del file viene impostata sul campo dati del blocco (8 byte dall'inizio del blocco). Per i blocchi "RIFF" ed "LIST", la posizione del file è impostata sulla posizione successiva al tipo di modulo o al tipo di elenco (12 byte dall'inizio del blocco). Quando si esce da un blocco, la posizione del file viene impostata sulla posizione successiva alla fine del blocco.

Per creare un nuovo blocco, usare la funzione [**mmioCreateChunk**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiocreatechunk) per scrivere un'intestazione di blocco nella posizione corrente in un file aperto. Le funzioni **mmioAscend**, **mmioDescend** e **mmioCreateChunk** usano la struttura [**MMCKINFO**](/windows/win32/api/mmiscapi/ns-mmiscapi-mmckinfo) per specificare e recuperare informazioni sui blocchi "riff".

 

 
---
description: Il componente principale dell'interfaccia di stampa è lo spooler di stampa.
ms.assetid: 36ffb001-78e2-4fa0-8241-3891493ac02d
title: Spooler di stampa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52bac19b44ebed5762abdb00b9ea044cf775a7a7ca8193c641709ad2c39436dd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119033929"
---
# <a name="print-spooler"></a>Spooler di stampa

Il componente principale dell'interfaccia di stampa è lo spooler di stampa. Lo spooler di stampa è un file eseguibile che gestisce il processo di stampa. La gestione della stampa comporta il recupero della posizione del driver della stampante corretto, il caricamento del driver, lo spooling di chiamate di funzioni di alto livello in un processo di stampa, la pianificazione del processo di stampa per la stampa e così via. Lo spooler viene caricato all'avvio del sistema e continua a essere eseguito fino all'arresto del sistema operativo.

Le applicazioni che stampano creano un contesto di dispositivo (DC) della stampante. Quando un'applicazione crea un controller di dominio della stampante, lo spooler esegue le attività necessarie, ad esempio la determinazione del percorso del driver della stampante richiesto e il caricamento del driver. Lo spooler di stampa determina anche il tipo di dati utilizzato per registrare il processo di stampa.

Lo spooler di stampa supporta i tipi di dati seguenti:

-   Metafile avanzato (EMF).
-   Testo ASCII.
-   Dati non elaborati, che includono tipi di dati della stampante, ad esempio PostScript, PCL e tipi di dati personalizzati.

È possibile aggiungere tipi di dati personalizzati per lo spooler installando driver della stampante e processori di stampa aggiuntivi. Un processo di stampa è un documento archiviato internamente e codificato usando uno dei tipi di dati supportati e un processo di stampa può contenere una o più pagine di output. Il processo di stampa può essere costituito da più moduli. ad esempio, un processo può essere costituito da una busta e da tre pagine di carta A4. Un processo di stampa viene definito (o racchiuso tra parentesi) dalle [**funzioni StartDoc**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca) [**ed EndDoc.**](/windows/desktop/api/Wingdi/nf-wingdi-enddoc)

Il tipo di dati predefinito per un processo di stampa è il metafile avanzato. Un record EMF è una struttura compatta usata per archiviare comandi di output di testo, comandi di grafica raster e così via. Quando un'applicazione chiama [**StartDoc,**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca)lo spooler crea un file di spooling e un file di dati e inizia a archiviare i record EMF nel file di spooling. Ogni volta che l'applicazione chiama una delle funzioni di disegno GDI, uno o più nuovi record EMF vengono creati e archiviati nel file di spooling. I file di spool e di dati vengono creati in una directory del sistema operativo. Lo spooler usa il file di spooling per archiviare i record EMF e usa il file di dati per registrare il tipo di modulo, il tipo di dati per il processo di stampa, la stampante di destinazione e così via. Lo spooler elimina questi file al termine della stampa del processo.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Metafile in formato avanzato](/windows/desktop/gdi/enhanced-format-metafiles)
</dt> </dl>

 

 

---
title: Stringhe di formato dei rapporti di mancato recapito RPC
description: Stringhe di formato NDR RPC (Remote Procedure Call).
ms.assetid: 9c83a039-49d3-491d-8110-29d1548730de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d0a481e2c992f3fd4dda2d5552fbbabb7e9b01e6eb639a092e25ba9a26bd59a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118926305"
---
# <a name="rpc-ndr-format-strings"></a>Stringhe di formato dei rapporti di mancato recapito RPC

## <a name="ndr-engine-32-bit-interpreter"></a>Motore NDR: interprete a 32 bit

Questo documento descrive i descrittori di stringa di formato, talvolta definiti MOP, per il motore NDR a 32 bit. Questa sezione descrive le modifiche associate all'evoluzione dall'interprete [**–Oi**](/windows/desktop/Midl/-oi) al livello dell'interprete **–Oif,** nonché le aggiunte correlate alle pipe e al supporto asincrono.

Questo documento descrive la tecnologia MIDL (Current Microsoft Interface Definition Language) dal punto di vista del motore e il motore NDR corrente.

## <a name="overview"></a>Panoramica

Il motore NDR è il motore di marshalling dei componenti RPC (Remote Procedure Call) e DCOM. Gestisce tutti i problemi relativi agli stub di una chiamata remota. Come processo, il marshalling NDR è guidato dal codice C da stub generati da MIDL, da un generatore di tipo JIT MIDL o da stub generati da altri strumenti o scritti manualmente. A sua volta, il motore NDR determina il runtime sottostante (DCOM o RPC) che comunica con trasporti specifici.

L'obiettivo originale della progettazione era fornire uno strumento per il marshalling efficace dei dati arbitrari, in base alle informazioni fornite dal compilatore MIDL. Le stringhe di formato descritte in questo documento, e in effetti tutte le informazioni generate dal compilatore per l'utilizzo del motore NDR, sono sempre state considerate un'interfaccia interna tra il compilatore e il motore. Analogamente, anche le interfacce disponibili per il motore per gestire i problemi di runtime sono per lo più interne (sul lato runtime RPC esistono alcune eccezioni e alcune interfacce DCOM usate dal motore sono esterne).

Due approcci tipici al marshalling sono sempre stati la tecnologia inline e basata sui dati (interpretata). MIDL supporta entrambe le opzioni [**–Os**](/windows/desktop/Midl/-os) e [**\* –Oi**](/windows/desktop/Midl/-oi) negli stub generati da C. INOLTRE, MIDL può generare le librerie TLB usate dal pacchetto oleautomation. Di conseguenza, una prospettiva degli elementi interni del motore è che è costituita da due parti.

La prima è un set di routine che gestiscono il ridimensionamento, il marshalling e così via, corrispondenti a oggetti tipo di dati tipici, ad esempio una struttura o una matrice. Queste routine sono ottimizzate per le prestazioni. ad esempio, in genere tentano di bloccare la copia dei dati laddove possibile. Questa parte viene spesso definita motore NDR principale.

La seconda parte è costituita da un interprete e dai relativi elementi correlati. L'interprete usa routine del motore NDR principale, come da una libreria interna, per eseguire una chiamata remota con tutti gli argomenti sottoposti a marshalling e di cui è stato eseguito il marshalling, in base alle esigenze.

Il motore NDR di base viene usato in modo simile sia dagli stub inline che dall'interprete. Tutte le routine del motore di base dipendono dallo stato passato da una struttura di messaggi stub. La struttura viene impostata in modo appropriato dallo stub inline o dall'interprete. Nel corso degli anni il motore principale era stato usato in un contesto diverso; attualmente l'interprete è in realtà un set di diversi cicli di interprete distinti. Questi sono correlati agli interpreti vecchi e nuovi ([**–Oi**](/windows/desktop/Midl/-oi) e **–Oif**), nonché ai cicli correlati alla serializzazione dei dati (pickling), al supporto asincrono RPC e al supporto asincrono DCOM (RPC e DCOM hanno modelli di programmazione asincroni diversi).

Oltre all'aggiunta di nuove funzionalità, un aspetto importante dell'evoluzione del motore NDR è un cambiamento generale nell'approccio agli interpreti. NDR versione 1.1 è iniziato come parte di un nuovo approccio MIDL 2.0 al marshalling, con gli stub inline preferiti per considerazioni sulle prestazioni. Con la versione più recente del rapporto di mancato recapito, [**–Oif**](/windows/desktop/Midl/-oi) è diventato la modalità più usata del compilatore, quasi all'esclusione degli stub inline.

I descrittori di stringa di formato del motore NDR RPC sono descritti in modo più dettagliato negli argomenti seguenti:

-   [Stringhe di formato](format-strings.md)
-   [Stringhe di formato della procedura](procedure-format-strings.md)
-   [Descrittore dell'intestazione della procedura](procedure-header-descriptor.md)
-   [Selettori](handles.md)
-   [Intestazione](the-header.md)
-   [Descrittori di parametri](parameter-descriptors.md)
-   [Stringhe di formato dei tipi](type-format-strings.md)

 

 
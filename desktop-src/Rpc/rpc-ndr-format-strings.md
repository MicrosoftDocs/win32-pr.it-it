---
title: Stringhe di formato di recapito RPC
description: Stringhe di formato NDR RPC (Remote Procedure Call).
ms.assetid: 9c83a039-49d3-491d-8110-29d1548730de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf0569a913d6c5a4b19b342cc288d6a8682dfc4a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103872890"
---
# <a name="rpc-ndr-format-strings"></a>Stringhe di formato di recapito RPC

## <a name="ndr-engine-32-bit-interpreter"></a>Motore NDR: interprete a 32 bit

In questo documento vengono descritti i descrittori di stringhe di formato, detti anche MOPs, per il motore di NDR a 32 bit. In questa sezione vengono descritte le modifiche associate all'evoluzione dall'interprete [**-OI**](/windows/desktop/Midl/-oi) al livello dell'interprete **-OIF** , nonché le aggiunte correlate alle pipe e al supporto asincrono.

In questo documento viene descritta la tecnologia Current Microsoft Interface Definition Language (MIDL) dal punto di vista del motore e il motore NDR corrente.

## <a name="overview"></a>Panoramica

Il motore di mancato recapito è il motore di marshalling dei componenti RPC (Remote Procedure Call) e DCOM. Gestisce tutti i problemi relativi agli stub di una chiamata remota. Come processo, il marshalling del rapporto di recapito è determinato dal codice C da stub generati da MIDL, da un generatore di tipi JIT MIDL o da stub generati da altri strumenti o scritti manualmente. Il motore di NDR, a sua volta, determina il tempo di esecuzione sottostante (DCOM o RPC) che comunica con trasporti specifici.

L'obiettivo originale della progettazione era quello di fornire uno strumento per il marshalling efficace per i dati arbitrari, in base alle informazioni fornite dal compilatore MIDL. Le stringhe di formato descritte in questo documento, ed effettivamente tutte le informazioni generate dal compilatore per l'utilizzo del motore NDR, sono sempre state considerate un'interfaccia interna tra il compilatore e il motore. Analogamente, le interfacce disponibili per il motore di per gestire i problemi in fase di esecuzione sono principalmente interne (alcune eccezioni sono presenti sul lato run-time RPC e alcune interfacce DCOM utilizzate dal motore sono esterne).

Due approcci tipici al marshalling sono sempre stati inline e tecnologia basata sui dati (interpretata). MIDL supporta entrambi i commutatori [**-OS**](/windows/desktop/Midl/-os) e [**-OI \***](/windows/desktop/Midl/-oi) negli stub generati da C. MIDL può inoltre generare le librerie TLB utilizzate dal pacchetto oleautomation. Di conseguenza, una prospettiva degli elementi interni del motore è costituita da due parti.

Il primo è un set di routine che gestiscono il ridimensionamento, il marshalling e così via, corrispondenti a oggetti tipici del tipo di dati, ad esempio una struttura o una matrice. Queste routine sono ottimizzate per migliorare le prestazioni. ad esempio, in genere tentano di bloccare la copia dei dati laddove possibile. Questa parte è spesso definita motore di recapito di base.

La seconda parte è costituita da un interprete e dagli elementi correlati. L'interprete usa le routine del motore di recapito centrale, come se si trattasse di una libreria interna, per eseguire una chiamata remota con tutti i relativi argomenti sottoposti a marshalling e senza marshalling, a seconda dei casi.

Il motore di recapito di base viene usato in modo analogo, indipendentemente dal fatto che venga usato dagli Stub inline o dall'interprete. Tutte le routine del motore di base dipendono dallo stato passato da una struttura di messaggi stub. La struttura viene configurata in modo appropriato dallo stub inline o dall'interprete. Nel corso degli anni il motore principale era stato usato in un contesto diverso; Attualmente l'interprete è in realtà un set di diversi cicli di interprete distinti. Queste sono correlate agli interpreti vecchi e nuovi ([**-OI**](/windows/desktop/Midl/-oi) versus **-OIF**), nonché ai cicli correlati alla serializzazione dei dati (selezione), al supporto asincrono RPC e al supporto asincrono DCOM (RPC e DCOM hanno modelli di programmazione asincroni diversi).

Oltre all'aggiunta di nuove funzionalità, un aspetto importante dell'evoluzione del motore NDR è un cambiamento generale nell'approccio agli interpreti. NDR versione 1.1 è iniziata come parte di un nuovo approccio MIDL 2,0 al marshalling, con gli stub inline preferiti per le considerazioni sulle prestazioni. Con la versione più recente di NDR, [**– OIF**](/windows/desktop/Midl/-oi) è diventata la modalità più utilizzata del compilatore, quasi all'esclusione degli stub inline.

I descrittori di stringa di formato del motore di recapito RPC sono descritti in modo più dettagliato negli argomenti seguenti:

-   [Stringhe di formato](format-strings.md)
-   [Stringhe di formato delle procedure](procedure-format-strings.md)
-   [Descrittore di intestazioni di routine](procedure-header-descriptor.md)
-   [Selettori](handles.md)
-   [Intestazione](the-header.md)
-   [Descrittori di parametro](parameter-descriptors.md)
-   [Stringhe di formato del tipo](type-format-strings.md)

 

 
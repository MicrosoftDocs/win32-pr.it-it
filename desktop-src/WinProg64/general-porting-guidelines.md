---
title: Linee guida generali per il porting
description: Il porting di applicazioni a 32 bit in Microsoft Windows a 64 bit sarà più semplice del porting di applicazioni a 16 bit in Windows a 32 bit. Tuttavia, lo spostamento andrà più agevolmente con un'attenta pianificazione. Di seguito sono riportate alcune linee guida generali.
ms.assetid: 28c1656e-93a2-441b-8946-18017e0b2b29
keywords:
- porting di applicazioni a 32 bit alla programmazione Windows a 64 bit di Windows a 64 bit
- Guida alla programmazione di Windows a 64 bit Guida alla programmazione Windows a 64 bit, linee guida per il porting
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d31734edd8b85bd61b8b84cb2c66d835f0085ac1
ms.sourcegitcommit: 35bb565804eaeed7ac5503595753f59d120076dd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "104234430"
---
# <a name="general-porting-guidelines"></a>Linee guida generali per il porting

Il porting di applicazioni a 32 bit in Microsoft Windows a 64 bit sarà più semplice del porting di applicazioni a 16 bit in Windows a 32 bit. Tuttavia, lo spostamento andrà più agevolmente con un'attenta pianificazione. Di seguito sono riportate alcune linee guida generali.

## <a name="planning"></a>Pianificazione

-   Determinare l'entità del lavoro richiesto per la porta. Misurare la quantità di lavoro che è necessario identificando gli elementi seguenti:
    -   Problema codice a 32 bit. Compilare il codice a 32 bit con il compilatore a 64 bit ed esaminare la portata degli errori e degli avvisi.
    -   Componenti o dipendenze condivise. Determinare quali componenti dell'applicazione hanno origine da altri team e se tali team pianificano di sviluppare versioni a 64 bit del codice.
    -   Codice dell'assembly o legacy. le applicazioni basate su Windows a 16 bit non vengono eseguite in Windows a 64 bit ed è necessario riscriverle. Sebbene il codice assembly x86 venga eseguito in WOW64, può essere utile riscrivere questo codice per sfruttare la velocità dell'architettura Intel Itanium.
-   Trasferire l'intera applicazione, non solo parti di esso.

    Sebbene sia possibile trasferire parti di un'applicazione o limitare il codice a 2G con/LARGEADDRESSAWARE: NO, questa strategia commercia il guadagno a breve termine per il dolore a lungo termine.

    > [!Note]  
    > /LARGEADDRESSAWARE: NO viene ignorato per un file binario ARM64.

     

-   Trovare sostituzioni per le tecnologie che non verranno trasferite.

    Alcune tecnologie, tra cui DAO (Data Access Object) e il motore di database Jet Red, non verranno trasferite in Windows a 64 bit.

-   Considerare la versione a 64 bit come versione del prodotto separata.

    Anche se il prodotto a 64 bit può condividere la stessa codebase del 32 bit, è necessario un test aggiuntivo e potrebbe avere altre considerazioni sulla versione.

## <a name="development"></a>Sviluppo

-   Inizia subito a sviluppare codice conforme.

    Gli sviluppatori possono iniziare a scrivere codice conforme usando i file di intestazione di Windows più recenti e i nuovi tipi di dati senza effetti negativi sullo sviluppo di prodotti a 32 bit. Per altre informazioni, vedere [preparazione per Windows a 64 bit](getting-ready-for-64-bit-windows.md).

-   Verificare che sia possibile compilare il codice per Windows a 32 e a 64 bit.

    Il nuovo modello di dati è stato progettato per consentire la compilazione di applicazioni a 32 e 64 bit da una singola codebase con poche modifiche. I team di sviluppo SQL Server e Windows sviluppano versioni 32 e 64 dei prodotti dalla stessa codebase.

-   Utilizzare le nuove funzionalità di ottimizzazione del compilatore per ottenere prestazioni ottimali.

    L'ottimizzazione del codice per i processori Intel Itanium è più importante rispetto a quella di x86. Il compilatore presuppone la maggior parte delle funzioni di ottimizzazione precedentemente gestite dal microprocessore. È possibile ottimizzare le prestazioni di un'applicazione a 64 bit utilizzando due nuove funzionalità di ottimizzazione del compilatore: *ottimizzazione* PGO e *ottimizzazione programma intera*. Entrambe le funzionalità generano tempi di compilazione più lunghi e richiedono lo sviluppo iniziale di scenari di test efficaci.

    L' *ottimizzazione* PGO prevede un processo di compilazione in due passaggi. Durante la prima compilazione, il codice viene instrumentato per acquisire il comportamento di esecuzione. Queste informazioni vengono usate durante la seconda compilazione per guidare tutte le funzionalità di ottimizzazione.

    L' *ottimizzazione dell'intero programma* analizza il codice in tutti i file dell'applicazione, non solo uno. Questo approccio aumenta le prestazioni in diversi modi, tra cui l'incorporamento migliore, nonché l'analisi degli effetti collaterali migliorata e le convenzioni di chiamata personalizzate.

## <a name="testing"></a>Test

-   Determinare se testare il codice 64 o 32 bit in esecuzione in WOW64.

    Alcune applicazioni includono codice nativo a 64 bit e codice a 32 bit in esecuzione in WOW64. Esaminare attentamente questo oggetto durante lo sviluppo di un piano di test e decidere se gli strumenti di test devono essere a 64 bit, a 32 bit o a una combinazione. Spesso è necessario testare entrambe le versioni a 64 e 32 bit dell'applicazione in Windows a 64 bit.

-   Testare i componenti di uso frequente a 32 bit.

    Innanzitutto, ricompilare il codice a 64 bit e testare. In secondo luogo, risolvere i problemi, ricompilare in 32 bit e quindi eseguire il test. Terzo, ricompilare a 64 bit e testare.

-   Testare i componenti COM e RPC.

    Assicurarsi che i componenti COM e RPC sia a 32 che a 64 bit comunicano correttamente. Potrebbe inoltre essere necessario testare le comunicazioni con componenti a 16 bit in una rete.

-   Testare la versione a 32 bit su Windows a 64 bit.

    I clienti possono continuare a usare applicazioni a 32 bit su Windows a 64 bit in cui i problemi di prestazioni e memoria non sono considerazioni principali.

-   Testare configurazioni di memoria diverse.

    L'aggiunta di grandi quantità di memoria nel server talvolta espone problemi precedentemente inosservati nell'applicazione o nel sistema operativo.

 

 





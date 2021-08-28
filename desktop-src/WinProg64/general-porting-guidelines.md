---
title: Linee guida generali sulla portabilità
description: Il porting di applicazioni a 32 bit in Microsoft Windows a 64 bit sarà più semplice rispetto al porting di applicazioni a 16 bit in applicazioni a 32 bit Windows. Tuttavia, lo spostamento sarà più semplice con un'attenta pianificazione. Di seguito sono riportate alcune linee guida generali.
ms.assetid: 28c1656e-93a2-441b-8946-18017e0b2b29
keywords:
- porting di applicazioni a 32 bit a 64 bit Windows programmazione Windows a 64 bit
- Guida alla programmazione Windows a 64 bit a 64 bit Windows programmazione a 64 bit , linee guida per la portabilità
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a586318ecc6ec8852077052cbcff41bffacff6c35c36d23de4b020ce19f12af
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119680241"
---
# <a name="general-porting-guidelines"></a>Linee guida generali sulla portabilità

Il porting di applicazioni a 32 bit in Microsoft Windows a 64 bit sarà più semplice rispetto al porting di applicazioni a 16 bit in applicazioni a 32 bit Windows. Tuttavia, lo spostamento sarà più semplice con un'attenta pianificazione. Di seguito sono riportate alcune linee guida generali.

## <a name="planning"></a>Pianificazione

-   Determinare l'entità del lavoro necessario per la porta. Misurare la quantità di lavoro coinvolta identificando gli elementi seguenti:
    -   Codice a 32 bit problematico. Compilare il codice a 32 bit con il compilatore a 64 bit ed esaminare l'entità degli errori e degli avvisi.
    -   Componenti condivisi o dipendenze. Determinare quali componenti dell'applicazione provengono da altri team e se tali team pianificano lo sviluppo di versioni a 64 bit del codice.
    -   Codice legacy o assembly. Le applicazioni Windows a 16 bit non vengono eseguite su Windows a 64 bit e devono essere riscritte. Mentre il codice assembly x86 viene eseguito in WOW64, è possibile riscrivere questo codice per sfruttare la velocità dell'architettura Intel Itanium.
-   Convertire l'intera applicazione, non solo parti di essa.

    Anche se è possibile convertire parti di un'applicazione o limitare il codice a 2G con /LARGEADDRESSAWARE:NO, questa strategia commercia il guadagno a breve termine per un problema a lungo termine.

    > [!Note]  
    > /LARGEADDRESSAWARE:NO viene ignorato per un file binario ARM64.

     

-   Trovare sostituzioni per le tecnologie che non verranno portate.

    Alcune tecnologie, tra cui DAO (Data Access Object) e il motore di database Jet Red, non verranno portate a Windows a 64 bit.

-   Considerare la versione a 64 bit come versione separata del prodotto.

    Anche se il prodotto a 64 bit può condividere la stessa base di codice a 32 bit, richiede test aggiuntivi e può avere altre considerazioni sulla versione.

## <a name="development"></a>Sviluppo

-   Iniziare subito a sviluppare codice conforme.

    Gli sviluppatori possono iniziare a scrivere codice conforme usando i file di intestazione Windows più recenti e i nuovi tipi di dati senza effetti negativi sullo sviluppo di prodotti a 32 bit. Per altre informazioni, vedere [Getting Ready for 64-bit Windows](getting-ready-for-64-bit-windows.md).

-   Assicurarsi che il codice possa essere compilato sia per i file a 32 che a 64 bit Windows.

    Il nuovo modello di dati è stato progettato per consentire la creazione di applicazioni a 32 e 64 bit da una singola codebase con poche modifiche. I SQL Server e Windows di sviluppo stanno sviluppando versioni a 32 e 64 bit dei prodotti dalla stessa codebase.

-   Usare le nuove funzionalità di ottimizzazione del compilatore per ottenere prestazioni ottimali.

    L'ottimizzazione del codice per i processori Intel Itanium è più importante di quanto non lo fosse per x86. Il compilatore presuppone che molte delle funzioni di ottimizzazione gestite in precedenza dal microprocessore. È possibile ottimizzare le prestazioni di un'applicazione a 64 bit usando due nuove funzionalità di ottimizzazione del compilatore: *Ottimizzazione* guidata profilo e *Ottimizzazione dell'intero programma.* Entrambe le funzionalità comportano tempi di compilazione più lunghi e richiedono lo sviluppo anticipato di scenari di test di qualità.

    *L'ottimizzazione PGO* prevede un processo di compilazione in due passaggi. Durante la prima compilazione, il codice viene instrumentato per acquisire il comportamento di esecuzione. Queste informazioni vengono usate durante la seconda compilazione per guidare tutte le funzionalità di ottimizzazione.

    *Ottimizzazione dell'intero* programma analizza il codice in tutti i file dell'applicazione, non solo uno. Questo approccio aumenta le prestazioni in diversi modi, tra cui una migliore inlining, nonché un'analisi degli effetti collaterali migliorata e convenzioni di chiamata personalizzate.

## <a name="testing"></a>Test

-   Determinare se si testerà codice a 64 o 32 bit in esecuzione in WOW64.

    Alcune applicazioni includono sia codice nativo a 64 bit che codice a 32 bit in esecuzione in WOW64. Esaminare attentamente questo problema durante lo sviluppo di un piano di test e decidere se gli strumenti di test devono essere a 64 bit, a 32 bit o una combinazione. Spesso è necessario testare entrambe le versioni a 64 e 32 bit dell'applicazione in Windows.

-   Testare i componenti a 32 bit usati di frequente.

    Prima di tutto, ricompilare il codice a 64 bit e testare. In secondo piano, correggere i problemi, ricompilare a 32 bit e quindi testare. In terzo piano, ricompilare a 64 bit e testare.

-   Testare i componenti COM e RPC.

    Assicurarsi che i componenti COM e RPC a 32 e 64 bit comunichino correttamente. Potrebbe anche essere necessario testare le comunicazioni con componenti a 16 bit in rete.

-   Testare la versione a 32 bit in una versione a 64 bit Windows.

    I clienti possono continuare a usare applicazioni a 32 bit in applicazioni a 64 bit Windows in cui i problemi di prestazioni e memoria non sono considerazioni importanti.

-   Testare configurazioni di memoria diverse.

    L'aggiunta di grandi quantità di memoria nel server talvolta espone problemi precedentemente inosservati nell'applicazione o nel sistema operativo.

 

 





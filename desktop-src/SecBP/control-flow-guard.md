---
description: Il controllo del flusso di controllo (CFG) è una funzionalità di sicurezza della piattaforma altamente ottimizzata che è stata creata per combattere le vulnerabilità di danneggiamento della memoria.
ms.assetid: 116EAD64-7CAE-455C-BA43-9492F78DE873
title: Protezione del flusso di controllo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91cf97a648443135e7fee666ea4c259b1c32104e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104132023"
---
# <a name="control-flow-guard"></a>Protezione del flusso di controllo

## <a name="what-is-control-flow-guard"></a>Che cos'è la protezione del flusso di controllo?

Il controllo del flusso di controllo (CFG) è una funzionalità di sicurezza della piattaforma altamente ottimizzata che è stata creata per combattere le vulnerabilità di danneggiamento della memoria. Ponendo restrizioni restrittive su dove un'applicazione può eseguire il codice, rende molto più difficile per gli exploit eseguire codice arbitrario attraverso vulnerabilità come gli overflow del buffer. CFG estende le tecnologie di mitigazione degli exploit precedenti, ad esempio [/GS](/cpp/build/reference/gs-buffer-security-check?view=vs-2019), [DEP](../memory/data-execution-prevention.md)e [ASLR](/archive/blogs/michael_howard/address-space-layout-randomization-in-windows-vista).

Questa funzionalità è disponibile in Microsoft Visual Studio 2015 e viene eseguita su versioni di Windows compatibili con CFG, ovvero le versioni x86 e x64 per desktop e server di Windows 10 e Windows 8.1 Update (KB3000850).

Si consiglia agli sviluppatori di abilitare la CFG per le proprie applicazioni. Non è necessario abilitare la funzionalità CFG per ogni parte del codice, perché una combinazione di CFG abilitata e il codice non abilitato per la CFG verrà eseguita correttamente. Tuttavia, la mancata abilitazione di CFG per tutto il codice può aprire gap nella protezione. Inoltre, il codice abilitato per la funzionalità CFG funziona correttamente nelle versioni di Windows "non compatibili con CFG" ed è quindi completamente compatibile con loro.

## <a name="how-can-i-enable-cfg"></a>Come è possibile abilitare la CFG?

Nella maggior parte dei casi, non è necessario modificare il codice sorgente. È sufficiente aggiungere un'opzione al progetto di Visual Studio 2015 e il compilatore e il linker abilitano la funzione CFG.

Il metodo più semplice consiste nel passare alle proprietà di configurazione delle proprietà di **\| \| configurazione \| C/C++ \| generazione del codice** e scegliere **Sì (/Guard: CF)** per la protezione del flusso di controllo.

![Proprietà cfg in Visual Studio](images/cfg-vs.png)

In alternativa, aggiungere **/Guard: CF** alle proprietà di progetto proprietà di **\| \| configurazione \| \| \| Opzioni aggiuntive della riga di comando di C/C++** (per il compilatore) e **/Guard: CF** to **Project Properties proprietà di \| \| configurazione \| \| \| Opzioni aggiuntive della riga di comando** (per il linker).

![Proprietà cfg per il compilatore](images/cfg-compiler.png)![Proprietà cfg per linker](images/cfg-linker.png)

Per ulteriori informazioni, vedere [/Guard (Abilita Guard flusso di controllo)](/cpp/build/reference/guard-enable-control-flow-guard?view=vs-2019) .

Se si compila il progetto dalla riga di comando, è possibile aggiungere le stesse opzioni. Se ad esempio si compila un progetto denominato test. cpp, usare **CL/Guard: CF test. cpp/link/Guard: CF**.

È anche possibile controllare dinamicamente il set di indirizzi di destinazione iCal che sono considerati validi da CFG usando [**SetProcessValidCallTargets**](/windows/desktop/api/memoryapi/nf-memoryapi-setprocessvalidcalltargets) dall'API di gestione della memoria. La stessa API può essere usata per specificare se le pagine sono destinazioni non valide o valide per la CFG. Per impostazione predefinita, le funzioni [**VirtualProtect**](/windows/desktop/api/memoryapi/nf-memoryapi-virtualprotect) e [**VirtualAlloc**](/windows/desktop/api/memoryapi/nf-memoryapi-virtualalloc) gestiscono un'area specificata di pagine eseguibili e di cui viene eseguito il commit come destinazioni di chiamata indirette valide. È possibile eseguire l'override di questo comportamento, ad esempio quando si implementa un compilatore just-in-time, specificando **destinazioni della pagina \_ \_ non valide** quando si chiama **VirtualAlloc** o non viene eseguito **\_ \_ alcun \_ aggiornamento** quando si chiama **VirtualProtect** come descritto in [**costanti di protezione della memoria**](/windows/desktop/Memory/memory-protection-constants).

## <a name="how-do-i-tell-that-a-binary-is-under-control-flow-guard"></a>Come è possibile stabilire se un file binario è sotto la protezione del flusso di controllo?

Eseguire lo [strumento DUMPBIN](/cpp/build/reference/dumpbin-reference) (incluso nell'installazione di visual studio 2015) dal prompt dei comandi di Visual Studio con le opzioni */headers* e */loadconfig* : **dumpbin/headers/loadConfig test.exe**. L'output di un file binario in CFG dovrebbe indicare che i valori dell'intestazione includono "Guard" e che i valori di configurazione di caricamento includono "CF instrumentato" e "FID Table present".

![output di dumpbin/headers](images/cfg-dumpbin-headers.png)

![output di DUMPBIN/loadConfig](images/cfg-dumpbin-loadconfig.png)

## <a name="how-does-cfg-really-work"></a>Come funziona la funzione CFG?

Le vulnerabilità software vengono spesso sfruttate fornendo dati improbabili, insoliti o estremi a un programma in esecuzione. Un utente malintenzionato può, ad esempio, sfruttare una vulnerabilità di overflow del buffer fornendo un maggior numero di input a un programma, quindi sovrascrivendo l'area riservata dal programma per mantenere una risposta. Questo potrebbe danneggiare la memoria adiacente che può avere un puntatore a funzione. Quando il programma chiama tramite questa funzione, può passare a una posizione non desiderata specificata dall'autore dell'attacco.

Tuttavia, una potente combinazione di supporto di compilazione e Runtime da CFG implementa l'integrità del flusso di controllo che limita strettamente la posizione in cui possono essere eseguite le istruzioni per le chiamate indirette.

Il compilatore esegue le operazioni seguenti:

1.  Aggiunge controlli di sicurezza leggeri al codice compilato.
2.  Identifica il set di funzioni nell'applicazione che sono destinazioni valide per le chiamate indirette.

Supporto del runtime, fornito dal kernel di Windows:

1.  Mantiene in modo efficiente lo stato che identifica destinazioni di chiamata indirette valide.
2.  Implementa la logica che verifica che una destinazione di chiamata indiretta sia valida.

Per illustrare:

![pseudocodice cfg](images/cfg-pseudocode.jpg)

Quando un controllo CFG ha esito negativo in fase di esecuzione, Windows termina immediatamente il programma, in modo da interrompere eventuali exploit che tentano di chiamare indirettamente un indirizzo non valido.

 

 

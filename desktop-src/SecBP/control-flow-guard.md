---
description: Control Flow Guard (CFG) è una funzionalità di sicurezza della piattaforma altamente ottimizzata creata per contrastare le vulnerabilità di danneggiamento della memoria.
ms.assetid: 116EAD64-7CAE-455C-BA43-9492F78DE873
title: Protezione del flusso di controllo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62186a86f821e7eb350381c7dfbc500c80dd040f4321a8f630c7d408937a8460
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119622818"
---
# <a name="control-flow-guard"></a>Protezione del flusso di controllo

## <a name="what-is-control-flow-guard"></a>Che cos'è Control Flow Guard?

Control Flow Guard (CFG) è una funzionalità di sicurezza della piattaforma altamente ottimizzata creata per contrastare le vulnerabilità di danneggiamento della memoria. L'inserimento di restrizioni rigide sulla posizione da cui un'applicazione può eseguire codice rende molto più difficile per gli exploit eseguire codice arbitrario tramite vulnerabilità come gli overflow del buffer. CFG estende le tecnologie di mitigazione degli exploit precedenti, ad esempio [/GS,](/cpp/build/reference/gs-buffer-security-check?view=vs-2019) [DEP](../memory/data-execution-prevention.md)e [ASLR.](/archive/blogs/michael_howard/address-space-layout-randomization-in-windows-vista)

Questa funzionalità è disponibile in Microsoft Visual Studio 2015 ed è in esecuzione nelle versioni "CFG-Aware" di Windows, ovvero le versioni x86 e x64 per Desktop e Server di Windows 10 e Windows 8.1 Update (KB3000850).

È vivamente consigliabile che gli sviluppatori abilitino CFG per le proprie applicazioni. Non è necessario abilitare CFG per ogni parte del codice, perché una combinazione di codice abilitato per CFG e non CFG verrà eseguita correttamente. Tuttavia, l'abilitazione di CFG per tutto il codice può aprire lacune nella protezione. Inoltre, il codice abilitato per CFG funziona correttamente nelle versioni "CFG-Unaware" di Windows ed è quindi completamente compatibile con esse.

## <a name="how-can-i-enable-cfg"></a>Come è possibile abilitare CFG?

Nella maggior parte dei casi non è necessario modificare il codice sorgente. È necessario aggiungere un'opzione al progetto Visual Studio 2015 e il compilatore e il linker abiliteranno CFG.

Il metodo più semplice è passare Project Proprietà di configurazione **\| \| \| C/C++ \| Code Generation** e scegliere Sì **(/guard:cf)** per Control Flow Guard.

![Proprietà cfg in Visual Studio](images/cfg-vs.png)

In alternativa, aggiungere **/guard:cf** Project Properties Configuration **\| Properties \| \| C/C++ \| Command Line Additional \| Options** (per il compilatore) e **/guard:cf** **a Project Properties Configuration Properties \| \| \| Linker Command Line Additional \| \| Options** (per il linker).

![Proprietà cfg per il compilatore](images/cfg-compiler.png)![Proprietà cfg per il linker](images/cfg-linker.png)

Per altre informazioni, vedere [/guard (Abilita controllo Flow Guard).](/cpp/build/reference/guard-enable-control-flow-guard?view=vs-2019)

Se si compila il progetto dalla riga di comando, è possibile aggiungere le stesse opzioni. Ad esempio, se si compila un progetto denominato test.cpp, usare **cl /guard:cf test.cpp /link /guard:cf**.

È anche possibile controllare dinamicamente il set di indirizzi di destinazione icall considerati validi da CFG usando [**SetProcessValidCallTargets**](/windows/desktop/api/memoryapi/nf-memoryapi-setprocessvalidcalltargets) dal API Gestione. La stessa API può essere usata per specificare se le pagine sono destinazioni valide o non valide per CFG. Per [**impostazione predefinita,**](/windows/desktop/api/memoryapi/nf-memoryapi-virtualprotect) le funzioni VirtualProtect e [**VirtualAlloc**](/windows/desktop/api/memoryapi/nf-memoryapi-virtualalloc) trattano un'area specificata di pagine eseguibili e di cui è stato eseguito il commit come destinazioni di chiamata indirette valide. È possibile eseguire l'override di questo comportamento, ad esempio quando si implementa un compilatore JIT, specificando **PAGE \_ TARGETS \_ INVALID** quando si chiama **VirtualAlloc** o **PAGE TARGETS NO \_ \_ \_ UPDATE** quando si chiama **VirtualProtect** come descritto in dettaglio in Costanti di protezione della [**memoria**](/windows/desktop/Memory/memory-protection-constants).

## <a name="how-do-i-tell-that-a-binary-is-under-control-flow-guard"></a>Come si fa a sapere che un file binario è sotto controllo Flow Guard?

Eseguire lo strumento [dumpbin](/cpp/build/reference/dumpbin-reference) (incluso nell'installazione di Visual Studio 2015) dal prompt dei comandi di Visual Studio con *le opzioni /headers* e */loadconfig:* **dumpbin /headers /loadconfig test.exe**. L'output per un file binario in CFG deve mostrare che i valori di intestazione includono "Guard" e che i valori di configurazione di caricamento includono "CF Instrumented" e "TABELLA FID presente".

![output da dumpbin /headers](images/cfg-dumpbin-headers.png)

![output da dumpbin /loadconfig](images/cfg-dumpbin-loadconfig.png)

## <a name="how-does-cfg-really-work"></a>Come funziona realmente CFG?

Le vulnerabilità software vengono spesso sfruttate fornendo dati improbabili, insoliti o estremi a un programma in esecuzione. Ad esempio, un utente malintenzionato può sfruttare una vulnerabilità di overflow del buffer fornendo più input del previsto a un programma, sovraccaricando così l'area riservata dal programma per contenere una risposta. Ciò potrebbe danneggiare la memoria adiacente che può contenere un puntatore a funzione. Quando il programma chiama tramite questa funzione, può quindi passare a una posizione non intenzionale specificata dall'utente malintenzionato.

Tuttavia, una potente combinazione di compilazione e supporto in fase di esecuzione da CFG implementa l'integrità del flusso di controllo che limita strettamente la posizione in cui possono essere eseguite le istruzioni di chiamata indirette.

Il compilatore esegue le operazioni seguenti:

1.  Aggiunge controlli di sicurezza leggeri al codice compilato.
2.  Identifica il set di funzioni nell'applicazione che sono destinazioni valide per le chiamate indirette.

Supporto di runtime, fornito dal kernel Windows:

1.  Gestisce in modo efficiente lo stato che identifica destinazioni di chiamata indirette valide.
2.  Implementa la logica che verifica che una destinazione di chiamata indiretta sia valida.

Per illustrare:

![pseudocodice cfg](images/cfg-pseudocode.jpg)

Quando un controllo CFG non riesce in fase di esecuzione, Windows termina immediatamente il programma, interrompendo così qualsiasi exploit che tenta di chiamare indirettamente un indirizzo non valido.

 

 

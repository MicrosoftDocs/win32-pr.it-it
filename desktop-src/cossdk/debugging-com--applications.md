---
description: Le tecniche di debug per le applicazioni COM+ dipendono dal linguaggio in cui si sceglie di scrivere il componente.
ms.assetid: 781a0b3f-2bd0-435b-b6fe-4469cc02e8b6
title: Debug di applicazioni COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4bcce186a954098bdebd4e7e326328b8be269a88ed9567a3e63185662fcda3d0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118307305"
---
# <a name="debugging-com-applications"></a>Debug di applicazioni COM+

Le tecniche di debug per le applicazioni COM+ dipendono dal linguaggio in cui si sceglie di scrivere il componente.

Se si esegue il codice in Microsoft Visual C++, è possibile avviare il debugger in C++ oppure, con un client remoto, è possibile eseguire il debug tramite ILC (Remote Procedure Control) OLE e il debug JIT (Just-In-Time). È sempre possibile usare lo strumento di amministrazione Servizi componenti per eseguire  il debug del componente con l'impostazione Avvio com+ nel **debugger** nella scheda Avanzate della finestra di dialogo Proprietà dell'applicazione  COM+. Per altre informazioni sul debug di componenti codificati in C++, vedere Debug di componenti [scritti in Visual C++](debugging-components-written-in-visual-c--.md).

A meno che non si eserviti il debug del multithreading, del rilevamento dei componenti, delle chiamate remote o dell'isolamento dei processi, è possibile usare l'ambiente microsoft Visual Basic a scopo di debug. [Debugging Components Written in Visual Basic](debugging-components-written-in-visual-basic.md) descrive il processo di debug all'interno di Visual Basic ambiente.

[L'argomento Debug nell'IDE Visual Basic](debugging-in-the-visual-basic-ide.md) fornisce una panoramica generale con linee guida, suggerimenti e una procedura per il debug nell'ambiente di sviluppo integrato (IDE).

Per altre informazioni sul debug di processi avanzati, vedere [Debugging Compiled Visual Basic Components](debugging-compiled-visual-basic-components.md).

> [!Note]  
> Sono state risolte diverse limitazioni associate all'Visual Basic per eseguire il debug dei componenti con MTS per COM+. Per altre informazioni, vedere [Supporto del debug Visual Basic COM+ in contrasto con MTS.](com--visual-basic-debugging-support-contrasted-with-mts.md)

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Gestione degli errori in COM+](handling-errors-in-com-.md)
</dt> </dl>

 

 




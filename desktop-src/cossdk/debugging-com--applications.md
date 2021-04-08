---
description: Le tecniche di debug per le applicazioni COM+ dipendono dal linguaggio in cui si sceglie di scrivere il componente.
ms.assetid: 781a0b3f-2bd0-435b-b6fe-4469cc02e8b6
title: Debug di applicazioni COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db096ceb525cd988afa55e49cc88fda0ddf52549
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748866"
---
# <a name="debugging-com-applications"></a>Debug di applicazioni COM+

Le tecniche di debug per le applicazioni COM+ dipendono dal linguaggio in cui si sceglie di scrivere il componente.

Se si esegue il codice in Microsoft Visual C++, è possibile avviare il debugger in C++ o, con un client remoto, è possibile eseguire il debug utilizzando il controllo remoto OLE procedure (RPC) e il debug JIT (just-in-Time). È sempre possibile usare lo strumento di amministrazione Servizi componenti per eseguire il debug del componente con l'impostazione **avvio com+ in debugger** nella scheda **Avanzate** della finestra di dialogo **proprietà** dell'applicazione com+. Per ulteriori informazioni sul debug di componenti codificati in C++, vedere [debug di componenti scritti in Visual C++](debugging-components-written-in-visual-c--.md).

A meno che non si stia attualmente eseguendo il debug di multithreading, rilevamento componenti, chiamate remote o isolamento dei processi, è possibile usare l'ambiente Microsoft Visual Basic a scopo di debug. Il [debug di componenti scritti in Visual Basic](debugging-components-written-in-visual-basic.md) descrive il processo di debug all'interno di un ambiente Visual Basic.

Il debug dell'argomento [nell'IDE di Visual Basic](debugging-in-the-visual-basic-ide.md) fornisce una panoramica generale con linee guida, suggerimenti e una procedura per il debug nell'Integrated Development Environment (IDE).

Per visualizzare altre informazioni sul debug di processi avanzati, vedere [debug di componenti Visual Basic compilati](debugging-compiled-visual-basic-components.md).

> [!Note]  
> Per COM+ sono state risolte diverse limitazioni associate all'uso dell'ambiente Visual Basic per eseguire il debug dei componenti con MTS. Per ulteriori informazioni, vedere [COM+ Visual Basic il supporto per il debug in contrapposizione a MTS](com--visual-basic-debugging-support-contrasted-with-mts.md).

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Gestione degli errori in COM+](handling-errors-in-com-.md)
</dt> </dl>

 

 




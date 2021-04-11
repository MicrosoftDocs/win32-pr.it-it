---
description: Quando un oggetto viene attivato in un determinato contesto, le chiamate successive a o da esso, all'interno del contesto, vengono gestite in modo diverso rispetto alle chiamate oltre il limite del contesto.
ms.assetid: 9e234b41-f269-4674-adc4-12018277a14b
title: Intercettazione di chiamate tra contesti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d70bc8bff83d02b13656f9854f0e6d16cd4e173
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104342261"
---
# <a name="interception-of-cross-context-calls"></a>Intercettazione di chiamate tra contesti

Quando un oggetto viene attivato in un determinato contesto, le chiamate successive a o da esso, all'interno del contesto, vengono gestite in modo diverso rispetto alle chiamate oltre il limite del contesto. Le chiamate attraverso il limite del contesto vengono gestite con proxy leggeri. Questi proxy gestiscono la mediazione necessaria per modificare l'ambiente di runtime da uno che lo inserisce nel chiamante, in modo che sia in grado di ospitare il chiamato. Questo processo è noto come *intercettazione*.

L'intercettazione delle chiamate tra contesti è necessaria perché gli oggetti in contesti diversi hanno requisiti di runtime diversi, questo è esattamente il motivo per i contesti. COM+ intercetta tutti i riferimenti a oggetti passati come parametri del metodo e li converte automaticamente in proxy in modo che possano essere utilizzati nel nuovo contesto.

Se si condividono i riferimenti agli oggetti tra i limiti del contesto in altri modi, ad esempio in variabili globali, è sempre necessario usare [**CoMarshalInterface**](/windows/desktop/api/combaseapi/nf-combaseapi-comarshalinterface) e [**CoUnmarshalInterface**](/windows/desktop/api/combaseapi/nf-combaseapi-counmarshalinterface). Queste funzioni possono convertire un riferimento a un oggetto in un proxy utilizzabile in un contesto diverso. Non condividere mai un riferimento a un oggetto non elaborato tra i limiti del contesto.

Il comportamento delle chiamate nel contesto può avere conseguenze indesiderate nel caso di oggetti che espongono interfacce che non possono essere sottoposte a marshalling. In questo caso, è probabile che si voglia insistere sul fatto che l'oggetto di cui non è possibile effettuare il marshalling venga attivato solo nel contesto del chiamante e mai nel suo contesto. Questa operazione può essere eseguita selezionando l'opzione **deve essere attivata nel contesto del chiamante** nella scheda **attivazione** della pagina **proprietà** componente. Per istruzioni dettagliate, vedere [applicazione dell'attivazione nel contesto del chiamante](enforcing-activation-in-the-caller-s-context.md) .

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Attivazione del contesto](context-activation.md)
</dt> </dl>

 

 

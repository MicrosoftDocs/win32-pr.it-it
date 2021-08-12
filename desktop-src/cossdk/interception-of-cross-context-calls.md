---
description: Quando un oggetto viene attivato in un determinato contesto, le chiamate successive a o da esso, all'interno del contesto, vengono gestite in modo diverso rispetto alle chiamate attraverso il limite del contesto.
ms.assetid: 9e234b41-f269-4674-adc4-12018277a14b
title: Intercettazione di chiamate tra contesti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a3a969479419b75313f8b439f3cf9ffc7b94946e9007752ccc4e99a54cd6ad7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118547838"
---
# <a name="interception-of-cross-context-calls"></a>Intercettazione di chiamate tra contesti

Quando un oggetto viene attivato in un determinato contesto, le chiamate successive a o da esso, all'interno del contesto, vengono gestite in modo diverso rispetto alle chiamate attraverso il limite del contesto. Le chiamate attraverso il limite del contesto vengono gestite con proxy leggeri. Questi proxy gestiscono tutto ciò che è necessario per modificare l'ambiente di run-time da uno che supporta il chiamante a uno che supporta il chiamato. Questo processo è noto come *intercettazione*.

L'intercettazione delle chiamate tra contesti è necessaria perché gli oggetti in contesti diversi hanno requisiti di run-time diversi. Questo è esattamente il motivo dei contesti. COM+ intercetta tutti i riferimenti a oggetti passati come parametri del metodo e li converte automaticamente in proxy in modo che siano utilizzabili nel nuovo contesto.

Se si condividono riferimenti a oggetti attraverso limiti di contesto con altri mezzi, ad esempio nelle variabili globali, è consigliabile usare sempre [**CoMarshalInterface**](/windows/desktop/api/combaseapi/nf-combaseapi-comarshalinterface) e [**CoUnmarshalInterface.**](/windows/desktop/api/combaseapi/nf-combaseapi-counmarshalinterface) Queste funzioni possono convertire un riferimento a un oggetto in un proxy utilizzabile in un contesto diverso. Non condividere mai un riferimento a un oggetto non elaborato tra i limiti di contesto.

Il comportamento delle chiamate nel contesto può avere conseguenze indesiderate nel caso di oggetti che espongono interfacce di cui non è possibile effettuare il marshalling. In questa circostanza, è probabile che si voglia insodette che l'oggetto di cui non è possibile effettuare il marshalling sia attivato solo nel contesto del chiamante e mai nel proprio contesto. A tale scopo, selezionare **l'opzione Deve essere attivato** nel contesto del chiamante nella **scheda Attivazione** della pagina **Proprietà del** componente. Per [istruzioni dettagliate, vedere Applicazione dell'attivazione](enforcing-activation-in-the-caller-s-context.md) nel contesto del chiamante.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Attivazione del contesto](context-activation.md)
</dt> </dl>

 

 
